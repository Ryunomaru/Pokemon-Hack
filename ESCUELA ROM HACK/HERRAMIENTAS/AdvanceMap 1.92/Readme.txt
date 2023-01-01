*********************************************
***          Advance Map Ver 1.92         ***
*********************************************
Dieses Programm ist f�r das Editieren von Maps, Gehdaten, Blockdaten, Events und Wildepokemondaten.
Man kann diese Daten editieren oder dem Spiel neue Daten hinzuf�gen.
Es ist auch ein Blockeditor enthalten
AM l�uft mit allen Pokemon Roms der AdanceVersion, in allen sprachen.
Neu k�nnen auch die Daten der Weltkarte ge�ndert werden.


!!!Achtung!!!
-------------
Bei dieser Version werden alle �nderungen direkt ins Rom gespeichert!
Durch Speichern unter kann man die aktuelle Map in eine andere Datei speichern.
Die Datei wird zuerst erstellt, indem die aktuelle Datei kopiert wird.
Alle weiteren �nderungen werden dann in die neue Datei gespeichert.


.:|WICHTIG|:.
-^-^-^-^-^-^-
Dieses Programm wurde von LU-HO Pok� programmiert und ist somit Copyright by LU-HO Pok�!
Dies wurde von Jiggly (programmierer von Goldmap 2 Beta) Officiel best�tigt.
Wen ihr AM von wo anderst als direkt bei http://am160.no-ip.info, vom FWB(Filb's World Board), von www.LU-HO.ch.vu, ampage.no-ip.info oder von
www.romhackersworld.de.vu runtergeladen habt, richtet mir das Bitte per E-Mail aus!



*********************************************
***          Tastenkombinationen          ***
*********************************************
Im Men� sind jeweils die Tastenkombinationen f�r den entsprechenden Men�punkt Sichtbar.

In den folgenden Kapiteln werden die verschiedenen M�glichkeiten beim editieren der Map aufgezeigt.


Map Ansicht:
------------
Linke Maustaste		=> Aktueller Block zeichnen / Stempel einf�gen
Mittlere Maustaste	=> F�llwerkzeug, alle zusammenh�ngenden Bl�cke mit dem aktuellen Block ersetzen.
Rechte Maustaste	=> Block unter Maus als aktueller Block ausw�hlen

Ctrl/Strg + Linke Maustaste	=> Nicht speziell, Aktueller Block zeichnen
Ctrl/Strg + Mittlere Maustaste	=> F�llwerkzeug, alle gleichen Blocks auf der Map(Auch nicht zusammenh�ngende) mit dem aktuellen Block ersetzen
Ctrl/Strg + Rechte Maustaste	=> Grosser Block ausw�hlen, beim klicken und fahren sieht man ein neues Fenster in dem der �Stempel� Block angezeigt wird.


Map Ansicht BlockPalette:
-------------------------
Linke Maustaste		=> Block unter Maus als aktueller Block ausw�hlen
Mittlere Maustaste	=> Block unter Maus als aktueller Block ausw�hlen
Rechte Maustaste	=> Block unter Maus als aktueller Block ausw�hlen

Ctrl/Strg + Linke Maustaste	=> Block unter Maus als aktueller Block ausw�hlen
Ctrl/Strg + Mittlere Maustaste	=> Block unter Maus als aktueller Block ausw�hlen
Ctrl/Strg + Rechte Maustaste	=> Grosser Block ausw�hlen, beim klicken und fahren sieht man ein neues Fenster in dem der �Stempel� Block angezeigt wird.


Gehdaten Ansicht:
-----------------
Linke Maustaste		=> Aktueller GehDatenBlock zeichnen
Mittlere Maustaste	=> F�llwerkzeug, alle zusammenh�ngenden GehDatenBl�cke mit dem aktuellen GehDatenBlock ersetzen.
Rechte Maustaste	=> GehDatenBlock unter Maus als aktueller GehDatenBlock ausw�hlen

