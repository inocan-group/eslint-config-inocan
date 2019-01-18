# Inocan Group's `eslint` Config

This is a simple and reusable configuration for **eslint** which should be used on all
Inocan Group projects (and of course everyone else is welcome to use as well). It
originates from the defaults that are now emitted as part of the Vue CLI 3.x tool when
configured for Typescript projects. We use this for both front and backend projects.

## Peer Dependencies

You should install the following peer dependencies in your project along side this repo:

- eslint
- [eslint-plugin-vue](https://github.com/vuejs/eslint-plugin-vue)
- [typescript-eslint-parser](https://github.com/typescript-eslint/typescript-eslint)

> **Note:** if you're using the Vue CLI and have chosen Typescript then these will be
> already included. If not then you'll want to add them manually.

## Logging

You may note the strong rules around using `console.xxx` (aka, warn in non-prod, error in
prod) but that's because we're a firm believer that all logging should use a _logging
framework_ and on Inocan Projects we use:

- [aws-log](https://github.com/inocan-group/aws-log) - for backend Typescript (in
  particular Lambda functions)
- [browser-log](https://github.com/inocan-group/browser-log) - for logging in the browser

If you need to make an exception then you'll need to put in the eslint directive:

```javascript
/* eslint no-console: "off" */
```

or just deal with the warning message if you're in development.

## License

Copyright (c) 2019 Inocan Group

Permission is hereby granted, free of charge, to any person obtaining a copy of this
software and associated documentation files (the "Software"), to deal in the Software
without restriction, including without limitation the rights to use, copy, modify, merge,
publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons
to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or
substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,
INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR
PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE
FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
DEALINGS IN THE SOFTWARE.
