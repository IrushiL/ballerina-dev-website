---
layout: ballerina-left-nav-pages
title: Setting up Visual Studio Code
permalink: /learn/setting-up-visual-studio-code/
active: setting-up-visual-studio-code
redirect_from:
  - /v1-2/learn/tools-ides/vscode-plugin
  - /v1-2/learn/tools-ides/vscode-plugin/
  - /learn/tools-ides/vscode-plugin
  - /learn/tools-ides/vscode-plugin/
  - /v1-2/learn/vscode-plugin
  - /v1-2/learn/vscode-plugin/
  - /learn/vscode-plugin/
  - /learn/vscode-plugin
  - /learn/tools-ides/setting-up-visual-studio-code
  - /learn/tools-ides/setting-up-visual-studio-code/
  - /learn/setting-up-visual-studio-code
---

# Setting up Visual Studio Code 

The VS Code Ballerina extension provides the Ballerina development capabilities in VS Code. The below sections include instructions on how to download, install, and use the features of the VS Code extension.

- [Downloading VS Code](#downloading-vs-code)
- [Installing the extension](#installing-the-extension)
- [Using the extension](#using-the-extension)

## Downloading VS Code 

Download the [Visual Studio Code editor](https://code.visualstudio.com/download).


## Installing the extension

Use either of the below approaches to install the VS Code Ballerina extension.

- [Installing via the VS Code editor](#installing-via-the-vs-code-editor)
- [Installing by downloading the extension](#installing-by-downloading-the-extension)

### Installing via the VS Code editor

Click **Extensions** on the left-most menu of the editor, search for the Ballerina extension, and click **Install**.

> **Tip**: Click **Reload** to reload the editor to apply the change.

![Install the extension via VS Code](/learn/images/install-via-editor.gif)

This downloads the extension and installs it.

### Installing by downloading the extension

1. Download the [Visual Studio Code Ballerina Extension](https://marketplace.visualstudio.com/items?itemName=ballerina.ballerina).
2. Follow either of the below approaches to install the extension.
    - [Using the VS Code editor](#using-the-vs-code-editor)
    - [Using the Command Line](#using-the-command-line)

#### Using the VS Code editor

1. Click **View** in the top menu of the editor and click **Command Palette**.
2. In the search bar, type "vsix" and click **Extensions: Install from VSIX...**.
3. Browse and select the VSIX file of the extension you downloaded.

![Install using the Command Palette of the editor.](/learn/images/install-via-palette.gif)

#### Using the Command Line
In a new Command Line tab, execute the below command.
```bash
$ code --install-extension <BALLERINA-EXTENSION-DIRECTORY>
```
> **Tip**: In the above command, `<BALLERINA_EXTENSION-DIRECTORY>` refers to the path of the Ballerina extension directory (i.e., the VSIX file) you downloaded.

## Using the extension

> **Tip:** Ballerina Language Specification supports a set of experimental features such as transactions syntax. In order to be compatible with the experimental features and for supporting language intelligence in VS Code Extension, enable the Allow Experimental option in user settings.

> **Troubleshooting**: If you installed a new Ballerina version recently, you might need to restart the VS Code Editor to pick the new Ballerina version. Herein, If you are using Mac OS, press 'Command+Q' keys to quit the app and reopen it.

The below sections include information on the various capabilities that are facilitated by the VS Code Ballerina Extension for the development process.

- [Language Intelligence](/learn/vscode-plugin/language-intelligence)
- [Run and Debug](/learn/vscode-plugin/run-and-debug)
- [Graphical View](/learn/vscode-plugin/graphical-editor)
- [Documentation Viewer](/learn/vscode-plugin/documentation-viewer)
- [Run All Tests](/learn/vscode-plugin/run-all-tests)

