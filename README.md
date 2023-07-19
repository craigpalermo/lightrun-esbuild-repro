# Lightrun ESBuild Bug Repro

Problem: Importing Lightrun in a Typescript app built with ESBuild causes execution to hang once it reaches the import.

## Setup

Run `npm i`.

## Steps to reproduce

Run `npm run build:tsc` to build with Typescript as a control.

Then, start the built app by running `node index.js`. You should see output similar to:

```
The app is executing now
Lightrun start fn: [Function: start]
```

Now, run `npm run build:esbuild` to build with ESBuild.

Run the app again (`node index.js`), and you'll notice there is no output and the process does not terminate.