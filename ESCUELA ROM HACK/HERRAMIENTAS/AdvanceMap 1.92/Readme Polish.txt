********************************************
*** Advance Map Ver 1.80 - Polish        ***
********************************************

Ten program s�u�y do edycji map, zezwole� ruchu, danych klock�w, event'�w i danych dzikich pokemon'�w.
P�niej do edycji powinny by� dost�pne te� dane kolizji.
Dzia�a on z ROM'ami Pokemon Ruby and Sapphire, Japanese and English.

!!!Uwaga!!!
-------------
W tej wersji zmiany s� zapisywane bezpo�rednio do ROM'a!
Wci�nij "Zapisz jako" by zapisa� map� w innym pliku.
Potem wczytaj �wie�o stworzony plik.
Wszystkie kolejne zmiany b�d� zapisywane w nowym pliku.



.:|WA�NE|:.
-^-^-^-^-^-^-
Ten program zosta� stworzony przez LU-HO Pok� i w rezultacie prawa autorskie nale�� do LU-HO Pok�!
Je�eli pobra�e� ten plik z innej strony ni� FWB(Filb's World board [http://www.filbboard.de]),
prosz� napisz mi o tym szybko! M�j mail to: lu.ho@tiscali.ch


**************************************
***    Zawarto�� plik�w ".ini"     ***
**************************************
AdvanceMap.ini:
--------------- 
Ten plik zosta� kompletnie zmieniony.
Teraz ka�dy j�zyk posiada swoje w�asne ustawienia.
W przysz�o�ci ka�da gra b�dzie posiada�a swoje w�asne ustawienia.
Ostatnie, lecz nie ostatnie, ka�dy offset jest przechowywany za pomoc� wzoru.

Przyk�ad:
[MapBankHeader]
art=pointer
nach=80180068890B091808687047
spiele=BPR,BPG,BPE,AXP,AXV

To znaczy, �e za bajtem "nach" b�dzie pod��a� pointer od nag��wka mapy. 
Te opcje znajduj� si� pod lini� "spiele".


Przyk�ad 2:
[PokemonNamen]
inkSprache=1
art=pointer
vor=30B50025084CC8F7
spiele=AXPJ,AXVJ,AXPE,AXVE

[PokemonNamen2]
art=pointer
position=$000144
spiele=BPR,BPG,BPE,AXP,AXV

To s� 2 wyj�cia. w pierwszym, wszystkie poarametry j�zykowe s� ustawione w "spiele"- , poniewa� "inkSprache" jest ustawione na 1.
Also we have the pointer to the at point "vor" described Bytes.
Poniewa� nie we wszystkich grach mo�na wyko�ysta� pierwsze wyj�cie, jest drugie wyj�cie, kt�re zosta�o u�yte do wszystkich gier.
W drugim wyj�ciu, pointer znajduje si� na swojej pozycji w "position" zmiennie.


Warto�ci hex'owe zawsze maj� przed sob� znak "$"!


Main.ini
--------
Tu s� zamieszczone wszystkie zarz�dzenia odpowiadaj�ce mapom.
Wszystko jest zapisane w poni�szym formacie:

[<Foldername>]
1=<Bank>.<map>
2=<Bank>.<map>
3=<Bank>.<map>
4=<Bank>.<map>
5=<Bank>.<map>
...

Przyk�ad:
[0]
1=0.0
2=0.1
3=0.2
...

[1]
1=1.0
...

Nazwy folder�w mo�esz sobie zmienia� dowoli;

S� pewne wyj�tki:
[<nazwa folderu>]
1=<etykieta>
2=<etykieta>
...
Po wi�cej musisz zerkn�� do Maps.ini


Maps.ini
--------
Tu znajduje si� spis map, ale tylko tych kt�re s� zapisane w Main.ini .
[<Bank>.<map>]
Name=<etykieta>

[0.0]
Name=PETALBURG CITY

[1.0]
Name=Route 101

Wa�ne:
Tu znajdzeisz tylko atrybuty 'name'.
Wyj�ciowym jest "[0.0]" je�eli jego zabraknie �adna mapa nie zadzia�a!
Offsety ju� nie s� u�ywane w tej wersji wi�c mo�esz je zmieni�.

Wyj�tek:
Tutaj etykieta do offset'u z stopki mapy musi by� zadeklarowana.
Bez tego offset si� nie za�aduje.

[<etykieta od Main.ini>]
Name=<etykieta>
<Dok�adna etykieta gry>=<Offset>


Przyk�ad:
[UNKNOWN45] 
POKEMON SAPPAXPD=$2CA960 
name=Insel?


Tilesets.ini
------------
Tileset-builder jest nowszy od wersji ver. 1.30.
Teraz mo�esz zmienia� numery klock�w z tymi z innych tileset'�w (pierwszy tileset to 0)
Je�eli tlieset jest w wy�szej cz�ci zmianie ulegnie 200 klock�w.

[1]
Blocks=$90

...

[24]
Blocks=$87


Sprachen.ini
------------
Wszystkie j�zyki s� zapisane w pewien spos�b.
Przyk�ad:
[Sprachen]
1=Deutsch
2=English

w pod-folderze "Ini/Sprachen" mo�esz znale�� <nazwa j�zyka>.ini-file, gdzie s� przechowywane teksty.
Mo�esz doda� tyle j�zyk�w, ile dusza zapragnie, ale musisz uwa�a� na "EndNutzer Vertrag".
"EndNutzer Vertrag" musi by� przt�umaczone, a �eby to zrobic musisz wys�a� do mnie ten j�zyk a ja go zamieszcz�.
Jak d�ugo tego nie zrbisz, tak d�ugo ten j�zyk nie b�dzie dost�pny ....
Mo�esz zmienia� j�zyki w "Settings"->"Language".

w czasie pierwszego startu AdvanceMap'a, mo�esz wybra� j�zyk.

Pliki GehDaten.ini/AufgabenDaten.ini i inne s� zaliczone w pliki nowego j�zyka.



***************************
***    Podzi�kowania    ***
***************************
Wielkie podzi�kowania id� do:
Jigglypuff for the Source of Goldmap2 Beta
and Jay, who gave it to me.

Dalsze podzi�kowania w�druj� do:
Tauwasser and F-Zero for their tutorials.
Mikaron for his work.
Serwe for giving me a few ideas.
Mulle who pointed me to a mistake.
Scizz, Timhay, GruntZ, Ashly138, Usohachi, BlueSonic, Sylph, Liquid_Thunder, IIIMQIII, Netto-kun for the translations of the inis.
And of course, Filb for his board.
Another tahnk you goes out to F-Zero who helped me with the Sprite-Pallets.
Also dark01 received a big thank you for his help with the Sprites.
Thanks to evilboy for his help at the FAQs.
Another thanks goes to Scizz, dark01, BlueSonic and F-Zero for the Betatests.