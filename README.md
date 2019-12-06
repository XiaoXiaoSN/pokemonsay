pokemonsay
==========

The project forked from [possatti/pokemonsay](https://github.com/possatti/pokemonsay)

![You should try pokemonsay!](example.png)

`pokemonsay` is like [`cowsay`][cowsay] but for pokémon only. It was inspired by [`ponysay`][ponysay] (`cowsay` for ponies). Internally, `pokemonsay` still uses `cowsay`, so you need it installed too (`cowsay`... not `ponysay`).

## Installation

### OS X

You can install `pokemonsay` through Homebrew. It is pretty straightforward:

```sh
$ brew tap xiaoxiaosn/xiaoxiao
$ brew install pokemonsay
```

## Usage

Now that you've installed `pokemonsay`, you can make it work like so:

```bash
$ pokesay Hello World
```

```bash
$ docker ps | pokesay -n $1
```

To have a random pokémon saying some random thing to you, use `fortune`:

```bash
$ fortune | pokesay
```

And if you really like it, you can add the command above to the end of your `~/.bashrc` file (or equivalent). So you will have a random pokémon speaking to you whenever you open a new terminal window! :D

You get a cowthink-like version too. Try it:

```bash
$ pokethink --pokemon Charmander "Should I wear some clothes?"
```

## Uninstall

Just in case you hate Pokémon and you've installed `pokemonsay` "by mistake"... Humpf! You can uninstall it by running:

```bash
$ sh $HOME/.pokemonsay/uninstall.sh
```

## Building the whole thing

In order to use `pokemonsay` you don't need to build anything because everything is built already within the repository. But if you want to download the whole images again or make some change in the process, here is how it's done:

```bash
# Download pokémon images from Bulbapedia... Thanks bulbapedia!
$ ./scrap_data.sh

# Manipulate the downloaded images, to make the pokémon look
# to the right, and trim the useless space around them.
$ ./fix_images.sh

# Use 'img2xterm' to generate .cow files (for 'cowsay').
$ ./make_cows.sh
```

And there it is. Now install it with `install.sh` and you are done.

## Special Thanks

A special thanks to my friend Lucas Coutinho Oliveira (@lucascsoliveira) who helped me with some Pokémon wisdom. Thanks buddy!

## NOTICE

Please notice I don't own Pokémon or anything related to it. Pokémon is property of [The Pokémon Company][the-pokemon-company].

[img2xterm]: https://github.com/rossy/img2xterm
[cowsay]: https://en.wikipedia.org/wiki/Cowsay
[ponysay]: https://github.com/erkin/ponysay
[the-pokemon-company]: https://en.wikipedia.org/wiki/The_Pok%C3%A9mon_Company
