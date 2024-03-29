# Electron React Webpack Typescript (Custom Titlebar)

A prebuilt project for creating desktop apps using Electron, React, Webpack & Typescript with hot-reload, easy to use custom import aliases & executable builds for distribution.

<br>
<img src="assets/images/anim_v8.gif" />
<br>

Special thanks to [@guasam](https://github.com/guasam) for development of Custom Window, Titlebar, UI/UX etc.

<br>

## Core Features

- 🌟 Electron
- 🌀 TypeScript
- ⚛️ React
- 🥗 SASS/SCSS Loader
- 🎨 CSS Loader
- 📸 Image Loader
- 🆎 Font Loader
- 🧹 ESLint
- 📦 Electron Forge
- 📐 Custom Window Frame
- 📐 Custom Window Titlebar
- 📐 Custom Window Menubar
- 🔱 Webpack & Configuration
- 🧩 Aliases for Project Paths
- 🗡️ Native (node) Modules Support
- 🔥 React Fast Refresh + Webpack HMR
- 🌞 Dark Mode + Light Mode (Theme)
- 🎁 Package Bundling (Distribution / Release)

<br>

## Custom Electron Window Titlebar & Menus

This project includes [electron-window](https://github.com/guasam/electron-window) as core of custom window components and modules.

**Following are the list of features it provides :**

- Custom Titlebar for Electron Window.
- Easily changable platform specific controls for max/min/close buttons using `windows` or `mac` value for `platform` property with `<WindowFrame>` in renderer.
- Titlebar menus can show/hide by pressing `alt` or `option` key.
- Window frame `title` prop displays in titlebar center when menus are toggeled off.
- Menu entries can be customized in `src/main/window/titlebarMenus.ts` file.
- Menu items and windows controls UI or colors can be customized easily by modifying the `src/renderer/window` components & styles.

<br>

### Custom Aliases for Paths

We can use predefined aliases for `import` paths already used in this project. Following are the details:

| Alias         | Target Path                |
| ------------- | -------------------------- |
| `@assets`     | `/assets`                  |
| `@main`       | `/src/main`                |
| `@renderer`   | `/src/renderer`            |
| `@common`     | `/src/common`              |
| `@src`        | `/src`                     |
| `@styles`     | `/src/renderer/styles`     |
| `@components` | `/src/renderer/components` |


<br>

### Want to use Vite instead of Webpack bundler?

Introducing the [ElectroVite](https://github.com/guasam/electrovite-react) project with a brief description below.

<br>

## Installation

![status](https://img.shields.io/badge/ERWT-Main%20Version-blue.svg)

Main version of this project contains files structure in separate context for `main` and `renderer`, with custom electron window, titlebar etc.

```bash
git clone https://github.com/codesbiome/electron-react-webpack-typescript-2024
```

<br>
<div align="center">
    <b>OR</b>
</div>
<br>

![status](https://img.shields.io/badge/ERWT-Minimal%20Version-0a922a.svg)

Minimal version of ERWT contains very simple project files structure, no custom window, no custom titlebar & menus.

```bash
git clone -b minimal https://github.com/codesbiome/electron-react-webpack-typescript-2024
```

<br>

Install dependencies using [pnpm](https://pnpm.io/) or [yarn](https://www.npmjs.com/package/yarn) or [npm](https://www.npmjs.com/) :

```bash
# using pnpm
pnpm install

# or using yarn
yarn install

# or using npm
npm install
```

<br />

## Start : Development

To develop and run your application, you need to run following command.
<br />
Start electron application for development :

```bash
yarn start
```

<br />

## Lint : Development

To lint application source code using ESLint via this command :

```bash
yarn lint
```

<br />

## Package : Production

Customize and package your Electron app with OS-specific bundles (.app, .exe etc)

```bash
yarn package
```

<br />

## Make : Production

Making is a way of taking your packaged application and making platform specific distributables like DMG, EXE, or Flatpak files (amongst others).

```bash
yarn make
```

<br />

## Publish : Production

Publishing is a way of taking the artifacts generated by the `make` command and sending them to a service somewhere for you to distribute or use as updates. (This could be your update server or an S3 bucket)

```bash
yarn publish
```

<br />

## Packager & Makers Configuration

This provides an easy way of configuring your packaged application and making platform specific distributables like DMG, EXE, or Flatpak files.

This configurations file is available in :

```bash
tools/forge/forge.config.js
```

For further information, you can visit [Electron Forge Configuration](https://www.electronforge.io/configuration)
