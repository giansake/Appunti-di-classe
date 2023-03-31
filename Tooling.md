# Tooling

> 1. Come posso configurare VSCode per aiutarmi nella stesura di HTML e CSS?    
> Quali pacchetti posso installare e come si installano in VSCode?  
> Cos'è un formatter?   
> Come imposto un formatter di default e come faccio a formattare il mio codice al salvataggio?
> 2. Come faccio a scrivere un commento in HTML?
>

## Visual Studio Code
### *L'editor di codice del corso*


[Visual Studio Code](https://code.visualstudio.com/)    
3 motivi per usare Visual Studio Code e non Sublime Text o Atom o Notepad, ecc ecc
    
- **Gratuito**
- Ampio ecosistema di pacchetti (plugin) per funzionalità aggiuntive o per la configurazione personalizzata dell'ambiente di lavoro
- Utile e funzionale con i diversi linguaggi di programmazione del web: HTML, CSS, JavaScript, PHP ecc ecc
    
## Come posso configurare VSCode per aiutarmi nella stesura di HTML e CSS?

Nella seconda lezione abbiamo installato VSCode e configurato gli strumenti minimi per assisterci nella corretta stesura di codice. 
Di seguito un recap di quanto fatto:

- [Installa VSCode scaricandolo qui](https://code.visualstudio.com/download) \
  Il Visual Studio Code a cui si fa riferimento qui è quello con l'icona **blu** e non con l'icona rosa
- Individuiamo le sezioni fondamentali del programma
  - File explorer (sidebar sulla sinistra)
  - Toolbar in basso, per la selezione del linguaggio e quindi della sintassi
  - Settings (icona dell'ingranaggio in basso a sinistra), per l impostazione dell'autoformatter ecc ecc
- Creaimo il primo file HTML, file > nuovo > seleziona il linguaggio html dalla toolbar in basso OPPURE salva il file assegnando l'estensione html, ad esempio: miofile.**html**\
In questo modo l'editor imposterà automaticamente il linguaggio corretto e quindi la giusta evidenziazione della sintassi.
- Siccome Visual Studio Code include già alcuni strumenti di supporto alla scrittura di codice ci basterà digitare un punto esclamativo nel file html che abbiamo appena creato, per ricevere un **_suggerimento emmet_** con lo snippet del codice html di base per disegnare una pagina. Alla comparsa del suggerimento, premete invio.
![Emmet](emmet.png "L'abbreviazione emmet più importante") 
Come si nota dall'immagine, lo snippet emmet ci restituirà l'HTML di base necessario per una pagina html. 
Una volta accettato il suggerimento di emmet, potremo inziare a disegnare la nostra pagina.
    
    Emmet sarà anche responsabile per l'autocompilazione del codice, ovvero ci suggerirà la corretta sintassi per i tag che scriviamo, mentre li stiamo scrivendo! 

    ![Emmet](emmet1.png "L'abbreviazione emmet più importante")\
    appena inizieremo a scrivere un tag html ci verrà suggerito uno snippet emmet, basterà premere invio per applicarlo al nostro codice, come nell'immagine successiva 
    ![Emmet](emmet2.png "L'abbreviazione emmet più importante")\
    Vi consiglio di andare subito a capo, cosi da farvi spazio per inserire il vostro contenuto seza rischiare di compromettere la sintassi. 

    **Cosi OK** \
    ![Emmet](emmet3.png "L'abbreviazione emmet più importante")\
     **Cosi NO** \
    ![Emmet](emmet4.png "L'abbreviazione emmet più importante")

    Ad ogni modo non preoccupatevi troppo di questo perché se avrete correttamente configurato l'autoformatter, come illustrato nei punti successivi, sarà lui ad occuparsi dello stile del vostro codice ogni volta che salverete.
    

- Personalmente, vi consiglio di installare il pacchetto [Prettier](https://prettier.io/) per la formattazione del codice. 
Nonostante VSCode disponga di default dei formatter necessari per HTML e CSS vi consiglio di installare il plugin Prettier dalla seziona Packages di VSCode.
Una volta attivato prettier potrete impostarlo come formatter di default seguendo i passaggi riportati qua sotto
    - Tasto destro sul file che volete formattare, in questo caso il file html
    ![Format](formatWith.png "Formatta il documento") 
    Al click sul semplice "Format Document" eseguirete una formattazione una-tantum e quindi non automatica al salvataggio. Per impostare la formattazione automatica procedete con **Format Document With**
    ![Imposta il formatter di default](setDefaultFormatter.png "Default Formatter") 
    Procedete con **Configure Default Formatter** e selezionate Prettier. 
    Perfetto!
    Ora dovete solo dire a VSCode di formattare il vostro codice ogni volta che salvate.
    Per farlo raggiungete la sezione Settings di VSCode, potete raggiungerla da *preferenze > settings* oppure dall'icona dell'ingranaggio in basso a sinistra nella sidebar.
    Una volta in settings vi consiglio di usare la barra di ricerca testuale per filtrare tra le impostazioni.
    ![Formatta al salvataggio](formatOnSave.png "Formatta al salvataggio") 
    Accertatevi che la checkbox sia spuntata e quindi attiva.
    Di seguito un articolo sul [perché usare un formatter di codice](https://medium.com/@ryconoclast/why-you-should-use-a-code-formatter-4f02dd40db14)


## NB: Il formatter ci indicherà anche gli eventuali errori nel codice

Assicuratevi che: 
- Prettier è il formatter di default per HTML e CSS
- Che la formattazione è correttamente configurata per essere applicata ad ogni salvataggio

Se saranno soddisfatte queste due condizioni allora potrete contare su Prettier anche per validare il vostro codice. 

Vi mostro un esempio:

Nel seguente codice c'è un errore, lo vedete?
![Codice con errore](error.png "Codice con erroe") 
Che lo vediate o no, Prettier è certo che ci sia un erroe. Come ci indica il box rosso in basso a destra, nella toolbar di VSCode. 
![Validazione di Prettier](errorPrettier.png "Codice con erroe") 
Al click sul box rosso Visual Studio ci mostra i log di Prettier. Un log è un documento di testo dove un determinato processo scrive ogni singola azione che compie. I log sono documenti usati per comprendere a quale punto e durante quale operazione un determinato processo è andato in errore. 
Nell'immagine seguente parte del log di Prettier per l'errore in questione.
![Log difficile da leggere](prettierLog.png "Log difficile da leggere") 

Poco prima di questo testo poco amichevole, troveremo una spiegazione un pò più umana dell'errore che Prettier ha individuato. Vi invito a cercare sempre una rappresentazione simile, senza fermarvi alle incomprensibili righe di testo dell'immagine precedente.
![Log utile e chiaro](prettierLogUseful.png "Log utile e chiaro")
Questo tipo di informazioni vi aiuterà a circoscrivere la parte di codice in cui è presente l'errore. In questo caso Prettier mi sta indicando che nel div che chiudo alla riga 6 c'è qualcosa che non va.

Di seguito, l'immagine del codice risolto e quindi dell'errore corretto. L'avevate scovato anche senza Prettier?\
![Codice corretto](errorResolved.png "Codice corretto") 


