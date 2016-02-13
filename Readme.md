[![Travis – build status
](https://img.shields.io/travis/tomekwi/elm-live/master.svg?style=flat-square
)](https://travis-ci.org/tomekwi/elm-live
) [![David – status of dependencies
](https://img.shields.io/david/tomekwi/elm-live.svg?style=flat-square
)](https://david-dm.org/tomekwi/elm-live
) [![Code style: airbnb
](https://img.shields.io/badge/code%20style-airbnb-777777.svg?style=flat-square
)](https://github.com/airbnb/javascript
)




# elm-live

**A flexible dev server for Elm  
Live reload included!**




<a                                                   id="/screenshot"></a>&nbsp;

<p align="center"><img
  alt="Screenshot"
  src="https://cdn.rawgit.com/tomekwi/elm-live/e851ffd/shot.png"
  title="Sweet, isn’t it?"
  width="656"
  height="308"
/></p>




<a                                                 id="/installation"></a>&nbsp;

## INSTALLATION

```sh
# Globally for a user:
npm install --global elm elm-live

# …or locally for a project:
npm install --save-dev elm elm-live
```

If you’d rather bring your own global `elm-make`, `npm install --global elm-live` will do.

Note that you need *node 4.0+* to run the tool natively. But if you’re stuck on an older version, don’t worry! [Rumour has it](https://github.com/tomekwi/elm-live/issues/2#issuecomment-156698732) that you can transpile the code to ES5!




<a                                                     id="/synopsis"></a>&nbsp;

## SYNOPSIS

```sh
elm-live [<OPTIONS>] [--] <ELM-MAKE ARGS>  
elm-live --help
```




<a                                                  id="/description"></a>&nbsp;

## DESCRIPTION

First, we spawn `elm-make` with the `ELM-MAKE ARGS` you’ve given.

When the build is ready, we start a static HTTP server in the current directory. We inject a _live reload_ snippet into every HTML file we serve. Every time a static file has changed, we’ll reload your app in all browsers you’ve opened it with. (Mobile and IE included!)

We also watch all `*.elm` files in the current directory and its subdirectories. Whenever you change, add or remove one of them, we’ll rebuild your program and reload the page.




<a                                                      id="/options"></a>&nbsp;

## OPTIONS

#### `--port=PORT`
Set the port to start the server at. `PORT` should be a valid port number. Default: `8000`.

#### `--open`
We’ll open the app in your default browser as soon as the server is up.

#### `--help`
You’re looking at it.




<a                                                      id="/license"></a>&nbsp;

## LICENSE

[MIT][] © [Tomek Wiszniewski][]

[MIT]: ./License.md
[Tomek Wiszniewski]: https://github.com/tomekwi
