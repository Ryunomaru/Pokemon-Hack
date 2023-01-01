********************************************
*** Advance Map Ver 1.80 - Francais      ***
********************************************

Ce programme est destin� � permettre de modifier les cartes, les mouvements possibles, les �v�nements et les informations relatives aux Pok�mons sauvages qui apparaissent.
Dans le futur, les informations li�es aux collisions (c-�-d les rencontres avec un objet, en se placant dessus en marchant) pouront aussi �tre modifi�es.
Il fonctionne avec les ROM de Pok�mon Rubis, Saphir et Emeraude, en langue Japonaise, Anglaise et Allemande et Fran�aise.

!!! Attention !!!
-----------------
Avec cette version, toute les modifications r�alis�es sont directement sauvegard�es dans la ROM !
Grace � la commande "Sauvegarder sous ...", il est possible de faire une copie dans un autre fichier.
Une fois la ROM recharg�e via le fichier copie, toutes les modifications sont alors sauvegard�es dans le nouveau fichier.


.:|IMPORTANT|:.
-^-^-^-^-^-^-^-
Ce programme a �t� �crit par LU-HO Pok�, et de ce fait, Copyright LU-HO Pok� !
Si vous l'avez t�l�charg� d'un autre site que de FWB (Filb's World Board [http://www.filbboard.de]),
merci de me le signaler. Mon adresse e-mail est : lu.ho@tiscali.ch


*********************************
*** Contenus des fichiers INI ***
*********************************
AdvanceMap.ini:
--------------- 
Les fichiers INI ont �t� compl�tement revus et modifi�s. 
Maintenant, chaque langage � sa configuration sp�cifique.
Au del�, chaque jeux � ses propres d�tails de configuration sp�cifiques.
Enfin, et cen'est pas la moindre modification, chaque Offset (d�calage d'adresse) est stock� dans un pattern (signature).

Par exemple :
[MapBankHeader]
art=pointer
nach=80180068890B091808687047
spiele=BPR,BPG,BPE,AXP,AXV

Cel� signifie que juste apr�s une s�quence d'octets identique � celle fournie apr�s 'nach' (le Pattern) se trouve le pointer qui d�fini le d�calage (l'Offset) pour le 'MapBankHeader' (Ent�te de la Banque de Carte).
La derni�re ligne indique que cette d�finition est valable pour plusieurs ROM, dont la liste est donn�e apr�s 'spiele'.

Autre Exemple :
[PokemonNamen]
inkSprache=1
art=pointer
vor=30B50025084CC8F7
spiele=AXPJ,AXVJ,AXPE,AXVE

[PokemonNamen2]
art=pointer
position=$000144
spiele=BPR,BPG,BPE,AXP,AXV

Ici, il y a deux paragraphes. 
Dans le premier, le param�tre 'inkSprache' �gal � 1 indique qu'il n'est valide que pour les ROM des langues sp�sifi�es dans la liste apr�s 'spiele'.
Ici, le pointeur  se trouve avant le pattern d�fini par 'vor'.
Puisque toutes les langues ne sont pas couvertes par le premier paragraphe, le deuxi�me paragraphe indique comment obtenir le pointeur pour les autres ROM. Ici, il sera plac�" � la position absolue d�finie par 'position'.

Attention � toujours mettre un "$" au d�but d'une valeur indiqu�e en hexad�cimal.


Main.ini
--------
Dans ce fichier sont �num�r�s les listes correspondant aux cartes.
Elles peuvent �tre tri�es dans l'ordre souhait�s.
Le format du fichier est le suivant :

[<Foldername>]
1=<Bank>.<map>
2=<Bank>.<map>
3=<Bank>.<map>
4=<Bank>.<map>
5=<Bank>.<map>
...

Exemple :
[0]
1=0.0
2=0.1
3=0.2
...

[1]
1=1.0
...

Les noms de dossiers peuvent �tre modifi�s � volont�;
� l'exception de :

