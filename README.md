# Il fascicolo sotto la lente

**Laboratorio interattivo, gratuito e utilizzabile anche offline, per riconoscere dati personali, informazioni riservate e rischi di reidentificazione nei documenti destinati a strumenti di intelligenza artificiale.**

Il progetto è una piccola applicazione web autonoma, pensata per chiunque voglia esercitarsi con l'analisi delle informazioni: personale degli enti pubblici, formatori, studenti, professionisti e gruppi di lavoro.

Non richiede account, registrazione, installazione, servizi cloud o una chiave API. **Tutti i casi sono inventati.**

## Prova subito

1. Scarica il file [`index.html`](./index.html).
2. Aprilo con un browser moderno (Chrome, Edge, Firefox o Safari).
3. Premi **«Apri il primo fascicolo»**.

Funziona anche senza connessione Internet: HTML, CSS, JavaScript e contenuti sono incorporati in un unico file.

## Che cosa puoi fare

- Esplorare **quattro fascicoli amministrativi simulati**.
- Selezionare direttamente nel documento ogni passaggio da valutare.
- Classificare l'informazione come **personale o identificativa**, **riservata dell'organizzazione** oppure **ordinaria/pubblica**.
- Proporre un trattamento: **mantenere**, **generalizzare** oppure **eliminare**.
- Consultare la **scheda dello strumento IA** e ulteriori **informazioni di contesto**, senza ricevere la risposta in anticipo.
- Visualizzare un'**anteprima didattica della versione rielaborata**.
- Decidere se utilizzare il documento nello specifico servizio descritto.
- Confrontare le scelte con un **commento ragionato per ogni passaggio** e con una valutazione della decisione complessiva.
- Annotare le riflessioni del gruppo, consultare il riepilogo e **scaricare un report in formato TXT**.
- Utilizzare un **timer facoltativo** e la modalità a schermo intero per laboratori o presentazioni.

### I quattro fascicoli

| # | Scenario | Che cosa mette alla prova |
| --- | --- | --- |
| 1 | **La pratica senza nome** | Codici, indirizzi, dati sanitari e pseudonimizzazione |
| 2 | **Nessun nome, ma non è pubblico** | Riservatezza di una bozza di appalto, anche senza dati personali |
| 3 | **Il report dei numeri troppo piccoli** | Reidentificazione mediante gruppi molto piccoli e dati combinabili |
| 4 | **Il rapporto già pubblicato** | Riconoscimento di un utilizzo ragionevolmente consentito, senza blocchi pregiudiziali |

Ogni caso richiede due tipi di giudizio: uno **sui singoli elementi del documento** e uno **sull'idoneità del suo utilizzo nello strumento proposto**. Le classificazioni sono valutate nel contesto specifico dello scenario, non come etichette universali applicabili a ogni dato.

## Come pubblicare su GitHub Pages

1. Crea un repository GitHub, per esempio `fascicolo-sotto-la-lente`.
2. Carica nella directory principale `index.html` e `README.md`.
3. Apri **Settings → Pages**.
4. In **Build and deployment**, scegli **Deploy from a branch**.
5. Seleziona il branch `main` e la cartella `/(root)`, quindi salva.
6. Quando la pubblicazione è completata, apri:

   `https://NOME-UTENTE.github.io/fascicolo-sotto-la-lente/`

Sostituisci `NOME-UTENTE` e il nome del repository con quelli effettivi. Non servono un processo di build, npm o GitHub Actions.

> Suggerimento: imposta il link del sito nella sezione **About** del repository, così le persone potranno avviare facilmente il laboratorio.

## Modalità d'uso consigliate

**Individuale:** leggi ogni caso, completa le classificazioni e confronta le motivazioni con i feedback prima di passare al successivo.

**In gruppo:** proietta l'applicazione su uno schermo, oppure lascia che ogni gruppo lavori su un dispositivo. Discute le scelte **prima** di aprire il commento. La simulazione è deliberatamente progettata per privilegiare il ragionamento rispetto alla velocità.

