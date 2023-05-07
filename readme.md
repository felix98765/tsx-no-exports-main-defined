```
npm install
npm start
```

throws:
```
node:internal/errors:490
    ErrorCaptureStackTrace(err);
    ^

Error [ERR_PACKAGE_PATH_NOT_EXPORTED]: No "exports" main defined in /tsx-no-exports-main-defined/node_modules/@auth/core/package.json
    at __node_internal_captureLargerStackTrace (node:internal/errors:490:5)
    at new NodeError (node:internal/errors:399:5)
    at exportsNotFound (node:internal/modules/esm/resolve:261:10)
    at packageExportsResolve (node:internal/modules/esm/resolve:535:13)
    at resolveExports (node:internal/modules/cjs/loader:569:36)
    at Module._findPath (node:internal/modules/cjs/loader:643:31)
    at Module._resolveFilename (node:internal/modules/cjs/loader:1068:27)
    at u.default._resolveFilename (/tsx-no-exports-main-defined/node_modules/@esbuild-kit/cjs-loader/dist/index.js:1:1519)
    at Module._load (node:internal/modules/cjs/loader:928:27)
    at Module.require (node:internal/modules/cjs/loader:1149:19)
    at require (node:internal/modules/helpers:121:18)
    at <anonymous> (/tsx-no-exports-main-defined/index.ts:1:22)
    at Object.<anonymous> (/tsx-no-exports-main-defined/index.ts:4:25)
    at Module._compile (node:internal/modules/cjs/loader:1267:14)
    at Object.F (/tsx-no-exports-main-defined/node_modules/@esbuild-kit/cjs-loader/dist/index.js:1:941)
    at Module.load (node:internal/modules/cjs/loader:1125:32)
    at Module._load (node:internal/modules/cjs/loader:965:12)
    at ModuleWrap.<anonymous> (node:internal/modules/esm/translators:165:29)
    at ModuleJob.run (node:internal/modules/esm/module_job:192:25) {
  code: 'ERR_PACKAGE_PATH_NOT_EXPORTED'
}

Node.js v20.1.0
```


@auth/core:
```
  "exports": {
    ".": {
      "types": "./index.d.ts",
      "import": "./index.js"
    },
```
