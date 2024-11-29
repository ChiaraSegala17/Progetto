STUDIO SUL SISTEMA DI GENERAZIONE AUTOMATICA DI SOTTOTITOLI IN ITALIANO SU YOUTUBE

ABSTRACT
Il progetto si propone di analizzare e confrontare i sottotitoli forniti dall'autore dei video e quelli generati automaticamente da YouTube. L'obiettivo è identificare somiglianze e differenze a livello di tokenizzazione, lemmatizzazione e PoS tagging, utilizzando strumenti di elaborazione del linguaggio naturale come spaCy. Il dataset è costituito da sottotitoli in lingua italiana, analizzati per estrarre comportamenti significativi. Questo progetto è motivato dalla necessità di valutare l'affidabilità dei sottotitoli automatici rispetto a quelli manuali.

DOMANDE DI RICERCA
L'idea del progetto nasce dall'osservazione di discrepanze linguistiche presenti a diversi livelli di analisi nei sottotitoli generati automaticamente da YouTube, in particolare quelli di una specifica playlist appartenente a un canale della piattaforma. Tali discrepanze sono emerse durante una prima analisi esplorativa, evidenziando differenze significative rispetto ai sottotitoli forniti dall'autore.

Sulla base di queste osservazioni preliminari, sono state formulate una serie di domande di ricerca volte a identificare e approfondire le problematiche linguistiche rilevate. L'attenzione si è focalizzata inizialmente sulle differenze nella tokenizzazione dei testi, per poi analizzare la coerenza e l'accuratezza della lemmatizzazione ed, infine, esaminare la distribuzione e la frequenza dei tag grammaticali utilizzati.

DATASET
Il dataset è composto da file di testo contenenti due tipologie distinte di sottotitoli: i sottotitoli forniti manualmente dall'autore dei video e quelli generati automaticamente da YouTube. Le due categorie sono state archiviate in due cartelle separate, denominate rispettivamente sottotitoli_autore e video_autosub.

Acquisizione dei dati
L'estrazione dei sottotitoli è stata effettuata utilizzando yt-dlp, uno strumento avanzato per il download di contenuti multimediali da piattaforme come YouTube, in combinazione con ffmpeg, una libreria altamente versatile per l'elaborazione e la conversione di file audio e video. La selezione dei video da cui estrarre i sottotitoli è avvenuta tramite un campionamento casuale, realizzato con il modulo Random della libreria Python.

Pre-elaborazione dei dati
I sottotitoli estratti sono stati suddivisi e archiviati nelle due cartelle sopra definite. Successivamente, sono stati sottoposti a un processo di pulizia e normalizzazione mediante l'uso del modulo Subprocess, per garantire un controllo preciso e avanzato sull'esecuzione dei processi di sistema.

Tokenizzazione, Lemmatizzazione e PoS Tagging
Per l'analisi linguistica, sono stati utilizzati strumenti specifici per il Natural Language Processing (NLP):
- La tokenizzazione è stata eseguita con il modulo word_tokenize della libreria NLTK.
- La lemmatizzazione e il PoS tagging sono stati realizzati con Stanza, preferita rispetto a NLTK per la maggiore precisione nel trattamento delle informazioni morfologiche e lessicali. Stanza utilizza il tagset standardizzato Universal Dependencies (UD) per le categorie grammaticali.

Confronto tra sottotitoli
Per effettuare un confronto quantitativo e qualitativo tra i due tipi di sottotitoli, sono state impiegate le seguenti librerie:
- NumPy e SciPy: utilizzate per la manipolazione e l'analisi numerica dei dati. Per garantire la compatibilità tra le versioni, è stato necessario un downgrade di NumPy.
- os, Pandas e Plotly: selezionate per interagire con le cartelle del file system, analizzare i dati dei file e creare tabelle interattive da esplorare più facilmente.

SUDDIVISIONE FASI PROGETTO 
Settimana 1: ideazione progetto, selezione e raccolta dei dataset necessari.
Settimana 2: selezione ed implementazione di programmi necessari, download e pulizia file. 
Settimana 3: tokenizzazione, lemmatizzazione e pos tagging.
Settimana 4: selezione ed implementazione programmi e librerie necessarie per il confronto. 
Settimana 5: confronto dei due dataset e creazione tabelle dei risultati per confronto. 
Settimana 6: scrittura del report finale, scrittura readme, preparazione repository e ultime correzioni di design del progetto.

DOCUMENTAZIONE
progetto_codice.ipynb = notebook con codice del progetto 
sottotitoli_autore = cartella con file di testo dei sottotitoli forniti dall'autore del canale considerato
video_autosub = cartella con file di testo dei sottotitoli generati automaticamente da YouTube
video_autosub_clean = cartella con file di testo dei sottotitoli generati automaticamente da YouTube puliti
tokenizza_sottotitoli_autore = cartella con file di testo dei sottotitoli dell'autore tokenizzati
sottotitoli_tokenizzati = cartella con file di testo dei sottotitoli automatici tokenizzati
sottotitoli_lemmatizzati_autore = cartella con file di testo dei sottotitoli dell'autore lemmatizzati
sottotitoli_lemmatizzati_youtube = cartella con file di testo dei sottotitoli automatici lemmatizzati
sottotitoli_pos_autore = cartella con file di testo dei sottotitoli dell'autore con pos tag
sottotitoli_pos_youtube = cartella con file di testo dei sottotitoli automatici con pos tag
confronto_tokenizzazione_interattivo.csv = cartelle con risultati del confronto dei sottotitoli tokenizzati 
confronto_lemmatizzazioni_interattivo.csv = cartelle con risultati del confronto dei sottotitoli lemmatizzati
confronto_pos_interattivo.csv = cartelle con risultati del confronto dei sottotitoli con pos tag
nuovo_env = cartella ottenuta dalla creazione di un ambiente virtuale isolato per installare versioni specifiche di NumPy e SciPy compatibili tra loro per evitare conflitti con versioni installate precedentemente.

