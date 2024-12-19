---
Order: 91
TOCTitle: Announcing Copilot Free in VS Code
PageTitle: Announcing a free GitHub Copilot for VS Code
MetaDescription: Announcing a free plan for GitHub Copilot in Visual Studio Code.
Date: 2024-12-18
Author: Burke Holland
---

# Announcing a free GitHub Copilot for VS Code

December 18, 2024 by Burke Holland, @burkeholland

We're excited to announce an all new **free plan for GitHub Copilot**, available for everyone today in VS Code. All you need is a GitHub account. No trial. No subscription. No credit card required.

[Enable GitHub Copilot Free](https://aka.ms/vscode-activatecopilotfree)

You can click on the link above or just enable GitHub Copilot right from within VS Code like so...

<video src="blog-video-v2.mp4" title="Copilot Edits video" controls poster="copilot-free.jpg"></video>

With GitHub Copilot Free you get **2000 code completions/month**. That's about 80 per working day - which is a lot. You also get **50 chat requests/month**, as well as **access to both GPT-4o and Claude 3.5 Sonnet models**.

If you hit these limits, ideally it's because Copilot is doing its job well, which is to help you do yours! If you find you need more Copilot, the [paid Pro plan](https://github.com/features/copilot#pricing-2) is unlimited and provides access to additional models like **o1** and **Gemini** (coming in the new year).

With this announcement, GitHub Copilot becomes a core part of the VS Code experience. The team has been hard at work, as always, improving that experience with brand new AI features and capabilities.  Let’s take a look at some of the newer additions to GitHub Copilot that dropped in just the past few months. This is your editor, redefined with AI.

## Work with multiple files using Copilot Edits

[Copilot Edits](https://code.visualstudio.com/docs/copilot/copilot-edits) is a multi-file editing experience that you can open from the top of the chat side bar. Given a prompt, Edits will propose changes across files including creating new files when needed. This gives you the conversational flow of chat combined with the power of Copilot's code generation capabilities. The result is something you have to try to believe.

<video src="../../11/12/blog-video-demo.mp4" title="Copilot Edits video" autoplay muted controls></video>

**Try this:** Build a native mobile app using Flutter. I [built a game last weekend](https://youtu.be/Vj13SdN6OxU?si=sUvbBw0KSQ5q6iWh) and I've never used Flutter in my life.

## Multiple models, your choice

Whether you're using [Chat](https://code.visualstudio.com/docs/copilot/copilot-chat), [Inline Chat](https://code.visualstudio.com/docs/copilot/getting-started-chat#_stay-in-the-flow-with-inline-chat), or [Copilot Edits](https://code.visualstudio.com/docs/copilot/copilot-edits), you get to decide who your pair programmer is.

![AI model selection menu in VS Code.](model-picker.png)

**Try this:** Use 4o to generate an implementation plan for a new feature and then feed that prompt to Claude in [GitHub Copilot Edits](https://code.visualstudio.com/docs/copilot/copilot-edits) to build it.

## Custom instructions

Tell GitHub Copilot exactly how you want things done with [custom instructions](https://code.visualstudio.com/docs/copilot/copilot-customization). These instructions are passed to the model with every request, allowing you to specify your preferences and the details that the model needs to know to write code the way you want it.

You can specify these at the editor or project level. We'll even pick them up automatically if you include a `.github/copilot-instructions.md` file in your project. These instructions can easily be shared with your team, so everyone can be on the same page - including GitHub Copilot.

For example...

```markdown
## React 18
* Use functional components
* Use hooks for state management
* Use TypeScript for type safety

## SvelteKit 4
* Use SSR for dynamic content rendering
* Use static site generation (SSG) for pre-rendered static pages.

## TypeScript
* Use consistent object property shorthand: const obj = { name, age }
* Avoid implicit any
```

**Try this:** Ask Copilot to generate the command to dump your database schema to a file and then set that file as one of your custom instructions.

## Full project awareness

GitHub Copilot has AI powered domain experts that you can mention with the `@` syntax. We call these, "participants". The [`@workspace` participant](https://code.visualstudio.com/docs/copilot/workspace-context) is a domain expert in the area of your entire codebase.

<video src="workspace-v2.mp4" title="VS Code's source control view showing a staged file. A commit message gets auto-generated by clicking a sparkle icon based on the staged changes" autoplay muted controls></video>

GitHub Copilot will also do intent detection (as seen in the video) and include the `@workspace` automatically if it sees you are asking a question that requires full project context.

**Try this:** Type `/help` into the chat prompt to see a list of all the particpants in GitHub Copilot and their various areas of expertise, as well as slash commands that can greatly reduce prompting.

## Naming things and other hard problems

They say naming things is one of the hardest problems in computer science. Press `F2` to rename something, and GitHub Copilot will give you some suggestions based on how that symbol is implemented and used in your code.

<video src="copilot-rename-v2.mp4" title="Copilot Edits video" autoplay muted controls></video>

**Try this:** If you don't know what to call something, don't overthink it. Just call it `foo` and implement it. Then hit `F2` and let GitHub Copilot suggest a name for you.

## Speak your mind

Select the microphone icon to start a voice chat. This is powered by the free, cross-platform [VS Code Speech extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-speech) that runs on local models. No 3rd party app required.

![VS Code with file list and voice input active.](vscode-speech.png)

**Try this:** Use Speech with GitHub Copilot Edits to prototype your next app. You can literally talk your way to a working demo.

## Be a terminal expert

With terminal chat, you can do just about anything in your terminal. Press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>i</kbd> while in the VS Code terminal and tell GitHub Copilot what you want to do. Copilot can also explain how to fix failed shell commands by analyzing the error output.

For instance, I know that I can use the [ffmpeg library](https://ffmpeg.org/) to extract frames from videos, but I don't know the syntax and flags. No problem!

![Terminal displaying a script to extract video frames.](terminal-inline-chat.png)

**Try this:** The next time you get an error in your terminal, look for the sparkle icon next to your prompt. Select it to have GitHub Copilot fix, explain, or even auto-correct the shell command for you.

## No fear of commitment

No more commits that say "changes". GitHub Copilot will suggest a commit message for you based on the changes you've made and your last several commit messages. You can [use custom instructions for commit generation](https://code.visualstudio.com/docs/copilot/copilot-customization#_define-commit-message-generation-custom-instructions) to format the messages _exactly_ the way you want.

<video src="ccdt-commit-msgs.mp4" title="Copilot Edits video" autoplay muted controls></video>

**Try this:** Go beyond commits. Install the [GitHub Pull Requests and Issues extension](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) and you can generate pull request descriptions, get summaries of pull requests and even get suggested fixes for issues. All without leaving VS Code.

## Extensions are all you need

Every VS Code extension can tie directly into the GitHub Copilot APIs and offer a customized AI experience. Check out MongoDB with [their extension](https://marketplace.visualstudio.com/items?itemName=mongodb.mongodb-vscode) that can write impressively complex queries, use fuzzy search and a lot more...

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/MLWlWrRAb4w?si=FzYwY_lOLUlfOmQ7" title="VS Code MongoDB extension" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**Try this:** Build your own extension for GitHub Copilot using GitHub Copilot! We've created some new tutorials that show you how to [build a code tutor chat paricipant](https://code.visualstudio.com/api/extension-guides/chat-tutorial) or [generate AI-powered code annotations](https://code.visualstudio.com/api/extension-guides/language-model-tutorial).

## A vision for the future

This last one is a preview of something we're adding to GitHub Copilot soon, but it's way too cool not to show you right now.

Install the [Vision Copilot Preview extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-copilot-vision) and ask GitHub Copilot to generate an interface based on a screenshot or markup.

<video src="copilot-vision-generate-ui.mp4" title="Copilot Edits video" autoplay muted controls></video>

Or use it to generate alt text for an image.

<video src="copilot-vision-markdown.mp4" title="Copilot Edits video" autoplay muted controls></video>

**Try this:** Mock up a UI using Figma or Sketch (or PowerPoint - it's ok if you do that. I do it too). Then use `@vision` to generate the UI. You can even tell it which CSS framework to use.

_Note:_ Vision is in preview today and requires you to have your own OpenAI, Anthropic, or Gemini API key. The key will not be required when we release it as part of GitHub Copilot. Coming Soon!

## Keeping up with GitHub Copilot

There's so much more GitHub Copilot we want to show you, but nothing can replace the experience of trying it for yourself. If you're just getting started, we recommend you check out [these 3 short videos](https://github.com/features/copilot/getting-started) to bring you up to speed quickly on the Copilot UI, as well as learning some prompt engineering best practices.

We ship updates and new features for GitHub Copilot every month. The best way to keep up with the latest and greatest in AI coding is to follow us on [X](https://twitter.com/code), [Bluesky](https://bsky.app/profile/vscode.dev), [LinkedIn](https://www.linkedin.com/showcase/vs-code/), and even [TikTok](https://www.tiktok.com/@vscode). We'll give you the updates as they drop - short and sweet - right in your feed.

And if you've got feedback, we'd love to hear it. Feel free to @ us on social or drop an issue or feature request on the [GitHub Copilot extension issues repo](https://github.com/microsoft/vscode-copilot-release).

## GitHub Copilot in other places

As part of the free tier, you will also be able to use GitHub Copilot on GitHub.com.

While we work with GitHub to build the Visual Studio Code experience, Copilot itself is not exclusive to VS Code. You may be wondering about editors like Visual Studio. Will those users get a free Copilot offering as well?

Yes. Absolutely. Check out [this blog post](https://aka.ms/copilot-free-vs) from the VS team on what works today and what’s coming shortly.

## The AI code editor for everyone

2025 is going to be a huge year for GitHub Copilot, now a core part of the overall VS Code experience. We hope that you’ll join us on the journey to redefine the code editor. Again.

[Enable GitHub Copilot Free](https://aka.ms/vscode-activatecopilotfree)

Happy Coding!

Burke Holland @burkeholland