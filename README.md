# How to: Write a README

QuotBlock [A software engineer’s guide to writing like a human person]
\*\*iconstack here

## Table of Contents

<details open> 
<summary>A ToC can be optional based on ReadMe length</summary>

- Overview
- Highlights
- Usage
  - Getting Started
    - Prereqs
    - Installation
    - Configuration
  - Project Structure
  - API
  - Important function calls?
- Community/Contributing
- Citations
- License
</details>

## Overview

QuotBlock [What is a readme, and why does it matter?]

When creating any new piece of client-centered software, one of the first things that any good developer should do is to start writing a README document to go along with all the changes they make. A readme is a markdown (text) document that outlines all the critical information relevant to a software project. It’s the first (and only thing) a user or contributor will see before investing time into installing the software, so it will give a strong impression of what they can expect from the rest of your project or codebase.

Most READMEs, or any good one at least, include a brief overview section with a paragraph or two explaining how the software works, what it does, why it was made (sometimes)/the problem it hopes to solve, and (sometimes) who made it.

## Highlights

A highlights section is a good practice to include at the top of a README. It can provide a quick overview of the things that make your software unique, often presented as a short, bulleted list.

Some main takeaways of this guide:

- Should be inviting and approachable
- Identify and sell the most unique part of your software
- Concise is key; longer = more daunting
- Link everything, everywhere (documentation, deployments, etc.)
- Don’t be afraid to use Emojis or icons. Visuals = 1000 words.

## Usage

### Getting Started

Here is where you outline everything necessary for the user or contributor to install, set up, and run your project, including any prerequisites that need to be installed. Here, examples and blocks of code are king over trying to explain in words

#### Prerequisites

Before install of abc (your program), make sure that xyz is installed.
`bash npm install -g xyz	# OR whatever the install command is`
`bash npm install -g efg	# A second dependency you rely on`

#### Installation

Your software supports [insert OS’s supported].
Quotblock: [Linux x64? Linux arm64? macOs x64 and/or Apple Silicon? Windows x64 and/or arm64?]

```
# with install script (access web from terminal) (typically the recommended way if available)
curl - fsSL https://yourSite.com/install | bash
```
