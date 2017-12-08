# Reproduction Steps
1. npm install
2. npm run start
3. open and edit ./src/beer.js
You  will see something like the following:
```
webpack: Compiling...
Hash: ea42064a3fb08ff14046
Version: webpack 3.10.0
Time: 38ms
    Asset    Size  Chunks                    Chunk Names
bundle.js  325 kB       0  [emitted]  [big]  main
  [21] (webpack)/hot nonrecursive ^\.\/log$ 170 bytes {0} [built]
  [26] ./src/beer.js 62 bytes {0} [built]
  [28] ./src/widgets Widget[.]js$ 198 bytes {0} [built]
    + 28 hidden modules
webpack: Compiled successfully.
```
Even though we only changed `./src/beer.js` it rebuilt all the stuff grabbed by `require.context()` call in `./src/theWidgets.js`