Ctrl/Strg + Linke Maustaste	=> Nicht speziell, Aktueller GehDatenBlock zeichnen
Ctrl/Strg + Mittlere Maustaste	=> F�llwerkzeug, alle gleichen GehDatenBlocks auf der Map(Auch nicht zusammenh�ngende) mit dem aktuellen GehDatenBlock ersetzen
Ctrl/Strg + Rechte Maustaste	=> GehDatenBlock unter Maus als aktueller GehDatenBlock ausw�hlen


Gehdaten Ansicht GehdatenPalette:
---------------------------------
Linke Maustaste		=> GehDatenBlock unter Maus als aktueller GehDatenBlock ausw�hlen
Mittlere Maustaste	=> GehDatenBlock unter Maus als aktueller GehDatenBlock ausw�hlen
Rechte Maustaste	=> GehDatenBlock unter Maus als aktueller GehDatenBlock ausw�hlen

Ctrl/Strg + Linke Maustaste	=> GehDatenBlock unter Maus als aktueller GehDatenBlock ausw�hlen
Ctrl/Strg + Mittlere Maustaste	=> GehDatenBlock unter Maus als aktueller GehDatenBlock ausw�hlen
Ctrl/Strg + Rechte Maustaste	=> GehDatenBlock unter Maus als aktueller GehDatenBlock ausw�hlen


Event Ansicht:
--------------
Linke Maustaste		=> Auswahl des obersten Events an dieser Stelle/verschieben
Mittlere Maustaste	=> Auswahl des obersten Events an dieser Stelle nicht verschieben
Rechte Maustaste	=> Auswahl des untersten Events an dieser Stelle/verschieben

Ctrl/Strg + Linke Maustaste	=> Auswahl des obersten Events an dieser Stelle/verschieben
Ctrl/Strg + Mittlere Maustaste	=> Auswahl des obersten Events an dieser Stelle nicht verschieben
Ctrl/Strg + Rechte Maustaste	=> Auswahl des untersten Events an dieser Stelle/verschieben

Linke Maustaste doppelklick	=> Auswahl des obersten Events an dieser Stelle und �ffnen des Scriptes im Externen Programm
Mittlere Maustaste doppelklick	=> Auswahl des obersten Events an dieser Stelle und �ffnen des Scriptes im Externen Programm
Rechte Maustaste doppelklick	=> Auswahl des untersten Events an dieser Stelle und �ffnen des Scriptes im Externen Programm


*********************************************
***            Inhalt der inis            ***
*********************************************

AdvanceMap.ini:
--------------- 
Dise ini wurde komplet �berarbeitet.
Nun steht f�r jede Sprache Sprachspezifische einstellungen.
Weiter gibt es f�r jedes Spiel R/S/E/FR/LG ein paar Speilspezifiesche einstellungen.
Und zum Schluss ist jeder ben�tigete Offset anhand eines Musters gespeichert.

Beispiel:
[MapBankHeader]
art=pointer
nach=80180068890B091808687047
spiele=BPR,BPG,BPE,AXP,AXV

Dies Bedeutet das nach den Bytes hinter "nach" der Pointer auf den MapHeader folgt.
Die Einstellungen gelten f�r alle Spiele welche unter "spiele" aufgelistetsind.


Beispiel2;
[PokemonNamen]
inkSprache=1
art=pointer
vor=30B50025084CC8F7
spiele=AXPJ,AXVJ,AXPE,AXVE

[PokemonNamen2]
art=pointer
position=$000144
spiele=BPR,BPG,BPE,AXP,AXV

Hier hat es 2 Eintr�ge. Beim 1. werden in der "spiele"- Auflistung die Sprachabk�rzung inbgriffen, weil "inkSprache" auf 1 gesetzt wurde.
Zudem ist hier der Pointer vor den unter "vor" beschriebenen Bytes.
Da mit diesem Eintrag nicht alle Spiele abgedekt sind, gibt es einen 2. Eintrag f�r diesen Offset welche f�r die andere Spiele g�ltig ist.
Nach dem 2.Eintrag befindet sich der Pointer an der unter "position" angegebenen Stelle im Rom.


Bei Hex Werten muss ein "$" davor stehen!


