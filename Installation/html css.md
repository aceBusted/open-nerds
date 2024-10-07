# Running HTML and CSS in Visual Studio Code

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installing Visual Studio Code](#installing-visual-studio-code)
- [Creating a New Project](#creating-a-new-project)
- [Writing HTML and CSS](#writing-html-and-css)
- [Running Your HTML and CSS Files](#running-your-html-and-css-files)
- [Conclusion](#conclusion)

## Introduction
Visual Studio Code (VS Code) is a popular code editor that provides an excellent environment for developing web applications. In this guide, you'll learn how to set up and run HTML and CSS files using VS Code.

## Prerequisites
Before you begin, ensure you have the following:
- A computer running Windows, macOS, or Linux.
- [Visual Studio Code](https://code.visualstudio.com/) installed.

## Installing Visual Studio Code
If you haven't installed VS Code yet, follow these steps:
1. Go to the [Visual Studio Code download page](https://code.visualstudio.com/).
2. Download the installer for your operating system (Windows, macOS, or Linux).
3. Run the installer and follow the prompts to complete the installation.

## Creating a New Project
1. Open Visual Studio Code.
2. Create a new folder for your project:
   - Click on **File** > **Open Folder...** (or **Open...** on macOS).
   - Create a new folder named `my-web-project` and select it.

3. Inside the folder, create two new files:
   - `index.html`
   - `styles.css`

## Writing HTML and CSS
### `index.html`
Open the `index.html` file and add the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>My Web Project</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is my first web project using HTML and CSS.</p>
</body>
</html>
```
