# sudweb.fr/2015 [![Stories in Ready](https://badge.waffle.io/sudweb/2015.png?label=ready&title=Ready)](https://waffle.io/sudweb/2015) [![Build Status](https://travis-ci.org/sudweb/2015.png?branch=master)](https://travis-ci.org/sudweb/2015)

Just some good old static webpages. We like to KISS.

## Contribute

Just fork this repo, commit your changes and open a pull request.

## Requirements

This project uses Sass, node and Grunt because we are cool kids.

You shoud be able to install node in a few commands:

* `brew install node` on Mac OS X for instance

## Install

`npm install` will install all dependencies mentioned in the package.json file

Now you just have to type `grunt` to run tasks and watch the changes :)

```
$ npm run watch
Running "htmlhint:build" (htmlhint) task
>> 6 files lint free.

Running "sass:dist" (sass) task

Running "watch" task
Waiting...
```

Happy coding!

## Thumbnails

You initially need to install [GraphicsMagick](http://www.graphicsmagick.org).

```bash
brew install graphicsmagick
```

Then run, each time you need to regenerate thumbnails:

```bash
npm run thumbs
```

They will be located in `img/orateurs/150`.

## Deploy

### Production

Once you are satisfied and are ready to deploy on `sudweb.fr/2015`, proceed as below:

```bash
npm run deploy-prod
ssh sudweb 'cd www/2015 && git pull'
```

**Notice**: `sudweb` is a hostname configured in `~/.ssh/config`.

### Development

To share what you have done without publishing it live, use the following command:

```bash
npm run deploy-dev
```

The content will be available on `http://<your username>.github.io/2015`.
