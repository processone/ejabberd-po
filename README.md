# ejabberd-po

This repository contains the `po` files that translators can edit to [localize ejabberd](https://docs.ejabberd.im/developer/extending-ejabberd/localization/#title) to their language.

As an alternative, you can use the [ejabberd-po Weblate](https://hosted.weblate.org/projects/ejabberd/ejabberd-po/) online service.

## Obtain your po file

First of all, get the po file of your language:
- If you already downloaded ejabberd source code, you can download this repository by running
  `./configure --enable-tools; ./rebar get-deps`
- If you have a Github account and plan to submit a Pull Request with your work, clone this repository.
- Or you can download only a po file, simply go to the [src dir](https://github.com/processone/ejabberd-po/tree/main/src), select your file, and click on `Raw`.

## Editor program

To edit a `po` file, you can use any [gettext](https://www.gnu.org/software/gettext/)-compatible program, for example:
- [Poedit](https://poedit.net/) (for Linux, Mac, Windows)
- [Virtaal](https://virtaal.translatehouse.org/) (for Linux, Mac, Windows)
- [Lokalize](https://apps.kde.org/en/lokalize) (for Linux KDE desktop)

## Share your improvements

Once you are happy with your translation work, you can submit a pull request in this github repository, or send your po file to the ejabberd mailing list...

## Test your translation in ejabberd

If you want to start using your translation, or see it in action, run this in the ejabberd source code directory:
```
./configure --enable-tools
./rebar get-deps
```

Then copy your updated po file in `deps/ejabberd-po/src/`

And finally prepare and process it with:
```
make translations
```
