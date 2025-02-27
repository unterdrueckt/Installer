<h1 align="center">BetterDiscord Installer</h1>

<p align="center">
  <a href="#overview">Overview</a> |
  <a href="#development">Development</a> |
  <a href="#contributors">Contributors</a>
</p>

<p align="center">
  <img alt="Preview" width="524" alt="Hero image" src="https://i.imgur.com/evmFCAf.png"/>
  <br/>
  A simple standalone program which automates the installation, removal and maintenance of <a href="https://github.com/BetterDiscord/BetterDiscord">BetterDiscord</a>.
</p>

---

# Overview

This repository contains the source code for the BetterDiscord installer. This installer is written with [electron-webpack](https://webpack.electron.build/) and [Svelte 3](https://svelte.dev/).

## Auto-Install Feature

This fork adds a new command-line argument:

- **`-autoinstall`** → Automatically installs BetterDiscord on the detected platform without user interaction.

### Usage:
To trigger an automatic installation, run:

```sh
BetterDiscord-Installer.exe -autoinstall
```

## Downloads

These will link you to the latest builds found in the [releases](https://github.com/BetterDiscord/installer/releases/) tab of this repository.

| [Windows (7+)](https://github.com/BetterDiscord/Installer/releases/latest/download/BetterDiscord-Windows.exe)  | [macOS (10.10+)](https://github.com/BetterDiscord/Installer/releases/latest/download/BetterDiscord-Mac.zip) | [Linux](https://github.com/BetterDiscord/Installer/releases/latest/download/BetterDiscord-Linux.AppImage) |
| ------------- | ------------- | ------------- |



## Codebase

```
.
├──assets                  // Contains static assets (such as images) used by the installer.
|  └──images               // Images (logos, backgrounds, etc...) used by the installer.
├──scripts                 // Scripts needed for development and contributing.
└──src                     // The installer's source code.
    ├──main                // Electron "main" process. Creates and configures the BrowserWindow.
    └──renderer            // Electron "renderer" process. Contains most components and scripts.
        ├──actions         // Scripts performed by the installer such as installing, repairing and uninstalling.
        |  └──utils        // Common utilities used by installer actions (such as killing discord).
        ├──common          // Common UI components such as buttons, checkboxes, radios, etc...
        ├──pages           // Component files for each page in the installer's setup process.
        ├──stores          // Svelte store used for storing global data.
        |  └──types        // Used for defining custom svelte stores.
        └──transitions     // Contains custom Svelte transitions and animations.
```

---

# Development

> This is a tutorial designed for people looking to contribute to, or work directly with the installer's source code. If you are just looking to download and install BetterDiscord, visit the [releases](https://github.com/BetterDiscord/installer/releases/) page of this repository.

## Prerequisites
- [Git](https://git-scm.com)
- [Node.js](https://nodejs.org/en/)
- [yarn](https://yarnpkg.com)
- Command line of your choice.

## Building

### 1: Clone the repository.
```ps
git clone https://github.com/BetterDiscord/installer && cd installer
```
This will create a local copy of this repository and navigate you to the root folder of the repository.

### 2: Install Dependencies
Run this command at the root folder to install dependencies:
```ps
yarn install
```

### 3: Run Build Script
To run the installer in development mode, simply run the following command:
```ps
yarn dev
```

## Additional Scripts

### Linting
This project uses [ESLint](https://eslint.org/). Run this command to lint your changes:
```ps
yarn lint
```

### Compiling & Distribution

```ps
yarn dist
```

---

# Contributors

For information on contributing to this project, please see [CONTRIBUTING.md](/CONTRIBUTING.md).

<a href="https://github.com/betterdiscord/installer/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=betterdiscord/installer" />
</a>
