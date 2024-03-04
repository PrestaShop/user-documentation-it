# Di che cosa hai bisogno per iniziare

## Istruzioni per la configurazione rapida

Di seguito, abbiamo messo a punto un elenco delle operazioni necessarie per avviare l'installazione di PrestaShop 1.7. Se necessiti di istruzioni più dettagliate, sono disponibili nelle sezioni successive a questa.

* Requisiti di sistema:
  * PHP 5.4 o versione successiva.
    * Impostazioni utili (nel file `php.ini`):&#x20;
      * `allow_url_fopen` impostato su On,&#x20;
      * `register_globals` impostato su Off`,`
      * `upload_max_filesize`impostato su "16M" (o più).
    * Devono avere estensioni PHP (nel file `php.ini`): PDO\_MySQL, cURL, SimpleXML, mcrypt, GD, OpenSSL, DOM, SOAP, Zip, fileinfo.
    * Strumenti server utili: cron/crontab, Memcached.
  * MySQL 5.0 o versione successiva.
  * Consigliato:&#x20;
    * Hosting Unix/Linux.
    * Apache Web Server 2.0 o versione successiva oppure nginx Web Server.
      * Impostazioni del modulo Apache:&#x20;
        * `mod_rewrite` abilitato,&#x20;
        * `mod_security` disabilitato,
        * `mod_auth_basic` disabilitato.
    * Almeno 128 Mb di RAM dedicata a PHP. Maggiore è la memoria, migliori saranno i risultati.
* Codice di accesso al server FTP, al database MySQL
  * Se non stai eseguendo un'installazione locale, devono essere forniti dal tuo host web.
* Qualsiasi editor di testo.
* Qualsiasi client FTP.
* Qualsiasi browser web moderno (se utilizzi Internet Explorer: almeno IE9).

Devi inoltre conoscere l'URL nel tuo dominio da cui desideri accedere al tuo o ai tuoi negozi.

