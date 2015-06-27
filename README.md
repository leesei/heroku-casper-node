# Heroku app: casper-node

A sample Heroku application that cascades [NodeJS][] on [CasperJS][], suitable for web scraping and automation.

> Now that [phantomjs](https://www.npmjs.com/package/phantomjs) and [casperjs](https://www.npmjs.com/package/casperjs) are both available on npm, it is easier to use [Node.JS buildpack](https://devcenter.heroku.com/articles/nodejs-support) to install them.

## Usage

Example usage:

```bash
$ git clone https://github.com/leesei/heroku-casper-node.git

$ cd heroku-casper-node

$ heroku create --stack cedar --buildpack https://github.com/ddollar/heroku-buildpack-multi.git

$ git push heroku master
```

## More info

This application uses [buildpack-multi][] to cascade [buildpack-casperjs][] and [buildpack-nodejs][].

```bash
$ cat .buildpacks 
https://github.com/leesei/heroku-buildpack-casperjs.git
https://github.com/heroku/heroku-buildpack-nodejs
```

[Spooky][] is used for Casper-Node binding, you can replace it with other module of your choice.

[PhantomJS][] is also available from `buildpack-casperjs`, you may as well drive it from Node.

[buildpack-casperjs]: https://github.com/leesei/heroku-buildpack-casperjs
[buildpack-multi]: https://github.com/ddollar/heroku-buildpack-multi
[buildpack-nodejs]: https://github.com/heroku/heroku-buildpack-nodejs
[CasperJS]: http://casperjs.org/
[NodeJS]: http://nodejs.org/
[PhantomJS]: http://www.phantomjs.org/
[Spooky]: https://github.com/WaterfallEngineering/SpookyJS
