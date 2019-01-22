# Le French typography

Sketch plugin to automatically add typographical French conventions and give a nice touch to UIs. Things like nonbreakable spaces or better fractions.

Install with the plugin manager Sketchpacks or by downloading
[the latest release](https://github.com/Saint-loup/french-typography/releases/latest) and opening the sketchplugin file.

[![Install PLUGIN NAME with Sketchpacks](french-typography/assets/sketchpacks-badge-install.png "Install French Typography with Sketchpacks")](https://www.sketchpacks.com/Saint-loup/french-typography)


##  What it does

When you unselect a text layer, it replaces characters with their proper equivalents. 

* It works whether you enable smart quotes substitutions at the system level (System > Keyboard > Text), since this Mac OS feature doesn't use non-breakable space.
* There's a setting to enable narrow non-breakable space. Toggling it replaces back and forth narrow and normal spaces in all the current Sketch document. The setting is closer to French conventions but off by default. The reason is a bug in Safari: resulting spaces will be displayed as zero-width, for instance if you copy & paste the text or export it with Craft. Sorry. The choice between compatibility and typographical correctness is yours to make.
* The plugin is called "French" but may work in some francophone contexts. Emphasis on *may*. No official support is hereby implied.


##### Insertion of non-breaking spaces

| Symbol                 | Statut |
| --------------------- | ------- |
| :                     |    ✔️   |
| «                     |    ✔️   |
| »                     |    ✔️ ️  |
| !                     |    ✔️   |
| ?                     |    ✔️   |
| ;                     |    ✔️   |
| %                     |    ✔️   |
| Em-dash / tiret demi-quadratin      |    ️ ✔️   |
| Currency :  $ €        |     ✔️    |
| Space between hundreds, thousands  |         |


#### Remplacement de caractères

| Symbole                      | Statut |
| ---------------------------- | ------ |
| From " to «                |     ✔️️️    |
| Double dash --> em-dash       |  ✔️    |
| Some fractions (½, ⅓, ¼ ) | ✔️   |
| Ordinal suffixes (1er, 2e…)|  ✔️️   |
| Ellipsis…   |   ✔️   |
| From N° to №                     |    ✔️️️  |


## What it doesn't do


* Inserting non-breaking spaces in complex cases (eg. latitudes), listed [here](https://www.btb.termiumplus.gc.ca/tpv2guides/guides/chroniq/index-fra.html?lang=fra&lettr=indx_autr8cDRJ-6fjpl0&page=9ouqyIer24Kc.html) or [there](https://en.wikipedia.org/wiki/Wikipedia:Manual_of_Style#Non-breaking_spaces).
* Accents on capital letters. There's no way to automatically tell SALE and SALÉ apart.
* Things that would be better handled with dedicated markup. For instance support and rendering of [fractions and exposants](https://en.wikipedia.org/wiki/Unicode_subscripts_and_superscripts#Superscripts_and_subscripts_block) in Unicode is really spotty.
* Typos like double spaces.


## Boring stuff

#### Build from source

Follow SKPM instructions : [here](https://skpm.io/help/) and [there](https://developer.sketchapp.com/guides/)

#### Tests

To check for errors in regex, in the plugin folder run:

`npm test`

It's a shorcut for : 
build && <sketchTool path> run <plugin path> testRegex

#### Debuging

There's a little debug mode, enabled by placed a file named "debug" in the assets folder. The result is some more in the console and in SKetch, when using the plugin. 
