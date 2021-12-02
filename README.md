# Angular13StorybookTest

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.0.3.

# Issue

## Steps to reproduce

- `ng new <project-name>`
- `ng g library <library-name>`
- Add some style definitions in the library
- Add includePath in stylePreprocessorOptions in angular.json
- Add a custom component/module (in this case button), which consumes styles from style-lib
- run `npx sb init`
- Include style library in webpack.config or webpackFinal in main.js
- Add a story for the previously created button

## What I expect
- `npm run storybook` does work

## What I get
```
SassError: expected "{".
  ╷
1 │ var api = require("!../../../node_modules/style-loader/dist/runtime/injectStylesIntoStyleTag.js");
  │                                                                                                  ^
  ╵
  src\app\button\button.component.scss 1:98  root stylesheet
    at processResult (C:\Users\XXX\Documents\code\angular13-storybook-test\node_modules\webpack\lib\NormalModule.js:751:19)
    at C:\Users\XXX\Documents\code\angular13-storybook-test\node_modules\webpack\lib\NormalModule.js:853:5
    at C:\Users\XXX\Documents\code\angular13-storybook-test\node_modules\loader-runner\lib\LoaderRunner.js:399:11
    at C:\Users\XXX\Documents\code\angular13-storybook-test\node_modules\loader-runner\lib\LoaderRunner.js:251:18
    at context.callback (C:\Users\XXX\Documents\code\angular13-storybook-test\node_modules\loader-runner\lib\LoaderRunner.js:124:13)
    at Object.callback (C:\Users\XXX\Documents\code\angular13-storybook-test\node_modules\sass-loader\dist\index.js:54:7)
    at Worker.<anonymous> (C:\Users\XXX\Documents\code\angular13-storybook-test\node_modules\@angular-devkit\build-angular\src\sass\sass-service.js:123:25)
    at Worker.emit (events.js:375:28)
    at MessagePort.<anonymous> (internal/worker.js:216:53)
    at MessagePort.[nodejs.internal.kHybridDispatch] (internal/event_target.js:399:24)
    at MessagePort.exports.emitMessage (internal/per_context/messageport.js:18:26)
SassError: SassError: expected "{".
  ╷
1 │ var api = require("!../../../node_modules/style-loader/dist/runtime/injectStylesIntoStyleTag.js");
  │                                                                                                  ^
  ╵
  src\app\button\button.component.scss 1:98  root stylesheet
    at Object.callback (C:\Users\XXX\Documents\code\angular13-storybook-test\node_modules\sass-loader\dist\index.js:54:16)
    at Worker.<anonymous> (C:\Users\XXX\Documents\code\angular13-storybook-test\node_modules\@angular-devkit\build-angular\src\sass\sass-service.js:123:25)
    at Worker.emit (events.js:375:28)
    at MessagePort.<anonymous> (internal/worker.js:216:53)
    at MessagePort.[nodejs.internal.kHybridDispatch] (internal/event_target.js:399:24)
    at MessagePort.exports.emitMessage (internal/per_context/messageport.js:18:26)
```
