# videojs-clsp Developer Notes <!-- omit in toc -->

## Table of Contents <!-- omit in toc -->

- [Getting Started](#getting-started)
    - [Prepare Node environment](#prepare-node-environment)
    - [Run development server](#run-development-server)
    - [Lint](#lint)
- [Versioning](#versioning)
- [Publishing](#publishing)
- [References](#references)


## Getting Started

### Prepare Node environment

1. Install latest NodeJS LTS version using `tj/n`:
    * [https://github.com/tj/n](https://github.com/tj/n)
        * **NOTE:** As of [`v0.19.5`](https://github.com/skylineos/videojs-clsp/releases/tag/v0.19.5), the NodeJS version must be `>=12 <13`.
    * Note if you're on Windows, you'll have to use a different node installation method
1. Install latest Yarn v1:
    * [https://classic.yarnpkg.com/en/docs/install#debian-stable](https://classic.yarnpkg.com/en/docs/install#debian-stable)
1. `yarn install`

### Run development server

1. `yarn run serve`
    * set `DEV_SERVER_HOST` to change the default host of `0.0.0.0`
    * set `DEV_SERVER_PORT` to change the port of `8081`
1. navigate to [http://localhost:8081](http://localhost:8081) in a supported browser
1. add a `clsp` url to any of the inputs, then click submit
1. click play on the video element (if not using an autoplay player)

### Lint

To lint your code after making changes, run:

```
yarn run lint
```


## Versioning

@see:

* [https://yarnpkg.com/lang/en/docs/cli/version/](https://yarnpkg.com/lang/en/docs/cli/version/)
* [https://semver.org/](https://semver.org/)

```
yarn version --new-version 1.2.3+4
```

## Publishing

1. Ensure all lint checks and tests pass
1. It is best to do this immediately after cutting a release tag
1. You MUST be on an unmodified checkout of the `git` tag you intend to publish.  i.e, `git status` should show:
    1. You have a tag checked out
    1. There are no changes staged for commit
1. You MUST have already run `yarn install`, since the dependencies are necessary for building and publishing
1. You MUST be logged in to the public npm registry
1. You MUST have access to the `skylineos` organization on npm
1. You MUST ONLY publish releases (e.g. `0.18.0`) or pre-releases (e.g. `0.18.0-4`)
    1. no builds or anything else without approval
    1. pre-releases should be published with the `beta` tag, e.g. `npm publish --tag beta`

When the above checklist is complete, publish via:

```
npm publish
```


## References

* [https://videojs.com/](https://videojs.com/)
* [https://docs.videojs.com/](https://docs.videojs.com/)
* [https://videojs.com/plugins/](https://videojs.com/plugins/)
* [https://github.com/videojs/generator-videojs-plugin](https://github.com/videojs/generator-videojs-plugin)
* [https://github.com/videojs/Video.js/blob/master/docs/guides/plugins.md](https://github.com/videojs/Video.js/blob/master/docs/guides/plugins.md)
* [https://github.com/videojs/generator-videojs-plugin/blob/master/docs/conventions.md](https://github.com/videojs/generator-videojs-plugin/blob/master/docs/conventions.md)