Durata indicativa: **25–35 minuti** per quattro fascicoli, aumentabile se si approfondiscono tutte le motivazioni e le domande di discussione. Il timer da 30 minuti è facoltativo e non blocca l'esperienza allo scadere.

## Personalizzazione

L'intero progetto è in `index.html`. Per modificare esempi e contenuti, cerca nel JavaScript le costanti:

- `CASES`: scenari, frammenti dei documenti, informazioni sul contesto e sullo strumento, classificazioni proposte e commenti.
- `CATEGORIES`: tre categorie di informazione.
- `ACTIONS`: tre interventi sul testo.
- `DECISIONS`: tre decisioni sul caricamento del documento.

Ogni fascicolo definisce un insieme di `parts` (testo e passaggi selezionabili) e una mappa `segments` con la categoria e gli interventi ritenuti coerenti nello scenario. Se aggiungi un nuovo segmento, assicurati che il suo `id` compaia sia in `parts` sia in `segments`.

**Nota:** le risposte sono volutamente contestualizzate. Un indirizzo, un importo o una media statistica non hanno sempre lo stesso significato in qualunque documento. La valutazione dipende dai mezzi ragionevolmente disponibili per l'identificazione, dallo scopo, dalla pubblicità delle informazioni e dalle autorizzazioni effettive.

## Privacy, sicurezza e funzionamento

- Non viene effettuata alcuna chiamata verso API o server.
- Non sono utilizzati cookie, analytics, localStorage o sessionStorage.
- Le risposte, il nome facoltativo del gruppo e le note rimangono nella memoria della pagina **soltanto finché resta aperta**.
- L'esportazione genera il TXT **localmente** nel browser.
- Non vengono caricati file veri; non c'è alcun collegamento a piattaforme di IA.
- Non è necessario né opportuno inserire dati personali reali nelle note.

**Attenzione:** la funzione di anteprima applica sostituzioni dimostrative alle porzioni marcate. **Non certifica anonimizzazione, sicurezza né autorizzazione all'uso**. Per documenti e sistemi reali servono sempre verifiche, basi giuridiche quando necessarie, misure e procedure applicabili.

## Limiti e responsabilità

Questo progetto è una **simulazione educativa**, non un sistema di anonimizzazione o classificazione documentale per pratiche reali e non costituisce parere legale.

Le classificazioni e i trattamenti proposti dipendono dai fatti inventati in ogni scenario. Non sostituiscono le procedure e le indicazioni del titolare del trattamento, del DPO o dei referenti competenti. Un servizio «autorizzato» non è automaticamente idoneo a ogni documento e a ogni finalità.

Per approfondire il tema della reidentificazione e della pseudonimizzazione sono utili le indicazioni del [Garante per la protezione dei dati personali](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10220271) e il [Regolamento generale sulla protezione dei dati (GDPR)](https://eur-lex.europa.eu/eli/reg/2016/679/oj/ita).

## Compatibilità

Browser recenti con supporto JavaScript e HTML `dialog`. L'interfaccia è responsive e funziona su computer, tablet e smartphone. Il layout documentale è particolarmente adatto a schermi di dimensioni medio-grandi.

Non sono previste integrazioni con database, sistemi di autenticazione o servizi di terze parti.

## Riutilizzo e contributi

Puoi scaricare e sperimentare il progetto localmente. Se desideri pubblicare una versione derivata e concedere esplicitamente ad altri i diritti di utilizzo, modifica e redistribuzione, aggiungi nel repository un file `LICENSE` con la licenza scelta dal titolare del progetto.

Per proporre miglioramenti, apri una **Issue** o una **Pull request** nel repository che ospita l'applicazione. Sono particolarmente utili segnalazioni su accessibilità, chiarezza dei casi, compatibilità con i browser e nuove situazioni d'uso.