Main.ini
--------
Hier sind die Ordner mit den entsprechenden Maps aufgelistet.
Es k�nnen beliebig Viele neue Ordner erstelt werden.
Der Aufbau sieht so aus:

[<OrdnerName>]
1=<Bank>.<map>
2=<Bank>.<map>
3=<Bank>.<map>
4=<Bank>.<map>
5=<Bank>.<map>
...

Beispiel:
[0]
1=0.0
2=0.1
3=0.2
...

[1]
1=1.0
...

Die Ordnernamen d�rfen frei ge�ndert werden;

Es gibt Ausnahmen in diesem Aufbau:
[<OrdnerName>]
1=<Frei w�hlbare Bezeihnung>
2=<Frei w�hlbare Bezeihnung>
...
Genaueres dazu unter Maps.ini


Maps.ini
--------
Hier sind die Maps aufgelistet, es erscheinen nur die,
welche in der liste der Ordner vorkommen.
[<Bank>.<map>]
Name=<Beschriftung>

[0.0]
Name=PETALBURG CITY

[1.0]
Name=Route 101

Wichtig:
Hier sollte man nur die 'Name'- Eigenschaft �ndern.
Die Namensgebung des Eintrages "[0.0]" bezieht sich auf die Position im Mapheader,
wird dies ge�ndert, funktionieren diese Maps nicht mehr!

Die Ausnahmen:
Hier muss f�r ALLE Spielversionw, in allen Sprachen der Genaue Offset der Daten (MapFooder) angegeben werden.
Bei denen welchen Kein Offset angegeben wird, kann die map nicht geladen werden.

[<Frei w�hlbare Bezeihnung aus der Main.ini>]
Name=<Beschriftung>
<Genaue Spielbezeichnung>=<Offset>


Beispiel:
[UNKNOWN45] 
POKEMON SAPPAXPD=$2CA960 
name=Insel?


Tilesets.ini
------------
Die Tileset-Bilder werden ab der ver 1.30 aus dem spiel geladen.
Optional kann hier zu jedem Tileset(erstes Tileset ist 0) stehen wie viele Blocks es hat "Blocks=$90".
Es werden dann auch nur soviele Bl�cke aus dem Spiel geladen, das spart Arbeitsspeicher.
Wenn sich ein Tileset im oberen Teil befindet, hat es automatisch $200 Bl�cke(bzw. $280 in fr/lg).

[1]
Blocks=$90

...

[24]
Blocks=$87


Sprachen.ini
------------
Darin sind alle Sprachen aufgelistet, die zur verf�gung stehen.
Beispiel:
[Sprachen]
1=Deutsch
2=English

Im UnterOrdner "Ini/Sprachen" hat es dann eine <Sprachbezeichnung>.ini-Datei, in welcher die Texte stehen.
Es k�nnen beliebig viele andere Sprachen hinzugef�gt werden, beachten sie aber den "EndNutzer Vertrag".
Der "EndNutzer Vertrag" muss auch �bersetzt werden und aschliessend mir zugeschickt, damit ich ihn Codiert ablegen kann.
Bevor ich dies getan habe, ich die Sprache nicht verf�gbar....
Die Sprache ist unter "Einstellungen"->"Sprache" ausw�hlbar.

Die Sprache die bei Ihnen Verwendet wird, k�nnen Sie beim ersten start von AdvanceMap festlegen.

Die Dateien GehDaten.ini/AufgabenDaten.ini und andere wurden direkt in die Neue Sprachen ini's integriert.


*********************************************
***    AdvanceMapError Berschreibungen    ***
*********************************************

AdvanceMapError(1): Try to read at pos 0! Please contakt luhopoke@gmail.com
Er versucht an Position 0 im Rom daten zu lesen. (-> nicht erlaubt)

AdvanceMapError(2): Cannot read bytes behind end of file! Please contakt luhopoke@gmail.com
Er versucht nach dem Dateiende im Rom daten zu lesen. (-> nicht m�glich)

AdvanceMapError(3): Cannot change bytes at pos 0! Please contakt luhopoke@gmail.com
Er versucht an Position 0 daten ins rom zu schreiben. (-> nicht erlaubt)

