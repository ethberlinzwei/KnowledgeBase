# Remix

[Remix](https://remix.ethereum.org) is a powerful, open source tool that helps you write Solidity contracts straight in the browser. Written in JavaScript, Remix supports both usage in the browser and locally. Remix also supports testing, debugging and deploying of smart contracts and much more.

We recently published an update that provides a way to develop external plugin, and the purpose of this hackathon is to build plugins for Remix.

## Features

Remix is a suite of tools written in JavaScript used for developing smart contracts,
It contains the following packages you can find on [GitHub](https://github.com/ethereum/remix):

-   remix-lib
-   remix-debug (contract debugging)
-   remix-analysis (solidity static analysis)
-   remix-solidity (solidity compiler)
-   remix-tests (smart contract unit testing)
-   remix-ide (IDE - remix.ethereum.org)
-   remixd (accessing local files from remix IDE)

<!-- TODO: Needed anymore? -->

## General overview

Here we describe basic information about this event.

-   Each team should have at least one person present at the event.
-   Each team should choose a plugin from the plugin list. <https://github.com/ethberlin-hackathon/ETHBerlin-Teambuilding/issues?q=is%3Aissue+is%3Aopen+label%3A%22Remix-IDE+%3Adesktop_computer%3A%22>
-   Please come to us prior starting, it is better to have a clear overview of who is working on what.
-   Feel free to communicate and ask question in <https://gitter.im/ethereum/remix-dev-plugin> .
-   If the plugin is already taken by another team, you can still take it, but we really encourage you to work with the other team rather than competing with them.
-   You are still completely free to bring your own ideas. Please reach out and ask us if you want your idea to be funded.
-   At the end of the hackathon or shortly after, the evaluation team will select a maximum of 4 teams that will receive a sponsorship.
-   To evaluate your development, we need you to provide a document describing your work (see the "Document" section).
-   The ultimate plan is for us to continue working together. So please, keep in contact with us after event.

## Plugin list

<https://github.com/ethberlin-hackathon/ETHBerlin-Teambuilding/issues?q=is%3Aissue+is%3Aopen+label%3A%22Remix-IDE+%3Adesktop_computer%3A%22>

## Evaluation team

The evaluation team is composed of people from the EF. We are here for:

-   Helping you on technical matters and to find the right person to answer technical question.
-   Selecting the 4 teams that will receive sponsorship.
-   Validating funded plugins.
-   Advising you if you wish to be more involved in the Ethereum community.

We are:
@ligi, @holiman (Martin), @leonardoalt, @yann300, @iurimatias, @chfast (Pawel), @axic (Alex), @ryestew (Rob), @ninabreznik , @serapath (Alex)

## Document

This document should contains:

-   General description of the project.
-   Contact of involved people.
-   Github repository where the project is stored.
-   Description about how to make it work.
-   What is left to be done in order to be usable in production.
-   What were the main problems you encountered while developing and how did you solve them.
-   What should have been done differently -if that applies.
-   How would it be possible to extend contribution beyond the current project.

We really recommend to take time for that if you want to apply for a sponsorship.

<!-- TODO: Down to here -->

## Getting Started

Once you have chosen a theme/plugin you have interest in, take the following steps:

-   Join <https://gitter.im/ethereum/remix-dev-plugin>
-   Speak to us online or at the event
-   Post a message in [the bounty issue](#) saying that you are starting it with your name and the name of your team (super important!).
-   Feel free to speak to us if you have any Ethereum related questions
-   Close to the end of the hackathon, send us a document describing your work (see the previous section). We will use it for selecting max 4 team that will receive a development grant from the Ethereum Foundation.
-   After the event we'd like to keep in contact for further contributions and collaboration

## Set up your development environment

Read these guides to learn how to setup your local environment for developing a Remix plugin:

-   <https://github.com/ethereum/remix/blob/master/docs/remix_plugin.md>
-   <https://github.com/ethereum/remix/blob/master/docs/remix_plugin_api.md>

<!-- TODO: Is this still current? -->

### easy way: cloning the sample project and setting up the plugin

follow the README of <https://github.com/yann300/remix-plugin>

### manual setup: building the Remix API lib and setting up the plugin

git clone <https://github.com/ethereum/remix-ide>
npm install
cd src/app/plugin

npm install
npm run browserify
This will generate the file `bundle.js`. Reference this file in any html page to start using the API.

Once you have this `bundle.js` (or `require('remix-plugin')`)

Create a folder (not necessarily in Remix) where the plugin code should go.
copy `bundle.js` to it.
Go in `test-browser/plugin` from the remix-ide project and copy the file `index.html` and `plugin.js` to your working directory.
Serve this folder through a web server `http-server .`

Go in Remix / settings tab, under the `Plugin` section paste the following declaration:

{
    "title": "<name of plugin>",
    "url": "<http://127.0.0.1:><port>"
}

Then start the plugin by clicking on its icon.

<!-- TODO: Down to here -->

## Need Help?

For more help, several members of the team will be at the hackathon, or chat to us in <https://gitter.im/ethereum/remix-dev-plugin> ;)
