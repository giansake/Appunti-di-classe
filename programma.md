### Programma Web Design I NABA - 2ndo semestre 2023

#### 1. Documenti marcati - web 0.1

Comprendere quali esigenze hanno portato allo sviluppo del web e dei suoi linguaggi. Acquisire una prima comprensione di come questi linguaggi interagiscono tra loro e le diverse funzionalità specifiche che soddisfano

In questa prima fase si traccerà una traiettoria storica per illustrare la genesi dei tre linguaggi fondamentali per il web

- Client e Server
  **Acquisire un primo modello mentale di come funziona il web, con particolare attenzione alla parte front-end ovvero UI**

  - Il primo server al CERN
  - La browser war e la nascita dei browser
  - L'evoluzione della professione, da Webmaster a Developer

- La Struttura - Il linguaggio HTML
  **comprendere il ruolo _"limitato"_ del linguaggio HTML e come farne un uso consapevole**

  - Limitazioni e malintesi
  - Quale bisogno soddisfa, il suo sweet-spot
    - Digressione sul linguaggio Markdown

- Lo Stile - Il linguaggio CSS
  **Acquisire i rudimenti fondamentali per poter scrivere del codice sempre più previdibile**

  - Le componenti di una regola CSS
  - Sintassi e selettori

- L'Interattività - Il linguaggio JavaScript - web 2.0
  - un linguaggio per **eseguire** programmi nel browser
  - 2008 - il turning point per JS
  - Node js e la possibilità di usare JavaScript anche al di fuori del browser
  - Risorse: [JavaScript book](https://launchschool.com/books/javascript/read/introduction#briefhistory)

#### 2. Ambiente di sviluppo locale

**Un overview sugli strumenti necessari per una buona ergonomia nello sviluppo di prodotti web**

- L'editor di codice - Visual Studio Code

  - Cos'è un editor di codice, caratteristiche generali
  - Perché VSCode, pacchetti e plugin
  - Emmet e formatter (Prettier)
  - Live server
  - Shortcuts

- La console per sviluppatori del browser - Ispeziona elemento
  **Per questo corso e per la rinomata fama di browser sottosviluppato è altamente sconsigliato l'uso di Safari. Rimane disponibile come browser di testing per gli obbligatori fix di stile specifici di Safari**

  - [DOM, document object model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
    [Il Document Object Model (DOM)](https://web.dev/learn/html/overview/#element,-attributes,-and-javascript) è la rappresentazione dei dati della struttura e del contenuto del documento HTML. Quando il browser analizza l'HTML, crea un oggetto JavaScript per ogni elemento e sezione di testo incontrati. Questi oggetti sono chiamati, rispettivamente, nodi-elemento e nodi-testo.

    - Best practices: ispeziona, sorgente di pagina, regole css e struttura html

- Mindset

  - Ricerca continua
  - Ripetere per consolidare una memoria muscolare
  - Approccio spugna
    [The developer mindset](https://skillcrush.com/blog/the-developer-mindset/)

  ```
  Simplicity is the ultimate sophistication. 
  Leonardo da Vinci
  ```

  ```
  If you can’t explain something in simple terms, you don’t understand it. 
  Richard Feynman
  ```

  ```
  Perfect is the enemy of good.
  Voltaire
  ```

  Avere a che fare con la programmazione in generale è spesso percepito come difficile. In realtà non lo è. Tuttavia, richiede un temperamento particolare: pazienza, persistenza, concentrazione, logica, orientamento ai dettagli, ecc. Quando un programmatore comprende e adotta questo temperamento, il suo lavoro diventa meno frustrante, più divertente e gratificante.

  La percezione della difficoltà di un compito è spesso inversamente proporzionale alla pazienza della persona che lo svolge. Se siete pazienti con voi stessi e siete disposti a dedicare tempo agli esercizi e ad applicare i concetti, svilupperete presto il temperamento necessario. Prima di rendervi conto di ciò che sta accadendo, vi ritroverete a risolvere problemi con il codice.

  Per la maggior parte delle persone è necessario un cambiamento di mentalità. Questo avverrà con la pratica e con una certa analisi riflessiva che ognuno di noi applicherà nel momento di tradurre un'idea in codice. Una volta avvenuto, i vostri progressi accelereranno. Questo, a sua volta, vi aiuterà a sviluppare la capacità di pensare profondamente a qualsiasi problema. Troverete che la capacità di pensare profondamente ai problemi sia soddisfacente, coinvolgente e un vantaggio gratificante della programmazione!

  Vi invito ad approfondire sempre la vostra comprensione, del significato e del potenziale, delle idee che incontrerete durante il corso.
  È importante, nella fase iniziale, le prime ¾ lezioni, non farci abbattere e puntare a trovare subito un metodo di lavoro da affinare nel resto del corso.

  ```
  Everything takes longer than you think
  ```

#### 3. Approfondimento HTML

- Elementi dell'HTML

  L'HTML è costituito da una serie di elementi, che si usano per racchiudere, o avvolgere, diverse parti del contenuto per farlo apparire o agire in un certo modo.

  Gli elementi HTML sono delineati da tag, scritti con parentesi angolari `<` e `>`.

  Elementi e tag non sono la stessa cosa, anche se molti usano i termini in modo intercambiabile. **Il nome del tag** è il contenuto tra le parentesi. **Il tag include le parentesi**. In questo caso, `<h1>`. Un "**elemento**" è costituito dai tag di apertura e chiusura e da tutto il contenuto tra questi tag, **compresi gli elementi annidati**.

  I browser non visualizzano i tag. I tag vengono utilizzati per interpretare il contenuto della pagina

- Gli attributi di un Elemento HTML

  Gli attributi forniscono informazioni sull'elemento. Gli attributi, come il resto del tag di apertura, non appariranno nel contenuto, ma contribuiscono a definire come il contenuto apparirà agli utenti vedenti e non vedenti (tecnologie assistive e motori di ricerca).

  Gli attributi appaiono solo nel tag di apertura. Il tag di apertura inizia sempre con il tipo di elemento. Il tipo può essere seguito da zero o più attributi, separati da uno o più spazi. La maggior parte dei nomi degli attributi è seguita da un segno di uguaglianza che lo equipara al valore dell'attributo, avvolto da virgolette di apertura e chiusura.

- Struttura base di un documento HTML, [i tag necessari **sempre**](https://web.dev/learn/html/document-structure/#add-to-every-html-document)

- [Come connettere fogli stile (CSS)](https://web.dev/learn/html/document-structure/#css)

  Gli stili, tramite `<link>` o `<style>`, o entrambi, dovrebbero essere inseriti nell'intestazione. Funzioneranno anche se inclusi nel corpo del documento, ma gli stili vanno inseriti nell'intestazione per motivi di prestazioni. Questo può sembrare un controsenso, perché si potrebbe pensare di voler caricare prima il contenuto, ma in realtà si vuole che il browser sappia come rendere il contenuto quando viene caricato.

  L'aggiunta degli stili per prima (nella `<head>` del documento) evita l'inutile re-render che si verifica se un elemento viene stilizzato **dopo** che è stato renderizzato per la prima volta.

- [Il tag `<script>`](https://web.dev/learn/html/document-structure/#scripts)

  ```html
  <script>
    document.getElementById("switch").addEventListener("click", function () {
      document.body.classList.toggle("black");
    });
  </script>
  ```

  Questo frammento crea un gestore di eventi per un elemento con l'id di switch. In JavaScript, non si vuole fare riferimento a un elemento prima che esista. Non esiste ancora, quindi non lo includeremo ancora. Quando aggiungeremo l'elemento interruttore, aggiungeremo il `<script>` in fondo al `<body>` piuttosto che nel `<head>`.
  Perché? Per due motivi.

  Vogliamo assicurarci che gli elementi esistano prima che venga incontrato lo script che vi fa riferimento, poiché non stiamo basando questo script su un evento [DOMContentLoaded](https://developer.mozilla.org/en-US/docs/Web/API/Document/DOMContentLoaded_event). Inoltre, JavaScript non solo [blocca il rendering], ma il browser interrompe il download di tutte le risorse quando vengono scaricati gli script e non riprende il download di altre risorse finché non viene eseguito il JavaScript.

  Per questo motivo, spesso le richieste di JavaScript si trovano alla fine del documento piuttosto che in testa.

- Commenti in HTML
  Tutto ciò che è compreso tra `<!--` e `-->` non sarà visibile o analizzato.

- [Metadata in HTML](https://web.dev/learn/html/metadata/)

- HTML semantico

  Nel secondo blocco di codice, possiamo capire l'architettura anche senza capire il contenuto, perché gli elementi semantici forniscono significato e struttura. Si può dire che la prima intestazione è il banner del sito, con il `<h1>` che probabilmente è il nome del sito. Il footer è il piè di pagina del sito: le cinque parole possono essere una dichiarazione di copyright o l'indirizzo dell'azienda.

  Il markup semantico non si limita a rendere il markup più facile da leggere per gli sviluppatori; si tratta soprattutto di rendere il markup più facile da decifrare per gli strumenti automatici. Gli strumenti per gli sviluppatori dimostrano come gli elementi semantici forniscano anche una struttura leggibile dalla macchina.

  - [Accessibilità](https://web.dev/learn/html/semantic-html/#accessibility-object-model-aom)

  - L'attributo `role`

    L'attributo `role` descrive il ruolo che un elemento ha nel contesto del documento. L'attributo `role` è un attributo globale, cioè è valido su tutti gli elementi

    Gli elementi semantici hanno ciascuno un ruolo implicito, che dipende dal contesto. Come abbiamo visto nella schermata degli strumenti di sviluppo dell'accessibilità di Firefox, il livello superiore `<header>`, `<main>`, `<footer>` e `<nav>` erano tutti punti di riferimento (_landmarks_), mentre il `<header>` annidato in `<main>` era una sezione. La schermata di Chrome elenca i ruoli ARIA di questi elementi: `<main>` è il principale, `<nav>` è la navigazione e `<footer>`, essendo il piè di pagina del documento, è il contenuto informativo. Quando `<header>` è l'intestazione del documento, il ruolo predefinito è banner, che definisce la sezione come intestazione globale del sito. Quando un `<header>` o `<footer>` è annidato all'interno di un elemento di sezione, come `<section>` per esempio, non è un ruolo di riferimento (_landmarks_).

    Come usare l'attributo `role` su tag non semantici.

    ```html
    <div role="banner">
      <span role="heading" aria-level="1">Three words</span>
      <div role="navigation">
        <a>one word</a>
        <a>one word</a>
        <a>one word</a>
        <a>one word</a>
      </div>
    </div>
    ```

    Anche se l'attributo role può essere usato per aggiungere semantica a qualsiasi elemento, si dovrebbero usare elementi con il ruolo implicito di cui si ha bisogno.

- [Un panorama in continuo sviluppo: nuovi tag 2020 `<summary>` e `<details>`](https://web.dev/learn/html/details/)

---

L'HTML deve essere usato per strutturare il contenuto, non per definirne l'aspetto. L'aspetto è di competenza dei CSS. Sebbene alcuni elementi siano definiti per apparire in un certo modo, non utilizzate un elemento in base al modo in cui il foglio di stile dell'interprete lo fa apparire di default. Piuttosto, selezionate ogni elemento in base al suo significato semantico e alla sua funzionalità.
Scrivere HTML in modo logico, semantico e significativo aiuta a garantire che gli stili CSS siano applicati come previsto.

---

#### 4. Approfondimento CSS

- Box model

  Una cosa molto importante da ricordare quando si scrivono i CSS, o quando si lavora sul web nel suo complesso, è che tutto ciò che viene visualizzato dai CSS è un riquadro. Che si tratti di un riquadro che utilizza il raggio del bordo per assomigliare a un cerchio o anche solo di un testo, la cosa fondamentale da ricordare è che si tratta di riquadri.

  I riquadri hanno comportamenti diversi in base al loro valore di visualizzazione, alle dimensioni impostate e al contenuto che li contiene. Questo contenuto può essere costituito da altri riquadri, generati da elementi figli, o da semplice testo. In ogni caso, il contenuto influisce sulle dimensioni del riquadro per impostazione predefinita.

  È possibile controllare questo aspetto utilizzando il **dimensionamento estrinseco**, oppure continuare a lasciare che il browser decida per noi in base alle dimensioni del contenuto, utilizzando il **dimensionamento intrinseco**.

- Sintassi e selettori

  - [selettori semplici](https://web.dev/learn/html/details/): global, class, id e attribute
  - raggruppare selettori
  - [specificità](https://web.dev/learn/css/specificity/)

- Proprietà **fisiche** vs Proprietà **logiche**

  Le proprietà fisiche `top`, `right`, `bottom`, and `left` si riferiscono alle dimensioni fisiche della finestra di visualizzazione.
  Si può pensare a queste proprietà come a una rosa dei venti su una mappa. Le proprietà logiche, invece, si riferiscono ai bordi di un riquadro in relazione al flusso generale dei contenuti. Pertanto, possono cambiare se cambia la direzione del testo o la modalità di scrittura.
  Si tratta di un grande cambiamento rispetto agli stili direzionali e ci offre molta più flessibilità nella stilizzazione delle nostre interfacce.

- Display e positioning

  - [Block flow](https://web.dev/learn/css/logical-properties/#block-flow) vs [Inline flow](https://web.dev/learn/css/logical-properties/#inline-flow)
  - [la proprietà `display`](https://web.dev/learn/css/layout/#understanding-the-display-property)

    **Inline**
    Gli elementi inline si comportano come le parole in una frase. Siedono uno a fianco all'altro disposti nella direzione della riga. Elementi come `<span>` e `<strong>`, utilizzati tipicamente per formattare pezzi di testo all'interno di elemetni come `<p>` (paragrafo), sono inline di default. Conservano infatti gli spazi bianchi circostanti.
    Non può essere impostata una `width` o un `height` specifica per elementi con display: inline. Qualsiasi margine o padding applicato a livello di span o strong sarà ignorato dagli elementi circostanti.

    **block**
    Gli elementi a blocchi non si affiancano l'uno all'altro. Creano una nuova riga per se stessi. A meno che non venga modificato da altro codice CSS, un elemento di blocco si espande per tutta la larghezza della riga, quindi copre l'intera larghezza in una modalità di scrittura orizzontale. Margini e padding di un elemento block sono rispettati dagli elementi circostanti.

    **Flexbox** e **Grid**
    La proprietà display determina anche il comportamento dei figli di un elemento. Ad esempio, impostando la proprietà display su `display: flex`, il riquadro diventa un riquadro a livello di blocco e converte anche i suoi figli in elementi flex. Questo abilita le proprietà flex che controllano l'allineamento, l'ordinamento e il flusso.

    Esistono due meccanismi di layout principali che creano regole di layout per più elementi: flexbox e grid. Hanno in comune delle somiglianze, ma sono progettati per risolvere problemi di layout diversi.

    **Flexbox**
    Flexbox è un meccanismo di layout per layout monodimensionali. Si tratta di un layout su un singolo asse, sia in orizzontale che in verticale. Per impostazione predefinita, flexbox allinea i figli dell'elemento l'uno accanto all'altro, nella direzione inline, e li allunga nella direzione del blocco, in modo che abbiano tutti la stessa altezza.

    Gli oggetti rimarranno sullo stesso asse e non si avvolgeranno quando finiscono lo spazio. Cercheranno invece di schiacciarsi l'uno sull'altro sulla stessa linea. Questo comportamento può essere modificato utilizzando le proprietà `align-items`, `justify-content` e `flex-wrap`.

    Flexbox also converts the child elements to be **_flex items_**, which means you can write rules on how they behave inside a flex container. You can change alignment, order and justification on an individual item. You can also change how it shrinks or grows using the `flex` property.

    **Grid**
    La griglia è simile per molti aspetti a flexbox, ma è progettata per controllare layout multiassiali invece di layout monoassiali (spazio verticale o orizzontale).

    Grid consente di scrivere regole di layout su un elemento con display: grid e introduce alcune nuove primitive per lo styling del layout, come le funzioni repeat() e minmax(). Un'unità di griglia utile è l'unità fr, che è una frazione dello spazio rimanente. È possibile costruire griglie tradizionali a 12 colonne, con uno spazio tra ogni elemento, con 3 proprietà CSS:

    ```css
    .my-element {
      display: grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 1rem;
    }
    ```

  - [Position](https://web.dev/learn/css/layout/#positioning)

    L'ultimo punto di questa panoramica sui meccanismi di layout è il posizionamento. La proprietà position modifica il comportamento di un elemento nel normale flusso del documento e il suo rapporto con gli altri elementi. Le opzioni disponibili sono `relative`, `absolute`, `fixed` e `sticky`, mentre il valore predefinito è `static`.

    **L'aggiunta di** `position: relative` **a un elemento lo rende anche il blocco contenente di qualsiasi elemento figlio con** `position: absolute`**.**
    Ciò significa che i suoi figli saranno riposizionati su questo particolare elemento, invece che sul genitore relativo più in alto, quando gli viene applicata una posizione assoluta.

- Typography
- Colors
- Gradients

---

#### 5. JavaScript - web 2.0

---

### Risorse utili:

[Learn CSS](https://web.dev/learn/css/)
[CSS Podcast](https://thecsspodcast.libsyn.com/)
[Layout Land Youtube Channel](https://www.youtube.com/channel/UC7TizprGknbDalbHplROtag)

[Learn HTML](https://web.dev/learn/html/)
[Mozilla Web Documentation](https://developer.mozilla.org/en-US/)

[Learn JavaScript](https://launchschool.com/books/javascript)

#### Risorse bonus

_Ora che ChatGPT è sotto l'attento scrutinio della polizia del futuro dovremo ritornare ai trucchi del mestiere di prima, i generatori di codice! Personalmente li considero anche più divertenti di una chat bot..._

Copiate, incollate nel vostro css, puntando a uno dei vostri tag HTML e sperimentate

[Generatore di CSS](https://cssgenerator.org/)
Una collezione di generatori di codice CSS.
Tramite interfaccia potrete stilizzare la proprietà CSS in real-time e generare lo snippet di codice necessario.

[Neumorfismo](https://neumorphism.io/#e0e0e0)
Un trend di design che sta prendendo piede negli ultimi tempi.
È il successore dello Scheumorfismo, altro stile di design delle interfacce molto usato negli anni 2000, specialmente da Apple.

[Qui un articolo che illustra](https://appleinsider.com/articles/22/08/23/what-apple-learned-from-skeuomorphism-and-why-it-still-matters), anche visivamente, in cosa comporta lo Scheumorfismo e riporta un pò della sua storia e declino.

[Generatore di sfumature CSS](https://cssgradient.io/)
[Generatore di sfumature CSS di Josh Comeau](https://www.joshwcomeau.com/gradient-generator/)
Potete usare entrambe ma vi lascio [il link all'articolo del nostro collega Josh](https://www.joshwcomeau.com/css/make-beautiful-gradients/), dove ci illustra un problema che hanno le sfumature sul web, un punto di grigio nel centro che spegne tutta la bellezza dei gradienti.
