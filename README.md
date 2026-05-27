# How to: Write a README

> A software engineer’s guide to writing like a human person

[![Canvas](https://img.shields.io/badge/Canvas-E72429?logo=canvas&logoColor=white)](https://northeastern.instructure.com/courses/254655) [![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)](https://github.com/ljchandler21/howTo-Write-a-README) [![License](https://img.shields.io/badge/CC%20BY--NC--ND%204.0-ED592F?logo=creativecommons&logoColor=white)](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.en) [![Markdown](https://img.shields.io/badge/markdown-000000?logo=markdown&logoColor=white)](https://github.com/adam-p/markdown-here/wiki/markdown-cheatsheet) [![Spotify](https://img.shields.io/badge/Spotify-1ED760?logo=spotify&logoColor=white)](https://tinyurl.com/engw-feedback)

## Table of Contents

<details open> 
<summary>A Table of Contents can be optional based on your README's length</summary>

- [Overview](#overview)
- [Highlights](#highlights)
- [Usage](#usage)
  - [Getting Started](#getting-started)
    - [Prereqs](#prerequisites)
    - [Installation](#installation)
    - [Configuration](#configuration)
  - [Project Structure](#project-structure)
  - [API](#api)
  - [Important function calls](#important-function-calls)
- [Community/Contributing](#communitycontributions)
- [License](#license)
- [Citations](#acknowledgements)
</details>

## Overview

> What is a readme, and why does it matter?

When creating any new piece of client-centered software, one of the first things that any good developer should do is to start writing a README document to go along with all the changes they make. A readme is a markdown (text) document that outlines all the critical information relevant to a software project. It’s the first (and only thing) a user or contributor will see before investing time into installing the software, so it will give a strong impression of what they can expect from the rest of your project or codebase.

Before you write anything, it helps to know who you're writing for. A README typically serves three distinct readers: the evaluator (quickly deciding whether your project is worth their time), the implementer (just needs to get it running), and the contributor (wants to participate in the project's development). A good README holds all three in mind simultaneously, which is part of what makes it harder to write than it looks.

Most READMEs, or any good one at least, include a brief overview section with a paragraph or two explaining how the software works, what it does, why it was made (sometimes)/the problem it hopes to solve, and (sometimes) who made it. This section is, itself, meant to model what a good overview could look like.

## Highlights

A highlights section is a good practice to include near the top of your README. It can provide a quick overview of what makes your software unique, often presented as a short, bulleted list.

Some main takeaways of this guide:

- Should be inviting and approachable
- Identify and sell the most unique part of your software
- Concise is key; longer = more daunting
- Link everything, everywhere (documentation, deployments, etc.)
- Don’t be afraid to use Emojis or icons. Visuals = 1000 words.

## Usage

> What does it look like for someone to get your project running?

### Getting Started

Here is where you outline everything necessary for a user to install, set up, and run your project, including any prerequisites that need to be installed. Here, examples and blocks of code are king over trying to explain in words

#### Prerequisites

Before install of abc (your program), make sure that xyz is installed.

```bash
npm install -g xyz	# OR whatever the install command is
```

```bash
npm install -g efg	# A second dependency you rely on
```

#### Installation

Your software supports [*insert OS’s supported*].

> Linux x64? Linux arm64? macOS x64 and/or Apple Silicon? Windows x64 and/or arm64?

A step-by-step walkthrough is your best friend here

1. Get [your price] API key at [yourWebsite.com](yourWebsite.com)
2. Clone this repo

```bash
git clone github.com/your_username/repo_name.git
```

3. Install whatever packages

```bash
# with install script (access web from terminal) (typically the recommended way if available)
curl - fsSL https://yourSite.com/install | bash

# with bash
npm install
```

#### Configuration

_This section can sometimes be condensed with the previous one_

1. Enter your api key in `importantConfigFile.fileType`

```js
const API_KEY = ‘KeyFromStep1’;
```

2. Call the start command

```bash
npm run arg1 arg2 arg3
```

Explain the start arguments:

- `arg1` could be the number of ?
- `arg2` could be the username for system account
- `arg3` whatever you want it to be

### Project Structure

Here is where you provide more detailed information about the peoject for contributors to help with. These are typically things like implementation details that would scare off a more surface user, while aiding further development or interaction.

_Play it by ear with these. A file tree can be helpful but good organization/ low complexity can reduce the need, and if you dont expose an API then there obviously isn’t anything to list there._

#### File Structure

```
This is where/
├── You can outline/
│   |   ├── theOverallFileStructure.js
│   └────── ofYourProject.html
├── Typically including.txt
├── but not limited to.md
├── client/
│   ├── src/
|   ├── tests/
│   └── styles.css
├── server/
│   ├── src/
|   └── tests/
├── public/
│   └── favicon.ico
└── package.json
```

#### API

Your project's API is the language that lets other software interact with it while not having to directly call the functions or methods that your project contains. As such, it's important to lay out whatever critical API your project does have/use, so that other people can build your software into their already-existing stack, which is what you want at the end of the day. If you’re creating an API-based service, you should at least include some of the foundational calls here.

Here is an example of what that could look like, pulled from a project of my own:

<i>

The server provides the following REST endpoints: requests are routed to these endpoints in `server/src/app.ts`.

#### `/api/user`

| Endpoint     | Method | Description                           |
| ------------ | ------ | ------------------------------------- |
| `/list`      | POST   | Get details of a list of users        |
| `/login`     | POST   | Validate username/password entry      |
| `/signup`    | POST   | Create a new user                     |
| `/:username` | POST   | Update user's displayname or password |
| `/:username` | GET    | Get information about a user          |

#### `/api/friend`

| Method | Route                 | Purpose                                                            |
| ------ | --------------------- | ------------------------------------------------------------------ |
| POST   | `/request`            | Send a friend request (`{ auth, payload: {toUsername} }`)          |
| POST   | `/respond`            | Accept/reject a request (`{ auth, payload: {requestId, action} }`) |
| POST   | `/remove`             | Remove a friend (`{ auth, payload: {friendUsername} }`)            |
| GET    | `/list/:username`     | Get user's accepted friends list                                   |
| GET    | `/requests/:username` | Get pending incoming/outgoing requests                             |

</i>

#### Important function calls

Similarly to the API calls, if your service is operated through the user’s own terminal, you should list out some of the calls here. At minimum, you should lay out how to reach whatever is your software’s equivalent of a

```py
print("Hello, World!")
```

## Community/Contributions

By reading this, you’re currently contributing to this work, congrats! But you probably don’t want the worldwide community of programmers and devs to stop at reading your README. When telling other people they can contribute, a simple `Contributions are welcome!` is what you shouldn't say.

Instead, this is the place for you to outline a procedure such as:

```
1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
```

or to direct people towards

- Your repo’s Discussions tab (HYPERLINKED, OF COURSE)
- Creating Issues (another link) for discussing extended development

so that people can help contribute to the further development of this project, cause more features never hurt anybody (those definitely aren’t famous last words).

## License

For anyone to use your project, it has to have a license attached. Without one, nobody can legally use your repo, even if it is public. This is where you attach that info, and ideally [link](https://choosealicense.com/) (yes, another one) to the site outlining that license, or at least point them to the license file attached within your repo.

This project is distributed under the [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/) license. See [LICENSE](LICENSE.md) for more info.

## Acknowledgements

This is where you might list resources you found helpful and want, or need, to give credit to. In my case, these are some of the repos I found helpful as examples to synthesize this guide from:

#### Examples

- [Gyroflow|Gyroflow|Github](https://github.com/gyroflow/gyroflow)
- [Oven-sh|Bun|Github](https://github.com/oven-sh/bun)
- [RustDesk|RustDesk|Github](https://github.com/rustdesk/rustdesk)
- [ArgoSpenTech|Argos-Translate|Github](https://github.com/argosopentech/argos-translate)

#### Sources

- [[deleted]|How to Write a Readme|r/learnprogramming](https://www.reddit.com/r/learnprogramming/comments/vxfku6/how_to_write_a_readme/)
- [Akash|A Beginners Guide to writing a Kickass README|Medium](https://meakaakka.medium.com/a-beginners-guide-to-writing-a-kickass-readme-7ac01da88ab3)
- [Othneildrew|Best README Template|Github](https://github.com/othneildrew/Best-README-Template)
- [BaneSullivan|README|Github](https://github.com/banesullivan/README?tab=readme-ov-file)
