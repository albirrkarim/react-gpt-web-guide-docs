# API

The api is a function that you can use to integrate this package into your apps. When read this api docs you can toggle `Outline` (see top right) menu in github so you can navigate easily.

```js
import {
  // Main
  readThisScreen,
  useGPTWebGuide,

  // Utils
  speak,
  setGPTWebGuideStatus,
  startRecog,
  stopRecog,
  translateTo,
  playAudio,

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
  openaiChatCompletionsSimple,
} from "react-gpt-web-guide";
```

## Table of content

A. Main

B. Utils

C. Sharing state & constant

D. Compatibility tools

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

### useGPTWebGuide()

The `useGPTWebGuide` is the main hook.

#### Hook

```js
import { CONFIG_OPT, useGPTWebGuide } from "../gpt-web-guide";

const { stateRecog, stateGuide, action, prepare, askGPT } = useGPTWebGuide({
  initial_knowledge: DEMO_KNOWLEDGE,
  initial_actions_data: INITIAL_ACTION_DATA,
  config: {
    [CONFIG_OPT.siteLang]: "en-US",
    micOnSoundEffect: "/mic_on.mp3",
    micOffSoundEffect: "/mic_off.mp3",
  },
});
```

#### Initial Knowledge

Initial knowledge define what your website about.

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

#### Initial Action data

Initial action data is define programatic action.

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

<br/>

## B. Utils

### speak()

Built in speak function

### setGPTWebGuideStatus()

Function to set ai status.

```js
// GTP Web Guide Status (in the package)
const AI_STATUS_OPT = {
  OFF: "off",
  IDLE: "idle",
  LISTENING: "listening",
  LISTENING_USER_COMMAND: "listening_user_command",
  SPEAKING: "speaking",
  THINKING: "thinking",
  TRANSLATE: "translate",
  SHUTDOWN: "shutdown",
};

// Import the constant from package so the value can be constant (avoid typo)
import { AI_STATUS_OPT } from "gpt-web-guide";

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

console.log(translated_text) // halo
```

### playAudio()

coming soon

<br/>

## C. Sharing state & constant

### isScreenReaderActive()

### isVoiceCommandActive()

### CONFIG_OPT

### AI_STATUS_OPT

### ACTION_TYPE

<br/>

## D. Compatibility tools

### isChrome()

### isUsingAndroid()

### isUsingMozilla()

### isUsingSafari()

### isUsingiPad()

### openaiChatCompletionsSimple()
