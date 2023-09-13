# React GPT Web Guide

![GPT Web Guide](./img/React-GPT-Web-Guide.png)

**React GPT Web Guide** - Imagine you have an AI that can act as guide in your website. Can be use as AI Web Accessibility, Web Metaverse NPC, Conversational AI, etc.

See the [demo](https://react-gpt-web-guide.vercel.app)

This is the Documentation for private repo [demo website](https://github.com/albirrkarim/demo-website-gpt-web-guide) and [npm package](https://github.com/albirrkarim/react-gpt-web-guide)

**Table Of Contents**

- [A. Introduction](#a-introduction)
- [B. Can be used as](#b-can-be-used-as)
- [C. How It Works](#c-how-it-works)
- [D. Todo](#d-todo)
- [E. API](#e-api)
- [F. Example Code](#f-example-code)
- [G. Changelog](#g-changelog)
- [H. Disclaimer](#h-disclaimer)
- [I. Warranty](#i-warranty)
- [J. Feedback](#j-warranty)
- [K. FAQ](#k-faq)

# Docs for v1.4.0

# A. Introduction

Recently, i work for AI accessibility tools the idea is its like conversational ai that can guide the user with disability maybe motoric or have visual problem and I also have exhibition platform (mozilla hubs based) that require NPC that can act as guide to my user.

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

- [ ] Give source code comments (10%)
- [ ] API docs (10%)
- [ ] Automate the testing (Prompt Test, Unit Test)(20%)

<br/>
<br/>

# E. API

See [API.md](API.md)

<br/>

# F. Example Code

Contain simple example code, the full example code and implementation example using source code from demo website. the source code of demo website is included when you buy this package.

See [EXAMPLE_CODE.md](EXAMPLE_CODE.md)

<br/>

# G. Changelog

Changelog contains information about new feature, fix bug, and what you should do when the version is update.

See [CHANGELOG.md](CHANGELOG.md)

<br/>

# H. Disclaimer

There's no refund

<br>

# I. Warranty

I love feedback from my customers. You can write on the issue tab so when i have time i can try to solve that and deliver for the next update.

<br/>

# J. Feedback

Tell me what you think

Fill on the issue tab or Contact me:

Discord Username : albirrkarim

<br/>

# K. FAQ

Q: Why it's expensive?

A: Try yourself to make this package. you will be grateful I am selling it cheap.

<br/>

Q: Why it's not opensource package?

A: Well, i need money to funding the research, you know that making package is cost a lot of time and ofcourse money.

<br/>

Q: is Chat GPT api sometime give wrong output?

A: Yes, the ai not always 100% accurate, thats why i make prompt testing (which call real API not mocking) and unit test using [jest library](https://jestjs.io).

<br/>

Q: Voice Recognition is good enough?

A: For now i use [react speech recognition](https://github.com/JamesBrill/react-speech-recognition) package. the accuracy and the supported device is also based on that package.

<br/>

# Support me

<a href='https://ko-fi.com/Q5Q0BC92X' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://cdn.ko-fi.com/cdn/kofi3.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

<a href="https://trakteer.id/albirrkarim" target="_blank"><img id="wse-buttons-preview" src="https://cdn.trakteer.id/images/embed/trbtn-red-2.png" height="40" style="border:0px;height:40px;" alt="Trakteer Saya"></a>