[<FolderName>]
1=<Label>
2=<Label>
...

Pour plus de d�tails, voir le fichier "Maps.ini"


Maps.ini
--------
On trouve dans ce fichier les listes de cartes, mais seulement celles qui sont d�clar�es dans le fichier "Main.ini".

Le format est :
[<Banque>.<Carte>]
Name=<Nom_de_Carte>

Par exemple :
[0.0]
Name=PETALBURG CITY

[1.0]
Name=Route 101


Important :
Dans ce fichier, il n'est possible que de modifier la valeur du param�tre 'name' (le nom de la carte).
L'ent�te du paragraphe ("[<Banque>.<Carte>]", comme dans "[0.0]") est la r�f�rence � la position dans l'ent�te des Cartes, s'il est modifi�, la carte ne fonctionnera plus !
Les d�calages ('Offset') ne sont plus utilis�s dans cette version, mais ils peuvent demeurer dans le fichier.

Il y a une exception :
Le d�calage exact de l'en-pied de Carte (Map Footer) doit �tre d�clar� pour toutes les versions de ROM.
Sans cette information, la ROM n'est pas charg�e.

Le format est le suivant :
[<Label from Main.ini>]
Name=<Label>
<Exact Gamelabel>=<Offset>

Par exemple:
[UNKNOWN45] 
POKEMON SAPPAXPD=$2CA960 
name=Insel?


Tilesets.ini
------------
Le gestionnaire de Tilesets est apparu avec la version 1.30.
Il est maintenant possible de changer le nombre de blocs de chaque Tileset (le premier porte le num�ro 0).
Si le Tileset est dans la partie haute, il a automatiquement 200 blocs.

[1]
Blocks=$90

...

[24]
Blocks=$87


Sprachen.ini
------------
On trouve dans ce fichier les donn�es pour les diff�rentes langues disponibles.
Exemple:
[Sprachen]
1=Deutsch
2=English

Le sous r�pertoire "Ini/Sprachen" contient des fichiers nomm�s <Nom_De_Langue>.ini, dans lesquels se trouvent les traductions des textes du programme.
vous pouvez ajouter autant de langue que vous le souhaitez, mais vous devez respecter les termed du "Contrat d'Utilisateur Final" ("EndNutzer Vertrag")
Ce "Contrat d'Utilisateur Final" doit �tre traduit et �tre transmit � LU-HO pour qu'il puisse l'encrypter.
Tans que ceci n'est pas fait, la langue n'est pas disponible dans le programme. Ensuite, vous pouvez la s�lectionner avec "Settings"->"Language" ("Einstellungen"->"Sprache").

Lors du premier d�marrage de AdvanceMap, vous pouvez s�lectionner la langue de votre choix.

Les fichiers GehDaten.ini/AufgabenDaten.ini ainsi que d'autres ont maintenant �t� int�gr�s dans le nouveau fichier de langue.


********************************
***      Remerciements       ***
********************************
Les plus grand remerciements vont � Jigglypuff pour le Code Source de Goldmap2 Beta et � Jay, qui me l'a transmis.

Que soient aussi remerci�s :
Tauwasser et F-Zero pour leurs tutoriaux.
Mikaron pour ses travaux.
Serwe qui m'a apport� quelques id�es.
Mulle qui m'a signal� une erreur dans le programme.
Scizz, Timhay, GruntZ, Ashly138, Usohachi, BlueSonic, Sylph, Liquid_Thunder, IIIMQIII, Netto-kun pour leurs traductions des fichiers ini.
Et bien s�r Filb pour son Board.

Un autre grand merci � F-Zero qui m'a aid� sur les Palettes de Sprites.
Merci �galement � dark01 pour son aide sur les Sprites.
Merci � evilboy for son aide sur les FAQs.

Un dernier grand merci pour Scizz, dark01, BlueSonic et F-Zero pour leur r�le de b�ta-testeurs.
