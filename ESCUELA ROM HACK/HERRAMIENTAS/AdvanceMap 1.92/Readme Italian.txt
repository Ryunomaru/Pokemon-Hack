********************************************
***     Advance Map v1.92 - Italiano     ***
********************************************
Questo programma consenta la modifiche delle mappe, dei permessi, dei blocchi, degli eventi e dei Pok�mon selvatici.
AM funziona con tutte le ROM della serie Advance, tutte le lingue.
Ora � possibile anche cambiare le informazioni relative la mappa del mondo.


!!!Attenzione!!!
-------------
Con questa versione tutte le modifiche sono salvata direttamente sulla ROM!
Utilizzando "Salva con nome" puoi salvarle su un altro file.
Tutte le modifiche successive saranno quindi salvate sul nuovo file.


.:|IMPORTANTE|:.
-^-^-^-^-^-^-
Questo programma � stato programmato da LU-HO ed � soggetto ai diritti d'autore di LU-HO Pok�!
Advance Map deriva dalla versione beta di GoldMap 2, creata da Jiggly.
Se non hai scaricato il file da http://am160.no-ip.info, FWB(Filb's World Board), www.LU-HO.ch.vu, ampage.no-ip.info oppure da
www.romhackersworld.de.vu contattami al pi� presto! La mia mail �: luhopoke@gmail.com


*********************************************
***        Combinazioni di tasti          ***
*********************************************
In ogni menu sono visibili le combinazioni di tasti corrispondenti, se disponibili.
Vedio le differenti possibilit� durante la modifiche delle mappe.

Vista mappa:
-------------
Tasto sinistro del mouse		=> Posiziona il blocco attuale sulla mappa.
Tasto centrale del mouse		=> Sostituisce tutti i blocchi contigui a quello selezionato con quello attuale.
Tasto destro del mouse			=> Il blocco selezionato diventa quello attuale.

Ctrl + Tasto sinistro del mouse		=> Niente di speciale, posiziona il blocco attuale sulla mappa.
Ctrl + Tasto centrale del mouse		=> Sostituisce tutti i blocchi simili (anche non contigui) a quello selezionato con quello attuale.
Ctrl + Tasto destro del mouse		=> Permette di scegliere e posizionare pi� blocchi alla volta.


Vista mappa (tavolozza bocchi):
--------------------------------
Tasto sinistro del mouse		=> Il blocco selezionato diventa quello attuale.


Vista movimenti permessi:
--------------------------
Tasto sinistro del mouse		=> Posiziona il blocco attuale sulla mappa.
Tasto centrale del mouse		=> Sostituisce tutti i blocchi contigui a quello selezionato con quello attuale.
Tasto destro del mouse			=> Il blocco selezionato diventa quello attuale.

Ctrl + Tasto sinistro del mouse		=> Posiziona il blocco attuale sulla mappa.
Ctrl + Tasto centrale del mouse		=> Sostituisce tutti i blocchi contigui a quello selezionato con quello attuale.
Ctrl + Tasto destro del mouse		=> Il blocco selezionato diventa quello attuale.


Vista movimenti permessi (tavolozza):
--------------------------------------
Tasto sinistro del mouse		=> Il blocco selezionato diventa quello attuale.
Tasto centrale del mouse		=> Il blocco selezionato diventa quello attuale.
Tasto destro del mouse			=> Il blocco selezionato diventa quello attuale.

Ctrl + Tasto sinistro del mouse		=> Il blocco selezionato diventa quello attuale.
Ctrl + Tasto centrale del mouse		=> Il blocco selezionato diventa quello attuale.
Ctrl + Tasto destro del mouse		=> Il blocco selezionato diventa quello attuale.


Vista eventi:
--------------
Tasto sinistro del mouse 		=> Seleziona/sposta l'evento di posizione superiore.
Tasto centrale del mouse		=> Seleziona l'evento di posizione superiore (nessun movimento).
Tasto destro del mouse			=> Seleziona/sposta l'evento di posizione inferiore.

Ctrl + Tasto sinistro del mouse		=> Seleziona/sposta l'evento di posizione superiore.
Ctrl + Tasto centrale del mouse		=> Seleziona l'evento di posizione superiore (nessun movimento).
Ctrl + Tasto destro del mouse		=> Seleziona/sposta l'evento di posizione inferiore.

