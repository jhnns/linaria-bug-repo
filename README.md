# README

This repo demonstrates a linaria/babel bug. When running `npm run build`, it will throw:

```
Module build failed (from ./node_modules/babel-loader/lib/index.js):
SyntaxError: /Users/jhnns/dev/jhnns/linaria-bug-repo/src/main.js: /Users/jhnns/dev/jhnns/linaria-bug-repo/src/mobx.js: Exporting local "b", which is not declared.
  7 | }
  8 |
> 9 | export { a, b };
    |             ^
    at File.buildCodeFrameError (/Users/jhnns/dev/jhnns/linaria-bug-repo/node_modules/@babel/core/lib/transformation/file/file.js:249:12)
    at NodePath.buildCodeFrameError (/Users/jhnns/dev/jhnns/linaria-bug-repo/node_modules/@babel/traverse/lib/path/index.js:145:21)
    at getLocalMetadata (/Users/jhnns/dev/jhnns/linaria-bug-repo/node_modules/@babel/helper-module-transforms/lib/normalize-and-load-metadata.js:318:22)
    at /Users/jhnns/dev/jhnns/linaria-bug-repo/node_modules/@babel/helper-module-transforms/lib/normalize-and-load-metadata.js:347:33
    at Array.forEach (<anonymous>)
    at /Users/jhnns/dev/jhnns/linaria-bug-repo/node_modules/@babel/helper-module-transforms/lib/normalize-and-load-metadata.js:344:33
    at Array.forEach (<anonymous>)
    at getLocalExportMetadata (/Users/jhnns/dev/jhnns/linaria-bug-repo/node_modules/@babel/helper-module-transforms/lib/normalize-and-load-metadata.js:331:27)
    at getModuleMetadata (/Users/jhnns/dev/jhnns/linaria-bug-repo/node_modules/@babel/helper-module-transforms/lib/normalize-and-load-metadata.js:122:21)
    at normalizeModuleAndLoadMetadata (/Users/jhnns/dev/jhnns/linaria-bug-repo/node_modules/@babel/helper-module-transforms/lib/normalize-and-load-metadata.js:58:7)
```

## Steps to reproduce

- `npm i`
- `npm run build`