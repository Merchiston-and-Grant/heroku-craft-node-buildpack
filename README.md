# Heroku Craft Node Buildpack

A Heroku buildpack for deploying Craft CMS sites that have a Node.js front-end build.

It runs after the standard Node and PHP buildpacks and:

1. runs `npm install` in `app/src`;
2. writes the deployed commit hash to `app/craft/config/version.php`;
3. makes `app/craft` the root of the deployed app, dropping everything else.

## Usage

Always pin to a tag, never a branch:

```bash
heroku buildpacks:add https://github.com/Merchiston-and-Grant/heroku-craft-node-buildpack#0.3.0 --app <app>
```

To move an app to a new tag, change staging first, check a build, then live.

## Version

Current version: 0.3.0

Previously `sporkdigital/spork-heroku-craft-node-buildpack`. Moved to Merchiston & Grant in October 2026.

## Maintainer

Merchiston & Grant
