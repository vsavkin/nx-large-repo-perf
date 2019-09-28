# A Project for Scalability Testing

It's often useful to be able to generate a large workspace to test the scalability of our tooling.

This repo contains a script that generates such workspace.

Simply run:

```
node ./tools/scripts/generate-project.js
```

It will generate one app importing 10 libs, each of which importing other 10 libs, each of which has 10 components.

1 app: 
  -     10 * (1 + 10) = 110 libs   
  - 1 + 10 * (1 + 10 * (1 + 10)) = 1111 components

You can change the parameters. Open `generate-project.ts` and modify the parameters as you wish: 

```
const INIT_APP_INDEX = 0;
const NUMBER_OF_APPS = 1;
const NUMBER_OF_LIBS = 10;
const NUMBER_OF_CHILD_LIBS = 10;
const NUMBER_OF_COMPONENTS = 10;
```
