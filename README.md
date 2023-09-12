# React GPT Web Guide

![GPT Web Guide](./img/React-GPT-Web-Guide.png)

**React GPT Web Guide** Imagine you have an AI that can act as guide in your website.

See the [demo](https://react-gpt-web-guide.vercel.app)

This is the Documentation for [example implementation](https://github.com/albirrkarim/demo-website-gpt-web-guide)

**Table Of Contents**

- [A. Introduction](#a-introduction)
- [B. Can be used as](#b-todo)
- [C. How It Works](#b-todo)
- [D. Todo](#b-todo)
- [E. API](#c-api)
- [F. Example Code](#d-example-code)
- [G. Changelog](#e-changelog)
- [H. Disclaimer](#f-disclaimer)
- [I. Warranty](#g-warranty)
- [J. Feedback](#g-warranty)
- [K. FAQ](#h-faq)

# A. Introduction

Recently, i work for AI accessibility tools the idea is its like conversational ai that can guide the user with disability maybe motoric or have visual problem and I also have exhibition platform that require NPC that can act as guide to my user.

Both using react js for the implementation (UI) and for handing the complex logic, unstructured data we need strong understanding capabilities which open ai chat completion api have.

Then i make this package in about 1 month.

<br/>

# B. Can be used as

- Conversational AI
- Web Metaverse NPC
- AI Web Accessibility

<br/>

# C. How It Works

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

# D. Todo

<br/>

# E. API

<br/>

# F. Example Code

<br/>


# G. Changelog

<br/>

# H. Disclaimer

There's no refund

<br>
<br>

# I. Warranty

I love feedback from my customers. You can write on the issue tab so when i have time i can try to solve that and deliver for the next update.

<br/>

# J. Feedback

Tell me what you think

Fill on the issue tab or Contact me:

Discord Username : albirrkarim

# K. FAQ

Q: Why it's expensive?

A: Try yourself to make this package. you will be grateful I am selling it cheap.

<br/>

Q: Why it's not opensource package?

A: Well, i need money to funding the research, you know that making package is cost a lot of time and ofcourse money.

<br/>

# Support me

<a href='https://ko-fi.com/Q5Q0BC92X' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://cdn.ko-fi.com/cdn/kofi3.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

<a href="https://trakteer.id/albirrkarim" target="_blank"><img id="wse-buttons-preview" src="https://cdn.trakteer.id/images/embed/trbtn-red-2.png" height="40" style="border:0px;height:40px;" alt="Trakteer Saya"></a>