Doppio click sinistro			=> Seleziona l'evento di posizione superiore e lo apre con l'editor di script.
Doppio click centrale			=> Seleziona l'evento di posizione superiore e lo apre con l'editor di script.
Doppio click destro			=> Seleziona l'evento di posizione inferiore e lo apre con l'editor di script.


********************************
***   Contenuto degli INI    ***
********************************
AdvanceMap.ini:
--------------- 
L'INI � stato completamente riscritto.
Ora ogni linguaggio ha le sue impostazioni specifiche.
Ogni gioco, inoltre, ha impostazioni apposite.
Infine ogni offset � immagazzinato secondo un pattern.

Esempio:
[MapBankHeader]
art=pointer
nach=80180068890B091808687047
spiele=BPR,BPG,BPE,AXP,AXV

Questo indica che i byte dopo "nach" rappresentano il pointer dell'header mappa.
Queste impostazioni sono uguali per tutti i giochi e sono presenti sotto la lista "spiele".


Esempio 2:
[PokemonNamen]
inkSprache=1
art=pointer
vor=30B50025084CC8F7
spiele=AXPJ,AXVJ,AXPE,AXVE

[PokemonNamen2]
art=pointer
position=$000144
spiele=BPR,BPG,BPE,AXP,AXV

Qui ci sono due parti. La prima, tutti i parametri dei linguaggi sono sotto "spiele"- listing, perch� "inkSprache" � settato a 1.
Also we have the pointer to the at point "vor" described Bytes.
Dato che non tutti i giochi usano la prima parte, ce n'� una seconda universale.
Dopo la seconda parte, il pointer sar� trovato alla posizione impostata nella variabile "position".


I valori esadecimali devono sempre avere il "$"!


Main.ini
--------
Questo � l'ordine di come le mappe vengono listate.
Il formato � il seguente:

[<Foldername>]
1=<Bank>.<map>
2=<Bank>.<map>
3=<Bank>.<map>
4=<Bank>.<map>
5=<Bank>.<map>
...

Esempio:
[0]
1=0.0
2=0.1
3=0.2
...

[1]
1=1.0
...

I nomi delle cartelle possono essere cambiati a tuo piacimento.

Ci sono delle eccezioni:
[<FolderName>]
1=<Label>
2=<Label>
...

Per maggiori informazioni, vedi Maps.ini


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

Importante:
Qui dovresti modificare unicamente l'attributo "name".
La parte "[0.0]" si riferisce alla posizione dell'header mappa. Se alterato, la mappa potrebbe non funzionare pi�!
Gli offset non sono pi� usati in questa versione ma possono tranquillamente rimanere.

Eccezione:
Qui, per ogni gioco, l'offset del footer mappa deve essere esplicitamente dichiarato.


[<Nome da Main.ini>]
Name=<nome>
<nome esatto>=<Offset>


Esempio:
[UNKNOWN45] 
POKEMON SAPPAXPD=$2CA960 
name=Insel?


Tilesets.ini
------------
Questo file � stato rinnovato dalla versione 1.30.
Volendo puoi cambiare il numero di blocchi associato a ciascun tileset (il primo tileset � il numero 0).
Se il tileset � nella parte superiore avr� automaticamente 200 blocchi.

[1]
Blocks=$90

...

[24]
Blocks=$87


Sprachen.ini
------------
Qui c'� la lista di tutte le lingue disponibili.

Esempio:
[Sprachen]
1=Deutsch
2=English

Nella sottocartella "Ini/Sprachen" puoi trovare un file <nomelingua>.ini contenente le varie stringhe.
Puoi aggiungere quante lingue vuoi, ma devi curarti della "Licenza utente finale".
La "Licenza utente finale" deve essere tradotta, ed inviata a me in modo che la posso criptare.
Finch� non hai fatto ci�, la lingua non � disponibile...
La lingua pu� essere cambiata tramite "Impostazioni"->"Lingua".

Al primo avvio di AdvanceMap � possibile scegliere la lingua che preferisci.

File come GehDaten.ini/AufgabenDaten.ini ed altri sono stati inclusi nei nuovi file delle varie lingue.


*********************************************
***        Descrizione degli errori       ***
*********************************************

