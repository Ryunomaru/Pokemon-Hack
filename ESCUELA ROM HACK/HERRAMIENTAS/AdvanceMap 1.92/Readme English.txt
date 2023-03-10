********************************************
*** Advance Map Ver 1.90 - English       ***
********************************************

This program is for the editing of Map, movement permissions, block data, events and wild pokemon data.
A block editor is also available.
It is compatible with all version of Pok?mon Advance in all languages.

!!!Attention!!!
-------------
With this version all changes are saved directly into the rom!
Through "Save As" you can save the current map into another file.
Once loaded a copy of the current file is made.
All further changes are stored into the new file.



.:|IMPORTANT|:.
-^-^-^-^-^-^-
This program was programmed by LU-HO Pok? and is consequently copyrightED by LU-HO Pok?!
If you downloaded it from another place then from the FWB(Filb's World board [http://www.filbboard.de]),
please tell me right away! My mail is: lu.ho@tiscali.ch


*********************************************
***               Hot Keys                ***
*********************************************
The hotkeys are visible once you click on the menus, right behind the description.

Here we'll quickly explain most frequently needed hot keys.

Map view:
------------
Left mouse button			=> Draw current block / Stamp.
Middle mouse button			=> Fill tool, replace all connected blocks of the same type with another.
Right mouse button 			=> Select hovered block as current.

Ctrl/Strg + Left mouse button		=> Draw current block.
Ctrl/Strg + Middle mouse button		=> Fill tool, replace all connected blocks of the same type with another.
Ctrl/Strg + Right mouse button		=> Select big block, on click and select the selected area will be shown in a new window.


Map view - Block palette:
-------------------------
Left mouse button			=> Select hovered block as current.
Middle mouse button			=> Select hovered block as current.
Right mouse button			=> Select hovered block as current.

Ctrl/Strg + Left mouse button		=> Select hovered block as current.
Ctrl/Strg + Middle mouse button		=> Select hovered block as current.
Ctrl/Strg + Right mouse button		=> Select big block, on click and select the selected area will be shown in a new window.


Movement permissions:
-----------------
Left mouse button			=> Draw current block.
Middle mouse button			=> Fill tool, replace all connected blocks of the same type with another.
Right mouse button			=> Select hovered block as current.

Ctrl/Strg + Left mouse button		=> Draw current block.
Ctrl/Strg + Middle mouse button		=> Fill tool, replace all connected blocks of the same type with another.
Ctrl/Strg + Right mouse button		=> Select hovered block as current.


Movement permission palette:
---------------------------------
Left mouse button			=> Select hovered block as current.
Middle mouse button			=> Select hovered block as current.
Right mouse button			=> Select hovered block as current.

Ctrl/Strg + Left mouse button		=> Select hovered block as current.
Ctrl/Strg + Middle mouse button		=> Select hovered block as current.
Ctrl/Strg + Right mouse button		=> Select hovered block as current.


Event view:
--------------
Left mouse button			=> Select top event on position/move
Middle mouse button			=> Select top event on position (no moving)
Right mouse button			=> Select lowest event on position/move

Ctrl/Strg + Left mouse button		=> Select top event on position/move
Ctrl/Strg + Middle mouse button		=> Select top event on position (no moving)
Ctrl/Strg + Right mouse button		=> Select lowest event on position/move

Left mouse button double click		=> Select top event on position and open in script editor
Middle mouse button double click	=> Select top event on position and open in script editor
Right mouse button double click		=> Select lowest event on position and open in script editor



********************************
***     Contents of Inis     ***
********************************

AdvanceMap.ini:
--------------- 
The INI has been completely revamped.
Now every language has it's specific settings.
Further all games have some Game specifiy settings.
Last but not least, every offset is stored by a pattern.

Example:
[MapBankHeader]
art=pointer
nach=80180068890B091808687047
spiele=BPR,BPG,BPE,AXP,AXV

This means that after the Bytes after "nach" the Pointer to the Map Header is following.
This setting goes for all games which are listed under "spiele".


Example 2:
[PokemonNamen]
inkSprache=1
art=pointer
vor=30B50025084CC8F7
spiele=AXPJ,AXVJ,AXPE,AXVE

[PokemonNamen2]
art=pointer
position=$000144
spiele=BPR,BPG,BPE,AXP,AXV

Here are 2 entrys. In the 1st, all language parameters are set in the "spiele"- listing, because "inkSprache" is set to 1.
Also we have the pointer to the at point "vor" described Bytes.
Because not all games are used under the 1st entry, there's a 2nd entry which will be used for all games.
After the 2nd entry, the Pointer will be found at the position set in the "position" variable.


Hex values always have to carry a "$"!


Main.ini
--------
Here the orders with the corresponding maps are listed.
Many new orders can be produced at will.
The format is as follows:

[<Foldername>]
1=<Bank>.<map>
2=<Bank>.<map>
3=<Bank>.<map>
4=<Bank>.<map>
5=<Bank>.<map>
...

Example:
[0]
1=0.0
2=0.1
3=0.2
...

[1]
1=1.0
...

The foldernames can be changed as you please;

There are exceptions:
[<FolderName>]
1=<Label>
2=<Label>
...
For more, see Maps.ini


Maps.ini
--------
Here the maps are listed, but only the ones that are listed in Main.ini
appear.
[<Bank>.<map>]
Name=<Label>

[0.0]
Name=PETALBURG CITY

[1.0]
Name=Route 101

Important:
Here you should only alter the 'name' attribute.
The heading of the entry "[0.0]" refers to the position in the map header, if this is altered
then the maps will no longer work!
The offsets are no longer used in this version, however they can remain in there.

The exception:
Here for all game versions the exact offset to the Map Footer has to be declared.
Those without an offset won't be loaded.

[<Label from Main.ini>]
Name=<Label>
<Exact Gamelabel>=<Offset>


Example:
[UNKNOWN45] 
POKEMON SAPPAXPD=$2CA960 
name=Insel?


Tilesets.ini
------------
The tileset-builder is new from version 1.30.
Optionally, here you can change the number of blocks each tileset has (first tileset is 0)
If the tileset is in the upperpart it has 200 blocks automatically.

[1]
Blocks=$90

...

[24]
Blocks=$87


Sprachen.ini
------------
Here all languages that are available are listed.
Example:
[Sprachen]
1=Deutsch
2=English

In the subfolder "Ini/Sprachen" you can find a <Languagename>.ini-file, in which the texts are stored.
You can add as many languages as you want, but you have to take care of the "EndNutzer Vertrag".
The "EndNutzer Vertrag" has to be translated, and send to me so that I can encrypt it.
As long as I haven't done that, the language is not available....
You can change the language under "Settings"->"Language".

At the first start of AdvanceMap, you can select the language of your choice.

The files GehDaten.ini/AufgabenDaten.ini and others have been included in the new language files.



********************************
***          Greets          ***
********************************
A huge greeting goes to:
Jigglypuff for the Source of Goldmap2 Beta
and Jay, who gave it to me.

Further greets go to:
Tauwasser and F-Zero for their tutorials.
Mikaron for his work.
Serwe for giving me a few ideas.
Mulle who pointed me to a mistake.
Scizz, Timhay, GruntZ, Ashly138, Usohachi, BlueSonic, Sylph, Liquid_Thunder, IIIMQIII, Netto-kun for the translations of the inis.
And of course, Filb for his board.
Another tahnk you goes out to F-Zero who helped me with the Sprite-Pallets.
Also dark01 received a big thank you for his help with the Sprites.
Thanks to evilboy for his help at the FAQs.
Another thanks goes to Scizz, dark01, BlueSonic and F-Zero for the Beta tests.
Aruka and perappu music list extension.
A big thanks goes to Mastermind_X for the structure of the Word Map data and for helping me make use of it.
A big thanks to Tutti for his great beta testing and extension of the behaviour data.
Tauwasser, Scizz, Satry, Ashly138, Anthony, wakachamo, HackMew, Christos, Martin?, Sebbe17/Jungleman, 44tim44 for the new translations of the INIs.