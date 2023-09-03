## Introduction

![GPT Web Guide](./img/React-GPT-Web-Guide.png)

**React GPT Web Guide** Imagine you have an AI that can act as guide in your website.

See the [demo](https://react-gpt-web-guide.vercel.app)

<br/>

## Can be used as

- Conversational AI
- Web Metaverse NPC
- AI Web Accessibility

<br/>

## How It Works

### The Interaction

Using [Browser SpeechSynthesis API](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis) (text-to-speech) so the ai can speak and using [React Speech Recognition](https://github.com/JamesBrill/react-speech-recognition) for Speech Recognition (speech to text)

### As Web Accessibility Tools

Can be used as interactable web accessibility.

Screen Reader (all menus, buttons, form). Understand the user say and do the actions.

### As Metaverse NPC

You can set programatic action. so the package can integrate into your system.

```js
[
  {
    name: "Search",
    description: "Searching with some keyword",
    type: ACTION_TYPE.SEARCH,
    format: "search {keywords}",
    onAction: (params) => {
      console.log("Triggering onAction 2 with params: ");
      console.log(params);
      // params:
      //   {
      //     keywords: "elephant",
      //   }

      // this function will called if the user want to search something
    },
  },
];
```

<br/>

## Feedback

Tell me what you think

Fill on the issue tab or Contact me:

Discord Username : albirrkarim

<br/>

## Support me

<a href='https://ko-fi.com/Q5Q0BC92X' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://cdn.ko-fi.com/cdn/kofi3.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

<a href="https://trakteer.id/albirrkarim" target="_blank"><img id="wse-buttons-preview" src="https://cdn.trakteer.id/images/embed/trbtn-red-2.png" height="40" style="border:0px;height:40px;" alt="Trakteer Saya"></a>
