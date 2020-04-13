This repo demonstrates a bug in `next build` for serverless pages including Firestore.

1. Clone this repo
2. `npm install`
3. `npm run build`

Result:

```
➜ npm run build

> next-fb@1.0.0 build /Users/westont/Downloads/tmp/next-fb
> next build

Creating an optimized production build  

Compiled with warnings.

./node_modules/next/dist/next-server/server/load-components.js
Critical dependency: the request of a dependency is an expression

./node_modules/next/dist/next-server/server/load-components.js
Critical dependency: the request of a dependency is an expression

./node_modules/next/dist/next-server/server/load-components.js
Critical dependency: the request of a dependency is an expression

./node_modules/next/dist/next-server/server/load-components.js
Critical dependency: the request of a dependency is an expression

./node_modules/next/dist/next-server/server/require.js
Critical dependency: the request of a dependency is an expression

./node_modules/next/dist/next-server/server/require.js
Critical dependency: the request of a dependency is an expression


> Build error occurred
Error: ENOENT: no such file or directory, open 'google/protobuf/api.proto'
    at Object.openSync (fs.js:440:3)
    at Object.readFileSync (fs.js:342:35)
    at fetch (/Users/westont/Downloads/tmp/next-fb/.next/serverless/pages/index.js:3523:34)
    at Root.load (/Users/westont/Downloads/tmp/next-fb/.next/serverless/pages/index.js:3557:13)
    at Root.loadSync (/Users/westont/Downloads/tmp/next-fb/.next/serverless/pages/index.js:3598:17)
    at Object.loadSync (/Users/westont/Downloads/tmp/next-fb/.next/serverless/pages/index.js:28213:17)
    at Object.8ZNE (/Users/westont/Downloads/tmp/next-fb/.next/serverless/pages/index.js:4141:37)
    at __webpack_require__ (/Users/westont/Downloads/tmp/next-fb/.next/serverless/pages/index.js:23:31)
    at Object.<anonymous> (/Users/westont/Downloads/tmp/next-fb/.next/serverless/pages/index.js:5513:19)
    at Object.BYZf (/Users/westont/Downloads/tmp/next-fb/.next/serverless/pages/index.js:28111:30) {
  errno: -2,
  syscall: 'open',
  code: 'ENOENT',
  path: 'google/protobuf/api.proto'
}
```