# API

The api is a function that you can use to integrate this package into your apps. When read this api docs you can toggle `Outline` (see top right) menu in github so you can navigate easily.

This package is written with typescript, You don't have to read all the docs in here, because this package now support [VS Code IntelliSense](https://code.visualstudio.com/docs/editor/intellisense) what is that? simply its when you hover your mouse into some variable or function [VS Code](https://code.visualstudio.com) will show some popup (simple tutorial) what is the function about, examples, params, etc...

https://github.com/albirrkarim/react-speech-highlight-demo/assets/29292018/05d325f9-469c-47e9-97d3-10053628e18c

```js
import {
  // Main
  readThisScreen,
  useGPTWebGuide,
  GPTWebGuideProvider,

  // Utils
  speak,
  setGPTWebGuideStatus,
  startRecog,
  stopRecog,
  translateTo,
  openaiChatCompletionsSimple,

  // Sharing state & constant
  isScreenReaderActive,
  isVoiceCommandActive,
  CONFIG_OPT,
  AI_STATUS_OPT,
  ACTION_TYPE,

  // Compatibility tools
  isChrome,
  isUsingAndroid,
  isUsingMozilla,
  isUsingSafari,
  isUsingiPad,
} from "react-gpt-web-guide";
```

## Table of content

- [A. Main](API.md#a-main)

- [B. Utils](API.md#b-utils)

- [C. Sharing state & constant](API.md#c-sharing-state--constant)

- [D. Compatibility tools](API.md#d-compatibility-tools)

## A. Main

### readThisScreen()

This function to trigger the ai to read current page.

```js
useEffect(() => {
  readThisScreen({
    this_page_about: "You are on the demo website of GPT Web Guide",
    element: document, // what html element should ai to read
    callback: () => {
      // When ai done read the screen
    },
  });
}, []);
```
<br/>

### GPTWebGuideProvider

To provide the context of the GPT Web Guide. so the react state from the hook `useGPTWebGuide` can be shared accross the app components.

<details>
  <summary>Show Code example</summary>

  ```jsx
  import { useSnackbar } from "notistack";
  import { getActionData } from "@/app/Demo/Widget/helper/utils";
  import { DEMO_KNOWLEDGE } from "@/app/Demo/data/initialKnowledge";
  import { CONFIG_OPT, type ConfigGPTWebGuide, GPTWebGuideProvider } from "@lib/react-gpt-web-guide";
  import micOffSoundEffect from "@/app/assets/sound/mic-off.mp3";
  import micOnSoundEffect from "@/app/assets/sound/mic-on.mp3";

  /**
   * This is for GPT Web Guide
   * 
   * Don't forget to wrapp your app with the AssistantWrapper component
   * So the state of the useGPTWebGuide will be available accross the app
   */
  const AssistantWrapper = ({ children }: { children: JSX.Element }): JSX.Element => {
    const { enqueueSnackbar } = useSnackbar();
    const actionsData = getActionData(enqueueSnackbar);

    const initialConfig: Partial<ConfigGPTWebGuide> = {
      [CONFIG_OPT.siteLang]: "en-US",
      [CONFIG_OPT.micOffSoundEffect]: micOffSoundEffect,
      [CONFIG_OPT.micOnSoundEffect]: micOnSoundEffect,
    }

    return (
      <GPTWebGuideProvider
        initialKnowledge={DEMO_KNOWLEDGE}
        initialActionsData={actionsData}
        config={initialConfig}
      >
        {children}
      </GPTWebGuideProvider>
    );
  };

  export default AssistantWrapper;
  ```
</details>


### useGPTWebGuide()

The `useGPTWebGuide` is the main hook.

#### Hook

```js
import { CONFIG_OPT, useGPTWebGuide } from "@lib/react-gpt-web-guide";

const { stateRecog, stateGuide, action, prepare, askGPT } = useGPTWebGuide();
```

#### Initial Knowledge

Initial knowledge define what your website about.

<details>
  <summary>Show initial knowledge example</summary>

<br/>

```js
const DEMO_KNOWLEDGE = [
  {
    role: "system",
    content:
      "You are a ai web guide, you can help user press buttons, input text, filling form, etc. User can interact with you through voice command.",
  },
  // {
  //   role: "system",
  //   content: `You are the guide of website named 'senarai istilah jawa' its javanese dictionary website`,
  // },
];
```

</details>

#### Initial Action data

Initial action data is define programatic action.

<details>
  <summary>Show initial action example</summary>

<br/>

```js
const goodsDataJSON = [
  {
    name: "Wooden Chair",
    description: "Good chair",
    price: 20,
  },
  {
    name: "Steel Chair",
    description: "Good chair",
    price: 30,
  },
  {
    name: "Steel Table",
    description: "Good table",
    price: 40,
  },
];

const INITIAL_ACTION_DATA = [
  // Define the custom command
  // Sometimes you want add custom action and can be handled programmatically
  {
    name: "Place order",
    description: "User want to place order some goods",
    type: "place_order",
    format: "Order {goods}",
    param_options: {
      goods: goodsDataJSON,
    },
    onAction: (params) => {
      console.log("Triggering onAction Place order with params: ");
      console.log(params);
      enqueueSnackbar(
        "Triggering onAction Place order with params: " +
          JSON.stringify(params),
        {
          variant: "info",
        }
      );
    },
  },
  {
    name: "Search",
    description: "Searching with some keyword",
    type: ACTION_TYPE.SEARCH,
    format: "search {keywords}",
    onAction: (params) => {
      console.log("Triggering onAction search with params: ");
      console.log(params);
      //   {
      //     keywords: "elephant",
      //   }

      enqueueSnackbar(
        "Triggering onAction search with params: " + JSON.stringify(params),
        {
          variant: "info",
        }
      );
    },
  },
  {
    name: "feedback",
    description:
      'Users can provide suggestions, criticism, input to the website | This form feedback have 3 inputs. input "name"  have placeholder "Name", input "email"  have placeholder "Email", input "message" doesn\'t have placeholder ',
    type: "fill form",
    format: "feedback {name}  {email}  {message} ",
    onAction: (params) => {
      console.log("Triggering onAction feedback with params: ");
      console.log(params);
      // {
      //   name: "susanto"
      //   email:"email@gmail.com"
      //   message:"this website is good"
      // }
    },
  },
];
```

</details>

<br/>

## B. Utils

### speak()

Built in speak function

### setGPTWebGuideStatus()

Function to set ai status. see [AI_STATUS_OPT](API.md#ai_status_opt)

```js
// Import the constant from package so the value can be constant (avoid typo)
import { AI_STATUS_OPT } from "@lib/react-gpt-web-guide";

// Use like this
setGPTWebGuideStatus(AI_STATUS_OPT.TRANSLATE);
setGPTWebGuideStatus(AI_STATUS_OPT.SPEAKING);
// etc
```

### startRecog()

To start voice recognition

### stopRecog()

To stop voice recognition

### translateTo()

To translate some text into some language

```js
let defaultLanguge = "en-US";

// id-ID is language code for indonesia
const translated_text = await translateTo("hello", "id-ID", defaultLanguge);

console.log(translated_text); // halo
```

### openaiChatCompletionsSimple()

<br/>

## C. Sharing state & constant

Sharing package state and constant.

```jsx
import {
  isScreenReaderActive,
  isVoiceCommandActive,
  CONFIG_OPT,
  AI_STATUS_OPT,
  ACTION_TYPE,
} from "@lib/react-gpt-web-guide";
```

<br/>

## D. Compatibility tools

Contain Compatibility tools

```jsx
import {
  isChrome,
  isUsingAndroid,
  isUsingMozilla,
  isUsingSafari,
  isUsingiPad,
} from "@lib/react-gpt-web-guide";
```

Again, this package is using jsdoc so you can see each docs in your code editor with just hover your mouse into some variable. [see video above](#api)