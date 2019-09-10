
`yarn test-with-just-mocha-opts` (runs just `mocha`) results in

```
/Users/ab/code/mocha-bug-require/test/foo.js:1
(function (exports, require, module, __filename, __dirname) { import util from 'util'
                                                                     ^^^^

SyntaxError: Unexpected identifier
…
```

even though `--require esm` is in `mocha.opts`.

But `yarn test-with-require-cl-arg` (`mocha --require esm`) works just fine.