Per ulteriori informazioni, consulta la pagina ufficiale dei requisiti di sistema: [https://www.prestashop.com/it/system-requirements](https://www.prestashop.com/it/system-requirements.).

Una volta completata la configurazione, puoi utilizzare la guida di installazione: [http://doc.prestashop.com/display/PS17/Installing+PrestaShop](file:///display/PS17/Installing+PrestaShop).

## Istruzioni per la configurazione dettagliata

PrestaShop è un'applicazione web: per funzionare, deve essere installata su un server web e richiede un nome di dominio che verrà utilizzato dai visitatori per accedere al tuo negozio.

### Registrazione di un nome di dominio

Prima di procedere con qualsiasi download o installazione, devi specificare una home page per il tuo negozio on-line PrestaShop, composta da due elementi: un nome di dominio e un server web. Un dominio è l'identificatore on-line del tuo sito web, ad esempio [esempio.com](http://esempio.com) o [ilmionegozioonline.net](http://ilmionegozioonline.net). È la facciata pubblica del tuo server web e quindi del tuo negozio.

Devi acquistare un nome di dominio per il tuo negozio. Dovresti ottenerne uno quando implementi il tuo hosting web: molti host web, infatti, offrono un dominio gratuito con ogni nuovo account. Dovrebbero essere gratuiti per un anno o per la durata di abbonamento a tale host web. In genere, si ottiene il pacchetto completo (hosting+nome di dominio) in un'unica soluzione.

I nomi di dominio forniti da un host potrebbero presentare un problema: se il servizio dell'host non soddisfa le tue esigenze, potresti voler passare a un host migliore; di conseguenza, dovrai spostare file, dati e nome di dominio sull'altro host.

File e dati possono essere spostati facilmente, ma in base all'host, potresti riscontrare difficoltà a riottenere il tuo nome di dominio. Poiché l'host ha acquistato il nome di dominio per tuo conto, tecnicamente il dominio è di proprietà di tale host, il quale potrebbe persino impedirti di trasferirlo su un altro host o chiederti di sostenere un costo. E poiché il nome di dominio è il tuo brand e il tuo indirizzo sul web, devi sottostare alle regole dell'host web.

Ecco perché spesso si consiglia di ottenere il proprio nome di dominio da un registrar indipendente (per ulteriori informazioni, consulta: [https://it.wikipedia.org/wiki/Registrar](https://it.wikipedia.org/wiki/Registrar.)). Tecnicamente, non puoi in alcun caso acquistare un nome di dominio: in realtà si tratta solo di un noleggio, spesso sostenendo un costo annuale, che ti dà il diritto di utilizzarlo, tuttavia non appena smetti di pagare l'abbonamento, non ti appartiene più e chiunque può appropriarsene.

Oltre a sostenere un costo per la registrazione del nome di dominio, devi pagare anche il servizio di hosting web. Ma almeno ti resta la libertà di passare a un host migliore in qualsiasi momento, senza sostenere costi supplementari: devi solo modificare gli indirizzi DNS del nome di dominio. Entro 24 ore, la modifica si diffonderà in tutto il mondo.

Se invece desideri ottenere il nome di dominio da un registrar indipendente, di seguito ne elenchiamo alcuni che puoi ritenere affidabili:

* Gandi: [http://en.gandi.net/](http://en.gandi.net/)
* Namecheap: [http://www.namecheap.com/](http://www.namecheap.com/)
* GoDaddy: [https://it.godaddy.com/?countryview=1](https://it.godaddy.com/?countryview=1)
* IONOS: [https://www.ionos.it](https://www.ionos.it/)

Ce ne sono molti altri. Chiedi un parere ai tuoi amici!

### Ricerca di un host

Una volta ottenuto un nome di dominio, devi collegarlo a PrestaShop. In altre parole, i file di PrestaShop devono risiedere su un server web. È possibile che tu già disponga di un server web personale, ma è più probabile che il negozio sia ospitato da un servizio di hosting Internet (per ulteriori informazioni, consulta: [http://en.wikipedia.org/wiki/Internet\_hosting\_service](http://en.wikipedia.org/wiki/Internet\_hosting\_service)), che ti offre una home page on-line sostenendo un costo mensile o annuale.

Prima di avviare un negozio on-line, devi selezionare un provider di hosting. In pratica, quasi tutti gli host web sono compatibili con la soluzione PrestaShop. Tuttavia, solo alcuni provider di hosting offrono server ottimizzati per PrestaShop (installazione e versione aggiornata con un clic). Di seguito è disponibile il nostro [elenco di partner di hosting](https://www.prestashop.com/it/ecommerce-hosting).

Quando scegli l'host, ricordati di soddisfare un requisito fondamentale: deve offrire supporto per PHP 5.4 (o versione più recente), il linguaggio di programmazione con cui è stato compilato PrestaShop e MySQL 5 (o versione più recente), il sistema di database in cui vengono archiviati tutti i dati di PrestaShop. Sono presenti altri requisiti: per ulteriori informazioni, consulta la sezione "Requisiti tecnici" sotto.

### Requisiti tecnici

PrestaShop è un'applicazione eseguita su un server web ed è compilata con il linguaggio di programmazione PHP. I suoi dati vengono archiviati in un server MySQL.

PHP è un linguaggio di programmazione open source, utilizzato principalmente per le applicazioni web. Creato nel 1995, è attualmente il linguaggio di programmazione più utilizzato dagli sviluppatori web. Utilizza una sintassi C-like: per questo motivo, può essere facilmente appreso dagli sviluppatori.

MySQL è un sistema di gestione di database open source. Creato nel 1995, proprio come il linguaggio PHP, è attualmente il sistema di database più utilizzato dagli sviluppatori web. È basato sul linguaggio SQL, il codice di database maggiormente utilizzato.

Qualunque sia il servizio di hosting scelto, i seguenti componenti devono essere installati nel tuo server web:

* **Sistema**: Unix, Linux o Windows. Ti consigliamo vivamente di utilizzare Unix.
* **Server web**: Apache Web Server 2.0 o versione successiva.
* **PHP 5.4 o versione successiva**. È possibile che ti venga richiesto di attivare PHP 5 (contatta il tuo provider di hosting).
* **MySQL 5.0 o versione successiva**.
* Almeno 128 Mb di RAM sul server.

PrestaShop è inoltre compatibile con Microsoft IIS Web Server 6.0 o versione successiva e nginx 1.0 o versione successiva.

Ulteriori informazioni per gli amministratori di sistema sono disponibili nella [Guida per gli amministratori di sistema](file:///display/PS15/System+Administrator+Guide). Ti consigliamo vivamente di consultarla!

### Strumenti

Sono necessari due strumenti: un editor di testo, per la modifica dei file di testo, e un client FTP, per il trasferimento dei file dal tuo computer al server e viceversa.

**Editor di testo**

Di seguito sono disponibili alcuni editor di testo diffusi:

* Windows e OS X:
  * Sublime Text: [http://www.sublimetext.com/](http://www.sublimetext.com/)
  * Atom: [https://atom.io/](https://atom.io/)
* Unix/Linux:
  * Vim: [http://www.vim.org/](http://www.vim.org/)
  * Emacs: [http://www.gnu.org/software/emacs/](http://www.gnu.org/software/emacs/)

Non utilizzare un elaboratore di testo per la modifica dei file di testo, ad esempio Microsoft Word o Write di [OpenOffice.org](http://openoffice.org/).

Client FTP

FTP è l'acronimo di "File Transfer Protocol" (protocollo di trasferimento dei file), ovvero il metodo standard per trasferire file da un computer a un host web.

Nella presente guida, utilizzeremo FileZilla, un ottimo client FTP gratuito per Windows, Mac OS X e Linux. Scaricalo dal sito [http://filezilla-project.org/](http://filezilla-project.org/) e avvia il programma di installazione. Nota: non scaricare FileZilla Server, solo FileZilla Client!

Una volta installato FileZilla, devi configurarlo con i parametri di connessione del tuo server web, che dovrebbero esserti stati forniti dal tuo host. In caso contrario, contatta il tuo host o controlla la cartella dello spam della tua casella email.

In genere, i parametri necessari sono:

* **un nome host** o **un indirizzo IP**: la posizione del server FTP del tuo spazio di hosting.
* **un nome utente**: l'identificatore univoco del tuo account di hosting.
* **una password**: una misura di sicurezza obbligatoria.

Apri FileZilla, quindi il relativo strumento Gestore siti. A tale scopo, sono possibili tre opzioni:

* Premi Ctrl+S.
* Fai clic sull'icona "Apri il Gestore siti" nell'angolo superiore sinistro.
* Apri il menu "File", quindi seleziona l'opzione "Gestore siti...".

Viene visualizzata una finestra.

Per aggiungere il tuo spazio di hosting a Gestore siti:

1. Fai clic sul pulsante "Nuovo sito". Nell'elenco dei siti viene creata una nuova voce. Assegna un nome riconoscibile.
2. Nell'angolo destro, nella scheda "Generale", inserisci i seguenti parametri forniti dal tuo host: host, utente e password. Non modificare gli altri parametri predefiniti, a meno che non ti venga richiesto dall'host.
3. Una volta compilati tutti i campi, fai clic sul pulsante "Connetti". In questo modo, il tuo sito verrà salvato nell'elenco e verrà eseguito l'accesso al tuo account, affinché tu possa verificare che tutto funzioni correttamente.

Se non desideri utilizzare FileZilla, di seguito sono disponibili altri client FTP popolari:

* Windows:
  * CoreFTP: [http://www.coreftp.com/](http://www.coreftp.com/)
  * WinSCP: [http://winscp.net/](http://winscp.net/)
  * SmartFTP: [http://www.smartftp.com/](http://www.smartftp.com/)
* Mac OS X:
  * Cyberduck: [http://cyberduck.ch/](http://cyberduck.ch/)
  * Transmit: [http://www.panic.com/transmit/](http://www.panic.com/transmit/)
  * Fetch: [http://fetchsoftworks.com/fetch/](http://fetchsoftworks.com/fetch/)
* Unix/Linux:
  * gFTP: [http://gftp.seul.org/](http://gftp.seul.org/)
  * kasablanca: [http://kasablanca.berlios.de/](http://kasablanca.berlios.de/)
  * NcFTP: [http://www.ncftp.com/ncftp/](http://www.ncftp.com/ncftp/)

### Creazione di un piano

A questo punto, devi decidere dove ospitare PrestaShop. Sono disponibili quattro possibilità per il tuo nome di dominio:

* A livello di radice del dominio: [http://www.esempio.com/](http://www.esempio.com/)
* In una cartella: [http://www.esempio.com/negozio/](http://www.esempio.com/negozio/)
* In un sottodominio: [http://negozio.esempio.com/](http://negozio.esempio.com/)
* In una cartella di un sottodominio: [http://moda.esempio.com/boutique/](http://moda.esempio.com/boutique/)

Nota: grazie alla funzionalità multinegozio, puoi configurare tutti i negozi che desideri con un'unica installazione di PrestaShop 1.7, ognuno con il proprio nome di dominio specifico, se necessario. Tienilo presente quando decidi le posizioni in cui ospitare i vari negozi.\
&#x20;Qualsiasi sia il tuo piano, il negozio predefinito risiederà sempre nella posizione in cui si trova PrestaShop stesso.

### Installazione di PrestaShop

Infine, ora che tutti i requisiti sono stati soddisfatti, puoi utilizzare la guida di installazione: [http://doc.prestashop.com/display/PS17/Installing+PrestaShop](file:///display/PS17/Installing+PrestaShop).

**Sommario**

* Installazione di PrestaShop
  * Istruzioni per l'installazione rapida
  * Istruzioni dettagliate
    * Download e decompressione dell'archivio di PrestaShop
    * Caricamento di PrestaShop
    * Creazione di un database per il negozio
    * Avvio del programma di installazione automatico
    * Completamento dell'installazione

Il presente capitolo è indirizzato agli utenti che intendono installare PrestaShop sul proprio server web on-line.\
&#x20;Se desideri installare PrestaShop sul tuo computer, devi prima consultare le istruzioni contenute nella pagina: [Installazione di PrestaShop sul tuo computer](installazione-prestashop-computer.md).

Se hai già letto queste istruzioni, passa alla sezione "Creazione di un database per il tuo negozio" nella pagina corrente.