AdvanceMapError(1): Try to read at pos 0! Please contakt luhopoke@gmail.com
AdvanceMap ha tentato di leggere dei byte all'offset 0 della ROM. (-> vietato)
 
AdvanceMapError(2): Cannot read bytes behind end of file! Please contakt luhopoke@gmail.com
AdvanceMap ha tentato di leggere dei byte oltre la fine della ROM. (-> impossibile)
 
AdvanceMapError(3): Cannot change bytes at pos 0! Please contakt luhopoke@gmail.com
AdvanceMap ha tentato di scrivere dei byte all'offset 0 della ROM. (-> vietato)
 
AdvanceMapError(4): Cannot change bytes behind end of file! Please contakt luhopoke@gmail.com
AdvanceMap ha tentato di scrivere dei byte oltre la fine della ROM. (-> impossibile)

AdvanceMapError(5): The value at $XXXXXX is not a Pointer! Please contakt luhopoke@gmail.com
Il valore all'offset specificato dovrebbe essere un pointer, ma non lo �. (-> dati errati)
 
AdvanceMapError(6): Try to read more than 1023 Bytes a time! Please contakt luhopoke@gmail.com
AdvanceMap, tramite una funzione speciale, ha tentato di leggere pi� di 1023 byte. (-> bug in AdvanceMap)
 
AdvanceMapError(7): Try to save more than 1023 Bytes a time! Please contakt luhopoke@gmail.com
AdvanceMap, tramite una funzione speciale, ha tentato di scrivere pi� di 1023 byte. (-> bug in AdvanceMap)
 
AdvanceMapError(: Cannot read XX Bytes in a Array with the size of YY! Have read as much as possible. Please contakt luhopoke@gmail.com
AdvanceMap ha tentato di caricare un numero di byte superiore all'indice massimo dell'array. (-> bug in AdvanceMap)
 
AdvanceMapError(9): Pleace Extract the gba file from your zip/rar archive and open the gba file.
AdvanceMap non pu� leggere una ROM compressa in un archivio zip/rar in quanto va prima decompressa. (-> attenzione ^^)
 
AdvanceMapError(10): Cannot handle more then 60 MapNumbers per WorldMap. Please contakt luhopoke@gmail.com
Errore nell'editor della mappa del mondo, relativo alla funzione tuttora non attiva "Gestisci numeri mappa del mondo" (RF/VF).

AdvanceMapError(11): The File could not be open.
Impossibile aprire il file.
 
AdvanceMapError(12): Unknown Rom Type! This Rom cannot be edited with Advancemap.
La ROM aperta non corrisponde ad un gioco supportato. Solo le ROM Pok�mon della generazione Advance possono essere modificate con AdvanceMap.


*********************************
***      Ringraziamenti       ***
*********************************
Un grosso saluto va a:
BlueSonic(alias Jigglypuff) per la sorgente di Goldmap2 Beta
e Jay, che me l'ha fornita.

Ulteriori rigraziamenti:
Tauwasser e F-Zero per i loro tutorial.
Mikaron per il suo lavoro.
Serwe per qualche idea.
Mulle che mi ha segnalato un errore.
Scizz, Timhay, GruntZ, Ashly138, Usohachi, BlueSonic, Sylph, Liquid_Thunder, IIIMQIII, Netto-kun per la traduzione degli INI.
E naturalmente Filb per il suo forum.
Un altro ringraziamento a F-Zero per avermi aiutato con le palette degli sprite.
Stesso discorso per dark01 che mi ha aiutato con gli sprite.
evilboy per l'aiuto alle FAQ.
Ancora una volta grazie a Scizz, dark01, BlueSonic e F-Zero per il betatesting.
Aruka e perappu per la loro estensione della lista della musica.
Un enorme grazie a Mastermind_X che ha trovato il modo di modificare la mappa del mondo e che mi ha aiutato ad implementarne la funzione.
Un altro grazie a Tutti per le sue super prestazioni nel besta testing e per la lista del comportamento dei vari blocchi.
Infine un grazie a Tauwasser, Scizz, Satry, Ashly138, Anthony, wakachamo, HackMew, Christos, Martin�, Sebbe17/Jungleman, 44tim44 per le nuove traduzioni.