AdvanceMapError(4): Cannot change bytes behind end of file! Please contakt luhopoke@gmail.com
Er versucht nach dem Dateiende ins rom zu schreiben. (-> nicht m�glich)

AdvanceMapError(5): The value at $XXXXXX is not a Pointer! Please contakt luhopoke@gmail.com
Der Wert am angegebenen Offset sollte ein Pointer sein, ist es aber nicht. (-> fehlerhafte Daten)

AdvanceMapError(6): Try to read more than 1023 Bytes a time! Please contakt luhopoke@gmail.com
Er versucht mit einer Speziellen Funktion mehr als 1023 Bytes zu lesen, das ist mit der funktion aber nicht m�glich. (-> Bug in AdvanceMap)

AdvanceMapError(7): Try to save more than 1023 Bytes a time! Please contakt luhopoke@gmail.com
Er versucht mit einer Speziellen Funktion mehr als 1023 Bytes zu Schreiben, das ist mit der funktion aber nicht m�glich. (-> Bug in AdvanceMap)

AdvanceMapError(8): Cannot read XX Bytes in a Array with the size of YY! Have read as much as possible. Please contakt luhopoke@gmail.com
Er versucht Count Bytes in ein Array zu laden das nur anz gross ist.  (-> Bug in AdvanceMap)

AdvanceMapError(9): Pleace Extract the gba file from your zip/rar archive and open the gba file.
Der Benutzer versucht eine zip oder rar datei zu �ffnen. Das geht aber nicht. Der Benutzer wird aufgefordert die gba datei zu entpacken. (-> Benutzer macht was falsch^^)

AdvanceMapError(10): Cannot handle more then 60 MapNumbers per WorldMap. Please contakt luhopoke@gmail.com
Fehler im Weltkarten editor. F�r die noch inaktive Funktion "Weltkarten-Nr. zuordnen" (bei fr/lg). (-> wenn die bei jemandem Auftritt, muss ich der Weltkarten Edi etwas umprograammieren. Das sollte aber nicht geschehen^^)

AdvanceMapError(11): The File could not be open.
Wenn die Datei zum importieren von Daten nicht ge�ffnet werden kann.

AdvanceMapError(12): Unknown Rom Type! This Rom cannot be edited with Advancemap.
Die ge�ffnete Rom Datei ist kein unterst�tztes Spiel. Es k�nnen nur die Pokemon Spiele der Advance Generation bearbeitet werden.


*********************************************
***          Gr�sse/Danksagungen          ***
*********************************************
Der gr�sste Dank geht an:
BlueSonic(alias Jigglypuff) f�r den Source von Goldmap2 Beta
und Jay, der ihn �bermittelt hat.

Weitere gr�sse gehen an:
Tauwasser und F-Zero f�r Ihre Tuts.
Mikaron f�r seine Dienste.
Serwe der mich auf ein paar Ideen gebracht hat.
Mulle die mich auf einen Feher hinwies.
Scizz, Timhay, GruntZ, Ashly138, Usohachi, BlueSonic, Sylph, Liquid_Thunder, IIIMQIII, Netto-kun f�r die �bersetzungen der ini's.
Und nat�rlich Filb f�r sein Board.
Ein Weiterer Dank geht an F-Zero der mir bei den Paletten f�r die Sprites sehr geholfen hat.
Auch an dark01 geht f�r seine hilfe bei den Sprites einen grossen Dank.
An evilboy geht ein Dank f�r die Hilfe bei den FAQ's.
Nochmals ein dank geht an Scizz, dark01, BlueSonic und F-Zero f�r die Betatests.
Aruka und perappu f�r die Musiklisten Erweiterungen.
Ein grosser Dank geht an Mastermind_X welcher den Aufbau der Weltkarten Daten rausgefunden hat und mir bei der Umsetzung geholfen hat.
Einen grossen Dank an Tutti f�r seine super Betatest-Leistung und die Erweiterung der Verhaltensbyteliste.
Tauwasser, Scizz, Satry, Ashly138, Anthony, wakachamo, HackMew, Christos, Martin�, Sebbe17/Jungleman, 44tim44 f�r die neuen �bersetzungen der ini's.