# brankica - A NodeJS/TypeScript (node-ts) demo project to experiment with multipart mixed PDF uploading
The project is to experiment how the multipart/form-data and multipart/mixed HTTP post bodies are to be handled and used.

[Busboy](https://www.npmjs.com/package/busboy) cannot handle multipart/mixed content, unfortunately, only multipart/form-data.
In this new version multipart/form-data is used.

The [How to process POST data in Node.js?](https://stackoverflow.com/questions/4295782/how-to-process-post-data-in-node-js),
[CURL manual for -F parameter](https://curl.se/docs/manpage.html),
[How to read POST data?](https://nodejs.org/en/knowledge/HTTP/servers/how-to-read-POST-data/),
[Node JS Streams, Pipes and Events](https://www.guru99.com/node-js-streams-filestream-pipes.html)
are excellent sources of information.

## How this project was created
- First I created a repository in Github with gitignore, readme and license.
- I cloned this repo into a local folder with Visual Studio Code
- Opened a terminal and run command **npm init** (main (entry point) set to build/index.js), which creted package.json
- Then add runtime packages
    - npm install express busboy
- Add **development dependencies** of TypeScript, node-ts and types definitions for node and all other runtime packages
    - npm install typescript ts-node nodemon npm-run-all @types/node @types/express @types/busboy --save-dev
- Configure TypeScript with **npx tsc --init** which creates a created a **tsconfig.json** file with no questions.
    - "outDir": "./build",
    - "rootDir": "./src", // Create all TS files into this folder
- Add scritps to package.json
    - "start": "node .",
    - "dev": "nodemon ./src/index.ts",
    - "build": "tsc -p .",
- To run the application with node-ts **npm run dev**
 


