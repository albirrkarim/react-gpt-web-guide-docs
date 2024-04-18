![GPT Web Guide](./img/sosmed.png)

**React GPT Web Guide** - Interactable AI 3D Avatar that have controll over your frontend website

See the [demo](https://react-gpt-web-guide.vercel.app)

This is the Documentation for private repo [demo website](https://github.com/albirrkarim/demo-website-gpt-web-guide) and [npm package](https://github.com/albirrkarim/react-gpt-web-guide)

**Table Of Contents**

- [A. Introduction](#a-introduction)
- [B. Todo](#b-todo)
- [C. API & Example Code](#c-api--example-code)
- [D. Changelog](#d-changelog)
- [E. Disclaimer & Warranty](#e-disclaimer--warranty)
- [F. FAQ](#f-faq)
- [G. Payment](#g-payment)

<br/>

# Docs for v1.4.2

## A. Introduction

### What i want?

Recently, I worked on AI accessibility tools The idea is it's like conversational AI that can guide the user with a disability maybe a motoric, or visual problem and I also have an exhibition platform (Mozilla hubs based) that requires NPC that can act as a guide to my user.

Both using react JS for the implementation (UI) and for handling the complex logic, and unstructured data we need strong understanding capabilities which open AI chat completion API has.

What position is this package in your production apps?

Imagine the human body, They have a mouth (text-to-speech), ears (speech-to-text), a brain (chat GPT API), hands (programmatically calling function to do some action), eyes (the function that searches the web section, button, form, etc).

<br/>

### Use Cases

- Conversational AI
- Web Metaverse NPC
- AI Web Accessibility

<br/>

### How It Works

![GPT Web Guide Overview](./img/React-GPT-Web-Guide.png)

#### The Interaction

Using [Browser SpeechSynthesis API](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis) (text-to-speech) so the ai can speak and using [React Speech Recognition](https://github.com/JamesBrill/react-speech-recognition) for Speech Recognition (speech to text)

#### As Web Accessibility Tools

Can be used as interactable web accessibility.

Screen Reader (all menus, buttons, form). Understand the user say and do the actions.

#### As Metaverse NPC

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

## B. Todo

- [ ] Let me know what you want from this package, please write it on issues tab
- [ ] Make Youtube Video
- [ ] Make API Metaverse NPC (0%)
- [ ] Example Code for Metaverse NPC (0%)
- [ ] Example Code for AI Web Accessibility (0%)
- [ ] Give source code comments (10%)
- [ ] API docs (0%)
- [ ] Automate the testing (Prompt Test, Unit Test)(2%)

<br/>
<br/>

## C. API & Example Code

See [API.md](API.md)

See [EXAMPLE_CODE.md](EXAMPLE_CODE.md)

Contain simple example code, the full example code and implementation example using source code from demo website. the source code of demo website is included when you buy this package.

<br/>

# D. Changelog

Changelog contains information about new feature, fix bug, and what you should do when the version is update.

See [CHANGELOG.md](CHANGELOG.md)

<br/>

# E. Disclaimer & Warranty

There's no refund. I love feedback from my customers. You can write on the issue tab so when i have time i can try to solve that and deliver for the next update.

<br/>

<br/>

# F. FAQ

<details>
  <summary>Why it's expensive? Why it's not opensource package?</summary>
  
  <br/>

Try yourself to make this package. you will be grateful I am selling it cheap.

Well, i need money to funding the research, you know that making package is cost a lot of time and of course money.

</details>

<br/>

<details>
  <summary>Is Chat GPT api sometime give wrong output?</summary>

<br/>

Yes, the ai not always 100% accurate, thats why i make prompt testing (which call real API not mocking) and unit test using [jest library](https://jestjs.io).

</details>

<br/>

<details>
  <summary>Voice Recognition is good enough?</summary>

<br/>

For now i use [react speech recognition](https://github.com/JamesBrill/react-speech-recognition) package. the accuracy and the supported device is also based on that package.

</details>

<br/>

<details>
  <summary>Is the open ai API cost expensive?</summary>

<br/>

I try to do efficiency for each prompt so the cost is minimum and keep accurate.

</details>

<br/>

<details>
  <summary>Is it well documented and well crafted?</summary>
  
  <br/>

You can see the docs in this repo, and this package is written with typescript, and tested using jest to make sure the quality.

You don't have to read all the docs in here, because this package now support [VS Code IntelliSense](https://code.visualstudio.com/docs/editor/intellisense) what is that? simply its when you hover your mouse into some variable or function [VS Code](https://code.visualstudio.com/) will show some popup (simple tutorial) what is the function about, examples, params, etc...

Just use the source code from demo website, you can literally just understand the package.

https://github.com/albirrkarim/react-speech-highlight-demo/assets/29292018/05d325f9-469c-47e9-97d3-10053628e18c

</details>

<br/>
<br/>

## G. Payment

<br/>

The price is $140 USD. 

I accept various payment method:

<a href="https://github.com/sponsors/albirrkarim" title="Github Sponsors">
    <img src="https://github.com/albirrkarim/laravel-react-starter-kit-pro/assets/29292018/00e008ed-8d31-4b4c-a54d-a53ac62d9f91" width="350em">
</a>

<br/>
<br/>

When you country doesn't have acccess to github sponsors, you can use [wise.com](https://wise.com/invite/dic/albirrkarims). You can adjust the price (USD $140) into your currency then directly send with your currency using [wise](https://wise.com/invite/dic/albirrkarims).

<a href="https://wise.com/pay/me/albirrkarims" title="Wise Payment">
    <img src="https://github.com/albirrkarim/albirrkarim/assets/29292018/7a5fba67-9ec0-4401-b65b-780306128e87" title="@albirrkarims-wisetag" width="200em">
</a>

<br/>
<br/>

If you are in indonesia (my country) you can easily transfer through bank and e wallet (gopay, shopee pay, jenius)

<img src="./img/payment.png" width="350em">

<br/>
<br/>
