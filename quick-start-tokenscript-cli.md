---
description: Learn to create a TokenScript project in minutes with CLI.
---

# Quick Start TokenScript CLI

In this tutorial you will:

1. Quickstart tokenscript project
2. Build a project
3. Test (emulate) a project
4. TokenScript project lifecycle

## Prerequisites <a href="#prerequisites" id="prerequisites"></a>

Before starting this tutorial you must:

1. Install Node.js
2. Install Python
3. Install TokenScript CLI

## Quickstart a tokenscript Project

### Commands

Run these commands to create a TokenScript project for USDC (ERC-20) token. The next section provides the explanations for each command.

<pre><code>// Create a tokenscript project for USDC token
> mkdir quickstart
> cd quickstart

<strong>> tokenscript create
</strong>? Select project template Empty Project: An empty TokenScript project
? Enter a name for the TokenScript project: USDC
? Select the token type: erc20
? Enter the ethereum contract address for the TokenScript: 0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48
? Enter the ethereum chainID for the TokenScript: 1
? Enter a short description for the TokenScript: USDC
? Enter a URL to a website about this TokenScript: https://etherscan.io/token/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48
? Enter an icon URL for the TokenScript (base64 image URLs are supported): https://etherscan.io/token/images/centre-usdc_28.png
Initializing template...... done
Project successfully initialized!

> tokenscript build
Processing ./styles.css
Processing ./index.html
Processing ./mint.html
Validate TSML...... done

TokenScript build completed successfully!

> tokenscript emulate
Starting emulator...
Build started..
⚡️[server]: Server is running at https://localhost:8090
</code></pre>

### Explanation of commands

Create the project home directory.

```
> mkdir quickstart
```

Change to the project directory.

```
> cd quickstart
```

#### Create the tokenscript project

In this step, you need to prepare following informations:

* Project name - your project name.
* Token type - erc20, erc721, erc1155.
* Smart contract address for your token - the smart contract address, you have to know it, or inquiry the address from [https://etherscan.io/](https://etherscan.io/)
* chainID - the ethereum chainID. Find chainID by [https://chainlist.org/](https://chainlist.org/)
* Short description.
* A URL for your tokenscript website.
* An icon URL for your tokenscript.

```
> tokenscript create
? Select project template Empty Project: An empty TokenScript project
? Enter a name for the TokenScript project: USDC
? Select the token type: erc20
? Enter the ethereum contract address for the TokenScript: 0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48
? Enter the ethereum chainID for the TokenScript: 1
? Enter a short description for the TokenScript: USDC
? Enter a URL to a website about this TokenScript: https://etherscan.io/token/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48
? Enter an icon URL for the TokenScript (base64 image URLs are supported): https://etherscan.io/token/images/centre-usdc_28.png
Initializing template...... done
Project successfully initialized!
```

Build the tokenscript project.

```
> tokenscript build
```

Emulate the tokenscript project.

```
> tokenscript emulate
```

## Build a project

Once created a TokenScript project, you can update the project files like .html or tokenscript.xml. After all is done, you can build the project into one single file (tokenscript.tsml).

```
> tokenscript build
Processing ./styles.css
Processing ./index.html
Processing ./mint.html
Validate TSML...... done
```

## Test a project

After build, in order to verify the tokenscript project, you can emulate the project as following:

```
> tokenscript emulate
Starting emulator...
Build started..
⚡️[server]: Server is running at https://localhost:8090
```

It will pop up a browser tab automatically, if not you can visit [http://localhost:8090/?emulator](http://localhost:8090/?emulator)

## TokenScript project lifecycle

A classic tokenscript project lifecycle is as following:

1. Firstly, you need to create a project. Refer to [#create-the-tokenscript-project](quick-start-tokenscript-cli.md#create-the-tokenscript-project "mention")
2. Second, build the project. Refer to [#build-a-project](quick-start-tokenscript-cli.md#build-a-project "mention")
3. Third, you can see the demo by emulate the project. Refer to [#test-a-project](quick-start-tokenscript-cli.md#test-a-project "mention")
4. Fourth, optional, sign the tokenscript.tsml file with command `tokenscript sign`.
