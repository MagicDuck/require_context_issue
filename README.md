# Reproduction Steps
1. npm install
2. npm run start
3. open and edit ./src/beer.js
You  will see something like the following:
```
webpack: Compiling...
Hash: e3f58778c3d5e09acb1e
Version: webpack 3.10.0
Time: 40ms
    Asset    Size  Chunks                    Chunk Names
bundle.js  325 kB       0  [emitted]  [big]  main
  [21] (webpack)/hot nonrecursive ^\.\/log$ 170 bytes {0} [built]
  [26] ./src/widgets Widget[.]js$ 198 bytes {0} [built]
  [27] ./src/widgets/BarWidget.js 44 bytes {0} [optional] [built]
  [28] ./src/widgets/FooWidget.js 44 bytes {0} [optional] [built]
  [30] ./src/beer.js 53 bytes {0} [built]
    + 26 hidden modules
webpack: Compiled successfully.
```
Even though we only changed `./src/beer.js` it rebuilt all the stuff grabbed by `require.context()` call in `./src/theWidgets.js`
