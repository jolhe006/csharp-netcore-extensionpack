# Welcome to your VS Code Extension Pack

## What's in the folder

* This folder contains all of the files necessary for your extension pack.
* `package.json` - this is the manifest file that defines the list of extensions of the extension pack.

## Get up and running straight away

* Press `F5` to open a new window with your extension loaded.
* Open `Extensions Viewlet` and check your extensions are installed.

## Make changes

* You can relaunch the extension from the debug toolbar after making changes to the files listed above.
* You can also reload (`Ctrl+R` or `Cmd+R` on Mac) the VS Code window with your extension to load your changes.

## Install your extension

* To start using your extension with Visual Studio Code copy it into the `<user home>/.vscode/extensions` folder and restart Code.
* To share your extension with the world, read on https://code.visualstudio.com/docs about publishing an extension.



## Publishing Extensions
Once you have made a high-quality extension, you can publish it to the VS Code Extension Marketplace so others can find, download, and use your extension. Alternatively, you can package an extension into the installable VSIX format and share it with other users.

##  vsce

[vsce](https://github.com/microsoft/vscode-vsce), short for "Visual Studio Code Extensions", is a command-line tool for packaging, publishing and managing VS Code extensions.

### Installation

Make sure you have [Node.js](https://nodejs.org/) installed. Then run:

```bash
npm install -g @vscode/vsce
```

### Usage

You can use `vsce` to easily [package](#packaging-extensions) and [publish](#publishing-extensions) your extensions:

```bash
$ cd myExtension
$ vsce package
# myExtension.vsix generated
$ vsce publish
# <publisher id>.myExtension published to VS Code Marketplace
```

`vsce` can also search, retrieve metadata, and unpublish extensions. For a reference on all the available `vsce` commands, run `vsce --help`.

##  Publishing extensions
---

> [!NOTE]
> Due to security concerns, `vsce` will not publish extensions that contain user-provided SVG images.

The publishing tool checks the following constraints:

- The icon provided in `package.json` may not be an SVG.
- The badges provided in the `package.json` may not be SVGs unless they are from [trusted badge providers](/api/references/extension-manifest#approved-badges).
- Image URLs in `README.md` and `CHANGELOG.md` need to resolve to `https` URLs.
- Images in `README.md` and `CHANGELOG.md` may not be SVGs unless they are from [trusted badge providers](/api/references/extension-manifest#approved-badges).
---