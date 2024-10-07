
# Node.js Tutorial for Students

## Table of Contents
- [Introduction to Node.js](#introduction-to-nodejs)
- [Installation](#installation)
  - [Step 1: Install Node.js and npm](#step-1-install-nodejs-and-npm)
  - [Step 2: Verify Installation](#step-2-verify-installation)
- [Setting Up Your First Node.js Project](#setting-up-your-first-nodejs-project)
  - [Creating a Project Directory](#creating-a-project-directory)
  - [Initializing the Project](#initializing-the-project)
  - [Creating a Simple Server](#creating-a-simple-server)
- [Conclusion](#conclusion)

## Introduction to Node.js
Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine. It allows developers to use JavaScript to write server-side code and build scalable network applications. Node.js is known for its event-driven, non-blocking I/O model, which makes it lightweight and efficient.

## Installation

### Step 1: Install Node.js and npm
Node.js relies on npm (Node Package Manager) to manage dependencies and packages.

1. **Download and Install Node.js:**
   - Visit [https://nodejs.org/](https://nodejs.org/).
   - Download and install the LTS (Long-Term Support) version of Node.js, which comes with npm.

### Step 2: Verify Installation
1. Open a terminal or command prompt.
2. Run the following commands to check if Node.js and npm are installed correctly:
   ```bash
   node -v
   npm -v
   ```
   You should see version numbers for both commands, indicating that Node.js and npm are successfully installed.

## Setting Up Your First Node.js Project

### Creating a Project Directory
1. Open a terminal and create a new directory for your project:
   ```bash
   mkdir my-first-node-app
   cd my-first-node-app
   ```

### Initializing the Project
1. Initialize a new Node.js project by running:
   ```bash
   npm init -y
   ```
   This command creates a `package.json` file with default settings.

### Creating a Simple Server
1. Create a new file called `server.js`:
   ```bash
   touch server.js
   ```
2. Open `server.js` in your favorite text editor and add the following code:
   ```javascript
   const http = require('http');

   const hostname = '127.0.0.1';
   const port = 3000;

   const server = http.createServer((req, res) => {
     res.statusCode = 200;
     res.setHeader('Content-Type', 'text/plain');
     res.end('Hello, World!
');
   });

   server.listen(port, hostname, () => {
     console.log(`Server running at http://${hostname}:${port}/`);
   });
   ```
3. Save the file and run the server:
   ```bash
   node server.js
   ```
4. Open your browser and navigate to `http://127.0.0.1:3000/`. You should see "Hello, World!" displayed in your browser.

## Conclusion
You have successfully installed Node.js, set up a basic project, and created a simple server that responds with "Hello, World!" This is just the beginning of what you can achieve with Node.js. As you continue to explore, you'll discover the power of building server-side applications using JavaScript.

Happy coding!
