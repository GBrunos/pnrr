---
hide:
  - navigation
---



# Costruire un catalogo dei procedimenti amministrativi

!!! info inline end

    :man_raising_hand: Per le schede [**metadati**](https://uo-transizionedigitalecomunepalermo.github.io/mappatura-procedimenti-amministrativi/contenuti/schema-metadati/) e [**fasi operative**](https://uo-transizionedigitalecomunepalermo.github.io/mappatura-procedimenti-amministrativi/contenuti/fasi-operative/) dei procedimenti, fai riferimento alle relative pagine trattate in questo progetto di documentazione :octicons-link-external-16:

Conclusa la compilazione delle schede (**metadati** + **fasi operative**) da parte dei responsabili dei procedimenti, un ufficio centrale dell'Amministrazione provvede a 

- collezionare 
- e verificare 

i contenuti di tutte le schede tabellari. 

Viene creato una cartella su Google Drive che raccoglie tutte le schede compilate dal personale degli uffici. Successivamente si crea un `database` (sempre in formato excel su Googel Drive) che elenca tutte le schede dei procedimenti. Il `database` rappresenta la fonte dati che genererà l'interfaccia grafica del `catalogo` dei procedimenti.

:material-database-check-outline: Questa è una fase importante in quanto dal database realizzato si accederà ai dati nel dettaglio di tutti i procedimenti. 



## Aggiornamento periodico delle schede ("versionamento") :octicons-versions-16:
Un attività di fondamentale importanza è rappresentata dalla validazione delle schede nel tempo da parte dei responsabili dei procedimenti e dai dirigenti. Le norme cambiano e anche le procedure operative per la gestione dei procedimenti possono cambiare, è necessario, quindi, tenere traccia di eventuali cambiamenti.

I responsabili di procedimento e i dirigenti dovrebbero provvedere alla validazione dei contenuti delle schede dei procedimenti di competenza (dopo la prima versione), almeno con la seguente cadenza temporale:

!!! Note ""
    :exclamation: **semestrale** ed in concomitanza con le scadenze degli obiettivi di Unità Organizzative e dirigenziali, se nessuna nuova norma interviene a modificare le fasi di gestione del procedimento amministrativo. In questo caso se nessuna modifica viene ritenuta necessaria da apportare alla modalità di gestione e dei metadati, si conferma e valida il contenuto delle schede compilate il semestre precedente;

!!! Note ""
    :exclamation: **nel momento preciso in cui una nuova norma interviene** a modificare le fasi di gestione e/o i metadati del procedimento amministrativo. Si pensi, ad esempio, al cambio di ufficio che gestisce un procedimento, alla modifica di telefono/email/pec o alla modifica della modalità di pagamento.


Nei casi di modifica delle schede nei semestri successivi alla data di redazione della prima versione delle schede (metadati e fasi operative) è necessario aggiungere un record "data_versione_scheda" sia alla scheda "**fasi operative**" che alla scheda "**metadati**", in maniera tale da avere sempre definita la data di riferimento a partire dalla quale vigono le informazioni riportate nelle stesse schede. Il campo riportante la "data di versionamento" sarà il primo in ambedue le schede.


:material-file-document-multiple-outline: ==**fasi operative**== ↓

| <kbd>Ordine progressivo delle fasi del procedimento</kbd> | <kbd>Breve descrizione puntuale delle attività svolte, per fase, dal personale per gestire il procedimento amministrativo</kbd> | <kbd>Note che si ritengono utili inserire per illustrare al meglio le varie fasi del procedimento amministrativo. Utile a descrivere eventuali sotto-azioni necessarie al perfezionamento del procedimento amministrativo</kbd> |
|:-----|:-----|:-----|
| **`data_versione_scheda`** | 30/06/2021 | *la versione del 30/06/2021 è stata redatta al fine di recepire le indicazioni della legge n... del .... che ha introddoto alcune modifiche sulla gestione del procedimento e del relativo servizio all'utenza* |
| fase 1 | .............. | ........... |
| fase 2 | .............. | ........... |
| fase 3 | .............. | ........... |


:material-file-document-multiple-outline: ==**metadati**== ↓

| <kbd>ID metadato</kbd> | <kbd>Denominazione del metadato</kbd> | <kbd>Contenuto del metadato</kbd> |  <kbd>Note aggiuntive</kbd>  |
|:---|:--------------------------------------|:-----------------|:-----|
|**`versione`**| **`data_versione_scheda`**| 30/06/2021 | *la versione del 30/06/2021 è stata redatta al fine di recepire le indicazioni della legge 1234/2021 che ha introddoto alcune modifiche sulla gestione del procedimento ........ e del relativo servizio all'utenza* |
|1| Nome del procedimento amministrativo | ACQUISIZIONE DEL SERVIZIO DI REFEZIONE SCOLASTICA E DEL SERVIZIO DI FORMAZIONE ALIMENTARISTI |    |
|2|Descrizione del procedimento amministrativo | Autorizzazione alla fruizione ai dipendenti afferenti il Settore dei benefici L. 104/1992 |   |
|3|Nome dell'Area comunale competente|Area della Cittadinanza|  |
|4|Nome del Settore comunale competente e del Servizio Se non è previsto il Settore scrivere il nome del Servizio di appartenenza| Settore della Cittadinanza solidale- Staff responsabile di Settore|  |
|5| ..... | ..... | ...... |

Le informazioni di "versionamento" delle schede sono necessarie al fine di apportare le eventuali modifiche future all'applicativo informatico per la gestione dei procedimenti e anche per tenere traccia delle variazioni dei contenuti delle schede nel tempo.




## Creare un database con l'elenco dei procedimenti
Un ufficio centrale dell'Amministrazione procede con la creazione di un file in formato tabellare su Google Drive, in apposita cartella. 

Il file contiene i principali metadati relativi ai procedimenti:

- <kbd>denominazione procedimento</kbd> <small>(descrizione sintetica)</small>
- <kbd>nome_cognome del responsabile</kbd>
- <kbd>email responsabile</kbd>
- <kbd>telefono responsabile</kbd>
- <kbd>servizio/ufficio responsabile</kbd>
- <kbd>informazione che permette di capire se il procedimento è gestibile in "lavoro agile"</kbd> <small>(utile per la costruzione del POLA)</small>
- <kbd>numero progressivo identificativo del procedimento amministrativo in un database</kbd>
- <kbd>link URL alla scheda excel su Google Drive che contiene la scheda "metadati" e la scheda "fasi operative"</kbd>  <small>(deve essere un URL)</small>

Il database ha il seguente ==**schema dati**==:

|<kbd>area</kbd>|<kbd>settore</kbd>|<kbd>servizio</kbd>|<kbd>denominaz. procedimento</kbd>|<kbd>lavoro agile</kbd>|<kbd>email resp.procedimento</kbd>|<kbd>telefono info</kbd>|<kbd>link scheda</kbd>|<kbd>rif</kbd>|
|----|-------|--------|--------------------------|------------|-------------------------------|-------------|-----------|---|
|Decoro Urbano e Verde|                          |Capo Area / Responsabile del Verde Urbano|Risposta scritta interrogazione consiliare|si|nomecognome @comune.palermo.it|0917401111|[link](https://docs.google.com/spreadsheets/d/1qJ8iUDgwPxVebEOCjFFR-gKIWO5ro2hd/edit#gid=371520549)|1|
|Educazione Formazione e Politiche Giovanili| | staff Capo Area| Erogazione contributi  previsti dal D.Lgs n. 65 del 13.04.2017  (0-6 anni) | si | nomecognome @comune.palermo.it | 0917401111 - 0917401112 | [link](https://docs.google.com/spreadsheets/d/1xbGxiY8iYK2-k39EyPV_coAf7R4TrVuDd8SUmL9fGNs/edit#gid=1298047631)|2|

Dall'elenco dei procedimenti con il relativo link alle singole schede (compilate dai responsabili del procedimento), come passo successivo, si procede a creare un catalogo che permetta la consultazione online facile, con possibilità di effettuare ricerche multicriterio. 

!!! Note "Importante"
    **Il catalogo con la mappatura e le schede di analisi dei procedimenti può diventare un allegato del capitolato speciale di appalto che la PA può fornire alle aziende che parteciperanno alla fornitura del software per la digitalizzazione dei procedimenti dell'ente pubblico**. 
    
    :exclamation: In questo modo la PA ha svolto un lavoro importante e necessario affinchè le software house possano costruire e fornire un applicativo ideoneo a soddisfare al meglio i bisogni di digitalizzazione per la gestione dei procedimenti della PA.


---

## Creare un interfaccia grafica con GitHub :fontawesome-brands-github: per il catalogo online 
Attraverso un [**progetto di codice ospitato sulla piattaforma GitHub**](https://github.com/UO-TransizioneDigitaleComunePalermo/procedimenti-amministrativi-comunepalermo) è possibile creare un interfaccia di catalogo molto intuitiva per la consultazione online.

[![](https://user-images.githubusercontent.com/42996217/141148955-34ca8068-dc79-47ab-b341-2fa1e9f35ff1.png)](https://github.com/UO-TransizioneDigitaleComunePalermo/procedimenti-amministrativi-comunepalermo)

[**`GitHub`**](https://github.com/) è un servizio online gratuito di hosting per progetti software. E' la stessa piattaforma che viene utilizzata da [AGID e Dipartimento Trasformazione Digitale](https://github.com/italia/) per la conservazione e messa a disposizione pubblica online, del codice sorgente sorgente delle soluzioni informatiche realizzate per l'attuazione del Codice dell'Amministrazione Digitale.



### Usare il file excel Google Drive :material-google-drive: come fonte dati per il progetto su GitHub :fontawesome-brands-github:
:octicons-share-android-24: Il file creato precedentemente in formato tabellare su Google Drive con l'elenco dei procedimenti e i link alle schede di dettaglio, viene reso condivisibile (nelle impostazioni) in maniera tale che *chiunque navighi su internet e abbia questo link può visualizzare questo elemento*.

![](https://user-images.githubusercontent.com/42996217/141465351-5d7ec9f7-bfb3-408f-985b-d5f7f1aa290b.png)

Sul progetto da creare su GitHub si fa riferimento al link del foglio excel di Google Drive, specificatamente nel file **`index.html`** bisogna dare le seguenti istruzioni:
```
<link rel="exhibit/data" 
    type="text/csv"
    href="https://docs.google.com/spreadsheets/d/e/2PACX-1vQfrJ2qTTIIkX5Pf0Q4dxijhIA9R3XtocGEvhPsNA3Hd-OnhTgkYEqNJltvVeTdQrsXAsnrDX2_09lK/pub?output=csv" />
```
L'URL `https://docs.google.com/spreadsheets/d/e/2PACX-1vQfrJ2qTTIIkX5Pf0Q4dxijhIA9R3XtocGEvhPsNA3Hd-OnhTgkYEqNJltvVeTdQrsXAsnrDX2_09lK/pub?output=csv` è la fonte dati da cui il progetto GitHub genera l'interfaccia web di consultazione dei procedimenti amministrativi.

<br>

### Clonare il progetto esistente come modello da replicare per un nuovo catalogo :octicons-repo-clone-16:
La realizzazione del progetto su GitHub è possibile clonando il [**progetto già realizzato**](https://github.com/UO-TransizioneDigitaleComunePalermo/procedimenti-amministrativi-comunepalermo), e dando un nuovo titolo nella sezione "**Repository Name**" ↓

![clona il repository GitHub](https://user-images.githubusercontent.com/42996217/141466142-53cf9edb-6b6b-4df3-8795-ac6da2da9b0f.png)


### Codice sorgente open source :material-open-source-initiative:
Il codice sorgente per il progetto realizzato su GitHub è ["**open source**"](https://it.wikipedia.org/wiki/Open_source) ed è rilasciato con licenza aperta che ne permette il riutilizzo gratuito (licenza [CC BY SA](https://creativecommons.org/licenses/by-sa/4.0/deed.it)).


---

<br>

## Presentazione del catalogo :octicons-device-desktop-24:
Presentazione del [**catalogo dei procedimenti amministrativi del Comune di Palermo**](https://uo-transizionedigitalecomunepalermo.github.io/procedimenti-amministrativi-comunepalermo/) come strumento di conoscenza per il personale della PA, per i cittadini e per la costruzione della piattaforma digitale di gestione dei procedimenti.

[![](https://user-images.githubusercontent.com/42996217/141728854-f2e11070-85e4-4afc-a075-229beed21f34.png)](https://uo-transizionedigitalecomunepalermo.github.io/procedimenti-amministrativi-comunepalermo/)


