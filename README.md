Roundcube Webmail Stretched Elastic
===================================
This skin extends the Elastic skin shipped with Roundcube to add support for
Desktop and List display modes on the mail screen along with a few other
minor tweaks. This skin is not a standalone package.

ATTENTION
---------
This is just a snapshot from the GIT repository and is **NOT A STABLE version
of Stretched Elastic**. It is Intended for use with the **GIT-master** version
of Roundcube and it may not be compatible with older versions. Stable versions
of Stretched Elastic are available from the [Roundcube plugin repository][rcplugrepo]
or the [releases section][releases] of the GitHub repository.

License
-------

The contents of this folder are subject to the Creative Commons
Attribution-ShareAlike License. It is allowed to copy, distribute,
transmit and to adapt the work by keeping credits to the original
authors in the README.md file. See [CC BY-SA 3.0][ccv3] for details.

Install
-------
* Place this skin folder into skins directory of Roundcube
* To set this is the default skin set $config['skin'] to stretchedelastic
* To hide the original Elastic skin on the Roundcube settings screen use the
$config['skins_allowed'] option

**NB:** When downloading the plugin from GitHub you will need to create a
directory called stretchedelastic and place the files in there, ignoring the
root directory in the downloaded archive.

All styles are written using LESS syntax. The skins is distributed with
precompiled CSS but should you wish to customise it then recompliation can be
done using the lessc (>= 2.5.2) command line tool. This comes with the
nodejs-less RPM package or using npm install less which depend on nodejs.

    $ lessc --clean-css="--s1 --advanced" --include-path=../elastic/styles styles/styles.less > styles/styles.min.css

(--clean-css="--s1 --advanced" minifies the css, requires the clean-css Less
plugin. The plugin can be installed using npm install less-plugin-clean-css)

References to image files from the included CSS files can be appended with
cache-buster marks to avoid browser caching issues after updating.

Run bin/updatecss.sh --dir skins/stretchedelastic before packaging the skin or
after installing it on the destination system.

For Developers
--------------
- Skin color palette changes and other css modifications can be done
  via _styles.less and _variables.less files. Where you can overwrite all
  variables and add custom styles.

[rcplugrepo]: https://plugins.roundcube.net/#/packages/johndoh/stretchedelastic
[releases]: https://github.com/johndoh/roundcube-stretchedelastic/releases
[ccv3]: https://creativecommons.org/licenses/by-sa/3.0/