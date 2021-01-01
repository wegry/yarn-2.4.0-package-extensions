# yarn@2.4.0 and packageExtensions

Created with

```bash
$ yarn set version berry
$ yarn init
$ yarn add webpack{,-cli}
$ mkdir src
$ touch src/index.js
```

# Building

```bash
$ yarn webpack
```

The `main` branch will fail to build because, according to yarn@2.4,

> Module not found: Error: react-twitter-widgets tried to access react (a peer dependency) but it isn't provided by your application; this makes the require call ambiguous and unsound.

Switching to the `package-extension` branch, `yarn webpack` will build successfully because we introduced a `.yarnrc.yml` file.
