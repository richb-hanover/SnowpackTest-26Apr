# Starting new Snowpack project

* On 26 Apr 2021, use npx with a blank typescript template to create  new project.

* By default, this installs Snowpack 3.0.1. This generates the deprecated warnings (below).

* Manually changing to Snowpack 3.3.4 in the package.json file removes these warnings. The project seems to run fine.

* Using `yarn start`, see the second set (below) of Rollup warnings about *preventAssignment* even though the project doesn't use Rollup.

```
√ github % npx create-snowpack-app test26mar --template @snowpack/app-template-blank-typescript --use-yarn
npx: installed 24 in 2.795s

  - Using template @snowpack/app-template-blank-typescript
  - Creating a new project in /Users/richb/github/test26mar
  - Installing package dependencies. This might take a couple of minutes.

warning package.json: No license field
warning ../package.json: No license field
warning No license field
warning snowpack > rollup > fsevents@2.1.3: "Please update to latest v2.3 or v2.2"
warning snowpack > pacote > @npmcli/run-script > node-gyp > request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
warning snowpack > pacote > @npmcli/run-script > node-gyp > request > har-validator@5.1.5: this library is no longer supported

  - Initializing git repo.

  - Success!

Quickstart:

  cd test26mar
  yarn start

All Commands:

  yarn install     Install your dependencies. (We already ran this one for you!)
  yarn start       Start your development server.
  yarn run build   Build your website for production.
  yarn test        Run your tests.

```

## Error on initial start

```
√ test26mar % yarn start
yarn run v1.22.10
warning package.json: No license field
warning ../package.json: No license field
$ snowpack dev
[22:14:17] [snowpack] Welcome to Snowpack! Because this is your first time running
this project, Snowpack needs to prepare your dependencies. This is a one-time step
and the results will be cached for the lifetime of your project. Please wait...
[22:14:17] [snowpack] + canvas-confetti@1.4.0
[22:14:17] [esinstall:canvas-confetti] @rollup/plugin-replace: 'preventAssignment' currently defaults to false. It is recommended to set this option to `true`, as the next major version will default this option to `true`.
[22:14:17] [snowpack] Ready!
[22:14:17] [snowpack] Server started in 16ms.
[22:14:17] [snowpack] Local: http://localhost:8080
[22:14:17] [snowpack] Network: http://192.168.253.116:8080
[22:14:18] [@snowpack/plugin-typescript] 9:13:18 PM - Starting compilation in watch mode...
[22:14:19] [@snowpack/plugin-typescript] 9:13:19 PM - Found 0 errors. Watching for file changes.
⠏ watching for file changes...^C
```