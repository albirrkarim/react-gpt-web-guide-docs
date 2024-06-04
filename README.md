![GPT Web Guide](./img/sosmed.png)

**React GPT Web Guide** - Interactable AI 3D Avatar that have controll over your frontend website

[Try the demo React GPT Web Guide](https://react-gpt-web-guide.vercel.app)

Ask something? discord: albirrkarim

<br/>

## Features:

- All the feature that [React Speech Highlight](https://github.com/albirrkarim/react-speech-highlight-demo) have. This is the extended product of that package.
- Tested function and prompts using [jest](https://jestjs.io) and code linting using [eslint](https://eslint.org)
- Efficient [Chat GPT API cost](https://openai.com/pricing)
- Support [Typescript](https://www.typescriptlang.org), [Js Doc](https://jsdoc.app), [VS Code Intellisense](https://code.visualstudio.com/docs/editor/intellisense)
- Flexible package API.
- Less dependencies.

<br/>
<br/>

# Docs React GPT Web Guide v1.4.3

This is the Documentation for private repo [demo website](https://github.com/Web-XR-AI-lab/demo-website-gpt-web-guide)


**Table Of Contents**

- [A. Introduction](#a-introduction)
- [B. Todo](#b-todo)
- [C. API & Example Code](#c-api--example-code)
- [D. Changelog](#d-changelog)
- [E. Disclaimer & Warranty](#e-disclaimer--warranty)
- [F. FAQ](#f-faq)
- [G. Payment](#g-payment)

<br/>

## A. Introduction

### What i want?

Recently, I worked on AI accessibility tools The idea is it's like conversational AI that can guide the user with a disability maybe a motoric, or visual problem. 

### Solution ?

Making some frontend-package (npm package) that can doing various thing.

What position is this package in your production apps?

Imagine the human body, They have a mouth (text-to-speech), ears (speech-to-text), a brain (chat GPT API), hands (programmatically calling function to do some action), eyes (the function that searches the web section, button, form, etc).

### Use Cases

- Conversational AI
- Web Metaverse NPC
- AI Web Accessibility

### How It Works

![GPT Web Guide Overview](./img/overview.png)

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

See [API.md](API.md) and [EXAMPLE_CODE.md](EXAMPLE_CODE.md) that contain simple example code.

The full example code and implementation example using source code from demo website. the source code of demo website is included when you buy this package.

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
  <summary>How can I provide information for my chatbot?</summary>

<br/>

This package have something like initial knowledge. its some JSON that tell about:

`What is your website about?` -> so when the User ask the AI they can answer correctly.

</details>

<br/>

<details>
  <summary>Is it well documented and well crafted?</summary>
  
  <br/>

You can see the docs in this repo, and this package is written with typescript, and tested using jest to make sure the quality.

You don't have to read all the docs in here, because this package now support [VS Code IntelliSense](https://code.visualstudio.com/docs/editor/intellisense) what is that? simply its when you hover your mouse into some variable or function [VS Code](https://code.visualstudio.com/) will show some popup (simple tutorial) what is the function about, examples, params, etc...

Just use the source code from demo website, you can literally just understand the package.

</details>

<br/>
<br/>

## G. Payment

<br/>

The price is $140 USD. 

React GPT Web Guide ($100) + [React Speech Highlight](https://github.com/albirrkarim/react-speech-highlight-demo) (~~$70~~)($40) = $140

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
