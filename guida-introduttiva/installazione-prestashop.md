# Installazione di PrestaShop 1.7

PrestaShop è un programma di facile installazione. Una volta caricati tutti i file sul tuo server web, dovresti essere in grado di avviare la configurazione del negozio in meno di 5 minuti nella maggior parte dei casi: il processo di installazione è estremamente semplice e il programma di installazione esegue tutte le operazioni necessarie automaticamente. Per gli utenti meno esperti, l'intero processo potrebbe richiedere tra i 10 e i 20 minuti.

Prima di iniziare, verifica di soddisfare tutti i requisiti necessari: spazio del server sul provider di hosting, nome di dominio, client FTP ed editor di testo. Accertati di aver seguito attentamente le istruzioni contenute nella pagina "[Di che cosa hai bisogno per iniziare](di-che-cosa-hai-bisogno-per-iniziare.md)".

1&1 IONOS, il nostro partner di hosting web, offre un processo di installazione con un solo clic che ti permette di risparmiare tempo e di iniziare quanto prima. In questo caso, gli utenti inesperti potranno ridurre notevolmente i tempi di installazione.&#x20;

* [Hosting 1&1 IONOS](https://www.ionos.it/soluzioni-ecommerce/prestashop-hosting?ac=OM.IA.IAs96K414096T7073a)&#x20;

I seguenti host web utilizzano le seguenti librerie di script:

* [SimpleScripts](https://www.simplescripts.com/script\_details/install:PrestaShop)
* [Installatron](http://installatron.com/apps?locale=en#cmd=browser\&display=prestashop)
* [Softaculous](http://www.softaculous.com/apps/ecommerce/PrestaShop)

Alcuni di questi script supportano anche l'aggiornamento con un solo clic, una funzionalità dal valore inestimabile.

Altri host offrono i propri script di installazione. Per ulteriori informazioni, contatta il tuo host.

## Istruzioni per l'installazione rapida <a href="#installazionediprestashop1.7-istruzioniperlinstallazionerapida" id="installazionediprestashop1.7-istruzioniperlinstallazionerapida"></a>

Di seguito, è disponibile una serie di istruzioni pensate appositamente per gli utenti già esperti di installazione delle applicazioni PHP/MySQL su un server web. Se la mancanza di dettagli non soddisfa le tue esigenze, troverai istruzioni dettagliate nella sezione successiva del presente capitolo.

1. Se non lo hai già fatto, scarica e decomprimi il pacchetto di PrestaShop.
2. Se possibile, crea un database per il negozio PrestaShop sul tuo server web. Se non esiste alcun utente MySQL con tutti i privilegi di accesso e modifica di questo database, crealo.
3. Carica i tre file di PrestaShop nella posizione selezionata sul tuo server web, incluso il file ZIP (verrà decompresso automaticamente in seguito).
4. Esegui lo script di installazione di PrestaShop accedendo all'URL pubblico della posizione selezionata in un browser web. Dovrebbe trattarsi dell'URL in cui hai caricato i file di PrestaShop.
5. Segui le istruzioni in ciascuna schermata del programma di installazione.
6. Al termine dell'installazione, elimina la cartella `/install` e prendi nota di quella nuova della cartella `/admin`, che è stata generata in modo da risultare univoca per l'utente, per motivi di sicurezza.

A questo punto, PrestaShop dovrebbe risultare installato e pronto la configurazione. Procedi con il capitolo [Primi passi con PrestaShop 1.6](../guida-utente/primi-passi.md) della Guida utente.

## Istruzioni dettagliate <a href="#installazionediprestashop1.7-istruzionidettagliate" id="installazionediprestashop1.7-istruzionidettagliate"></a>

### Download e decompressione dell'archivio di PrestaShop <a href="#installazionediprestashop1.7-downloadedecompressionedellarchiviodiprestashop" id="installazionediprestashop1.7-downloadedecompressionedellarchiviodiprestashop"></a>

Puoi scaricare l'ultima versione di PrestaShop all'indirizzo [https://www.prestashop.com/it/download](https://www.prestashop.com/it/download).

È disponibile un'unica opzione di download: l'ultima versione stabile, predisposta per tutti i negozi on-line.

Se desideri scaricare una qualsiasi versione precedente, visita il seguente indirizzo: [https://www.prestashop.com/it/developers-versions#previous-version](https://www.prestashop.com/it/versioni-sviluppatori#previous-version).

Nota: sconsigliamo vivamente di utilizzare versioni diverse da quella corrente, che risulta essere la più stabile.

Fai clic sul pulsante "Scarica" e salva l'archivio sul tuo computer (ad esempio sul desktop). Il file dovrebbe presentare il seguente nome: "prestashop\_1.7.0.0.zip" (o equivalente, in base ai numeri di versione).

Il file scaricato è un archivio ZIP. Per continuare con il processo, **devi decomprimere l'archivio**.

Se il tuo sistema operativo non supporta in origine i file ZIP, puoi scaricare e installare un apposito strumento, ad esempio:

* Windows:
  * 7-zip: [http://www.7-zip.org/](http://www.7-zip.org/)
  * WinZip: [http://www.winzip.com/win/en/index.htm](http://www.winzip.com/win/it/index.htm)
  * WinRAR: [http://www.rarlab.com/](http://www.rarlab.com/)
* Mac OS X:
  * iZip: [http://www.izip.com/](http://www.izip.com/)
  * WinZip Mac: [http://www.winzip.com/mac/](http://www.winzip.com/mac/)
  * Zipeg: [http://www.zipeg.com/](http://www.zipeg.com/)

Utilizzando uno strumento per file ZIP; estrai il contenuto dell'archivio in un percorso noto dell'unità disco rigido (ad esempio sul desktop). **Non caricare il file ZIP direttamente nel server web**.

Nella cartella principale del file ZIP, sono presenti tre elementi:

* "prestashop.zip", che contiene tutti i file di PrestaShop da caricare sul server web.
* File "Install\_PrestaShop.html", che consente di aprire questa pagina nel browser web predefinito.
* File "index.php", che consente di avviare l'installazione.

Il file "Install\_PrestaShop.html" non deve essere caricato sul server web.

### Caricamento di PrestaShop <a href="#installazionediprestashop1.7-caricamentodiprestashop" id="installazionediprestashop1.7-caricamentodiprestashop"></a>

Ora dovresti disporre di uno spazio di hosting (in caso contrario, consulta il capitolo "Di che cosa hai bisogno per iniziare" della presente guida) e una cartella sull'unità disco rigido con l'archivio di PrestaShop decompresso.

Questo passaggio ti permette di caricare i file di PrestaShop sullo spazio di hosting. A tale scopo, collega il computer al server con uno strumento noto come "client FTP", che molto probabilmente hai già installato durante la lettura del capitolo "Di che cosa hai bisogno per iniziare". In questo caso, utilizzeremo il programma FileZilla gratuito ([http://filezilla-project.org/](http://filezilla-project.org/)).

Collegati allo spazio di hosting tramite il client FTP, utilizzando i dettagli di connessione forniti dal tuo host web (in caso contrario, contatta il tuo host). Una volta eseguita la connessione, devi trasferire i file di PrestaShop dal computer al server.

In FileZilla (o qualsiasi altro client FTP), sfoglia le cartelle locali finché non trovi quella che contiene i file di PrestaShop. Tienila aperta nella sezione "Sito locale" a sinistra.

Nella sezione "Sito remoto" (a destra), individua la posizione in cui desideri che PrestaShop diventi pubblicamente disponibile (radice del dominio, sottocartella, sottodominio ecc.) La scelta varia in base all'host e alle tue esigenze:

* Host:
  * Alcuni host potrebbero richiedere di collocare i file in una cartella specifica, ad esempio `/htdocs`, `/public_html`, `/web`, `/www`, `/`[nomedominio.com](http://nomedominio.com), etc.
  * Altri server FTP di host ti permettono di accedere direttamente allo spazio di caricamento appropriato.
* Le tue esigenze:
  * Se desideri che il tuo negozio sia il sito web principale per il tuo nome di dominio (ad es. [http://www.esempio.com](http://www.esempio.com/)), carica PrestaShop nella cartella principale dello spazio di caricamento (che potrebbe variare in base all'host).
  * Se desideri che il tuo negozio si trovi in una sottocartella del tuo nome di dominio ([http://www.esempio.com/negozio](http://www.esempio.com/negozio/)), devi prima creare una cartella tramite FileZilla (fai clic con il pulsante destro del mouse e scegli "Crea cartella"), quindi carica PrestaShop in tale cartella.
  * Se desideri che il tuo negozio si trovi in un sottodominio del tuo nome di dominio ([http://negozio.esempio.com](http://negozio.esempio.com/)), devi prima creare un sottodominio. Questa operazione varia in base all'host: ad esempio, semplicemente aggiungendo una nuova cartella con il client FTP o creando il sottodominio tramite il pannello di amministrazione dell'host. Consulta prima la documentazione di supporto del tuo host. Una volta creata, individua la cartella del sottodominio e carica PrestaShop in questa posizione.

Nel lato sinistro di FileZilla, dovrebbe essere presente la cartella locale in cui hai estratto i file di PrestaShop dall'archivio ZIP e nel lato destro la posizione di destinazione. Se non lo hai ancora fatto, il caricamento è un'operazione semplice: seleziona i tre file dalla cartella locale (utilizza Ctrl-A) e trascinali e rilasciali nella cartella remota oppure fai clic con il pulsante destro del mouse sulla selezione e scegli "Carica" nel menu contestuale.

### Creazione di un database per il negozio <a href="#installazionediprestashop1.7-creazionediundatabaseperilnegozio" id="installazionediprestashop1.7-creazionediundatabaseperilnegozio"></a>

Prima di poter installare effettivamente PrestaShop, devi verificare che MySQL Server disponga di un database predisposto per i dati di PrestaShop. In caso contrario, devi crearne uno.

Per creare un database, puoi utilizzare qualsiasi strumento di amministrazione di database. Utilizzeremo lo strumento phpMyAdmin gratuito ([http://www.phpmyadmin.net/](http://www.phpmyadmin.net/)), che dovrebbe essere fornito preinstallato dalla maggior parte degli hosting web.

Alcuni host spingono i clienti a utilizzare un pannello di controllo grafico, ad esempio cPanel, Plesk o uno personalizzato. Accertati di consultare la documentazione dell'host sulla gestione dei database MySQL e di creare un database per il tuo negozio seguendo le direttive specifiche di tale host.

Collegati a phpMyAdmin utilizzando le credenziali del tuo account, fornite dal tuo host. Dovrebbero essere accessibili tramite un URL standard, collegato al tuo nome di dominio o nome di dominio dell'host.

Nella colonna sinistra, sono elencati i database attualmente disponibili su MySQL Server. Alcuni di questi devono essere lasciati soli, poiché sono utilizzati da phpMyAdmin o dall'host: `phpmyadmin`, `mysql`, `information_schema`, `performance_schema` e altri. Consulta la documentazione dell'host per sapere se uno di questi può essere utilizzato come database predefinito.

In ogni caso, puoi creare un nuovo database dalla scheda "Database" e utilizzando il modulo centrale denominato "Create new database" (Crea nuovo database). Ti basterà inserire un nome univoco e fare clic su "Create" (Crea). Il nome del database verrà aggiunto all'elenco a sinistra. A questo punto, puoi utilizzarlo per archiviare i dati di PrestaShop.

### Avvio del programma di installazione automatico <a href="#installazionediprestashop1.7-avviodelprogrammadiinstallazioneautomatico" id="installazionediprestashop1.7-avviodelprogrammadiinstallazioneautomatico"></a>

A questo punto, è arrivato il momento di installare PrestaShop.

Il processo di installazione è abbastanza semplice poiché è facilitato dal programma di installazione automatico di PrestaShop. Dovresti essere in grado di utilizzarlo nel giro di pochi minuti. Accertati di leggere attentamente ciascuna pagina per non perdere alcuna informazione.

Per avviare il programma di installazione, ti basterà individuare la posizione di PrestaShop sul tuo server web: lo script rileverà automaticamente che PrestaShop non è installato e ti farà visualizzare il programma di installazione automatico. Al contempo, il file prestashop.zip caricato verrà decompresso. A questo punto, tutti i file di PrestaShop sono disponibili sul tuo server web.

Se stai eseguendo un'installazione sul tuo computer, l'installazione deve essere eseguita nella cartella di PrestaShop sul tuo server web locale, che dovrebbe essere disponibile all'indirizzo [http://127.0.0.1/prestashop](http://127.0.0.1/prestashop).

A questo punto, ti basterà leggere, selezionare e inserire altri moduli.

Si tratta di 6 passaggi. Nella parte superiore della pagina, l'assistente di installazione offre una visualizzazione dell'avanzamento del processo: i cerchi grigi si trasformano in segni di spunta verdi al termine di ogni passaggio.

#### Passaggio 1: pagina iniziale <a href="#installazionediprestashop1.7-passaggio1-paginainiziale" id="installazionediprestashop1.7-passaggio1-paginainiziale"></a>

Questa pagina è una rapida introduzione del processo di installazione. Puoi scegliere la lingua in cui visualizzare le istruzioni del programma di installazione.

Ti viene fornito anche un link al sito della documentazione ([http://doc.prestashop.com/](http://doc.prestashop.com/)) e un link alla nostra offerta di supporto. Per ulteriori informazioni sui nostri servizi di supporto, visita [https://addons.prestashop.com/it/35-guida](https://addons.prestashop.com/it/35-guida).

Seleziona la lingua in cui desideri visualizzare il programma di installazione, quindi fai clic sul pulsante "Avanti". Ciò imposterà anche la lingua predefinita dell'installazione di PrestaShop, tuttavia sono disponibili anche altre lingue.

#### Passaggio 2: licenze di PrestaShop <a href="#installazionediprestashop1.7-passaggio2-licenzediprestashop" id="installazionediprestashop1.7-passaggio2-licenzediprestashop"></a>

Questa seconda pagina è un semplice requisito: PrestaShop è un software gratuito e distribuito in base a un determinato set di licenze open source. Se non accetti i termini delle licenze, non puoi utilizzare il software; questo passaggio richiede di accettarle esplicitamente.

Leggi le licenze di PrestaShop:

* _Open Software License 3.0_ per PrestaShop, consultabile anche all'indirizzo [http://www.opensource.org/licenses/OSL-3.0](http://www.opensource.org/licenses/OSL-3.0).&#x20;
* _Academic Free License 3.0_ per i moduli e i template grafici, consultabile anche all'indirizzo [http://opensource.org/licenses/AFL-3.0](http://opensource.org/licenses/AFL-3.0).

Per installare PrestaShop, devi accettare entrambe le licenze.

Per accedere al passaggio successivo, devi selezionare la casella "Accetto i termini e condizioni", quindi fai clic su "Avanti". Se non accetti esplicitamente le licenze, non puoi installare PrestaShop: il pulsante "Avanti" non risulterà selezionabile.

#### Passaggi 3 e 4: compatibilità del sistema e informazioni del negozio <a href="#installazionediprestashop1.7-passaggi3e4-compatibilitadelsistemaeinformazionidelnegozio" id="installazionediprestashop1.7-passaggi3e4-compatibilitadelsistemaeinformazionidelnegozio"></a>

La terza pagina consente di verificare rapidamente i parametri del server sull'host. Nella maggior parte dei casi, questa pagina non viene mostrata poiché non viene rilevato alcun problema, quindi si passa direttamente alla quarta pagina, "Informazioni sul negozio". Se invece preferisci visualizzare la terza pagina, ti basterà fare clic sul link "Compatibilità del sistema" nella barra laterale sinistra.

Se si verificano problemi durante il controllo del server nel terzo passaggio, viene mostrata la pagina "Compatibilità del sistema", in cui puoi visualizzare tutti i controlli che hanno riportato esito negativo.

**Compatibilità del sistema**

In questa pagina, viene verificata l'assenza di problemi nella configurazione del server: impostazioni PHP, autorizzazioni su file e cartelle, strumenti di terze parti ecc.

Se si verificano problemi, il programma di installazione viene interrotto in questo punto, consentendoti di visualizzare alcuni dettagli tecnici che richiedono attenzione, ad esempio richiedendo di modificare la configurazione PHP o aggiornare le autorizzazioni dei file.

Di seguito è disponibile un elenco dei controlli eseguiti durante il terzo passaggio:

| **Controllo**                                                        | **Come/dove risolvere?**                                                                                     |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| PHP 5.4 o versione successiva è installato?                          | Server web                                                                                                   |
| PrestaShop è in grado di caricare file?                              | File php.ini (`file_uploads`)                                                                                |
| PrestaShop è in grado di creare nuovi file e cartelle?               | Browser file / client FTP / riga di comando                                                                  |
| La libreria GD è installata?                                         | File php.ini (`extension=`[php\_gd2.so](http://php\_gd2.so))                                                 |
| Il supporto di MySQL è attivo?                                       | File php.ini (`extension=`[php\_pdo\_mysql.so](http://php\_pdo\_mysql.so))                                   |
| Autorizzazione di scrittura ricorsiva su \~/config/                  | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/cache/                   | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/log/                     | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/img/                     | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/mails/                   | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/modules/                 | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/override/                | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/themes/default/lang/     | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/themes/default/pdf/lang/ | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/themes/default/cache/    | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/translations/            | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/upload/                  | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/download/                | Browser file / client FTP / riga di comando                                                                  |
| Autorizzazione di scrittura ricorsiva su \~/sitemap.xml              | Browser file / client FTP / riga di comando                                                                  |
| PrestaShop è in grado di aprire URL esterni?                         | File [php.in](http://php.in) (`allow_url_fopen`)                                                             |
| L'opzione "register global" di PHP è disattivata?                    | File php.ini (`register_globals`)                                                                            |
| La compressione GZIP è attivata?                                     | File .htaccess                                                                                               |
| L'estensione Mcrypt è disponibile?                                   | File php.ini (visita [http://php.net/manual/en/mcrypt.setup.php](http://php.net/manual/en/mcrypt.setup.php)) |
| L'opzione "magic quotes" di PHP è disattivata?                       | File php.ini (`magic_quotes_gpc`)                                                                            |
| L'estensione Dom è stata caricata?                                   | Opzione dell'ora di compilazione `--enable-dom`                                                              |
| L'estensione PDO MySQL è stata caricata?                             | File php.ini (`extension=`[php\_pdo\_mysql.so](http://php\_pdo\_mysql.so))                                   |

Sebbene la modifica della configurazione PHP possa essere effettuata solo in base ai singoli casi a seconda del livello di accesso al server, e quindi possa essere descritta solo in modo estremamente dettagliato, l'aggiornamento delle autorizzazioni dei file è sicuramente un argomento più semplice da spiegare.

Le autorizzazioni rappresentano la modalità con cui un file system concede diritti di accesso a utenti o gruppi di utenti specifici, permettendo di controllare la loro possibilità di visualizzare o apportare modifiche a file e cartelle. Il programma di installazione deve apportare diverse modifiche ai file caricati e se il file system non consente tali modifiche tramite autorizzazioni appropriate, non è possibile procedere ulteriormente con il processo di installazione.

Quindi, se il programma di installazione mostra che ad alcuni file o cartelle non sono associate le autorizzazioni appropriate, devi modificare tali autorizzazioni manualmente. A tale scopo, devi accedere ai tuoi file sul server web e quindi utilizzare il client FTP (ad esempio FileZilla) o la riga di comando.

Accedi all'account del server tramite il client FTP, seleziona la cartella di PrestaShop e individua le cartelle che richiedono una modifica delle autorizzazioni.

CHMOD

L'operazione di modifica delle autorizzazioni di file/cartelle su un sistema Unix/Linux viene definita "CHMOD", dal nome del comando omonimo (consulta: [https://it.wikipedia.org/wiki/Chmod](http://it.wikipedia.org/wiki/Chmod); puoi trovare una spiegazione delle autorizzazioni dei file qui: [http://www.elated.com/articles/understanding-permissions/](http://www.elated.com/articles/understanding-permissions/)). \
Assegnare a file o cartelle un'autorizzazione di scrittura significa "eseguire un'operazione CHMOD 755" o "CHMOD 775", in base all'host.

Alcuni host potrebbero richiedere di eseguire l'operazione CHMOD 777, sebbene sia consigliata solo per un'esigenza una tantum.\
Se devi ricorrere all'operazione CHMOD 777 per installare PrestaShop, verifica di passare a un'impostazione più sicura (ad esempio 775 per le cartelle e 664 per i file) al termine dell'installazione.\
Consulta attentamente la documentazione del tuo host.

Grazie a FileZilla (e alla maggior parte dei client FTP), non devi utilizzare comandi Unix. La maggior parte dei client FTP consente di modificare le autorizzazioni in tutta semplicità, anche in termini grafici: dopo aver individuato un file o una cartella che richiede tale modifica, fai clic con il pulsante destro del mouse su tale elemento, quindi scegli "File permissions..." (Autorizzazioni file) nel menu a discesa. Verrà visualizzata una finestra di piccole dimensioni.

In base alla configurazione del server (che non sempre è disponibile a portata di mano), devi selezionare entrambe le colonne di caselle "Read" (Lettura) e "Execute" (Esecuzione), e almeno le righe "Owner" (Proprietario) e "Group" (Gruppo) per la colonna "Write" (Scrittura). Alcuni host potrebbero richiedere di selezionare la casella "Write" (Scrittura) pubblica, ma è opportuno sapere che è meglio evitare di dare la possibilità a chiunque nel tuo server di modificare i contenuti della tua installazione di PrestaShop.

Alcune cartelle potrebbero richiedere di concedere autorizzazioni di modifica anche per i rispettivi file e sottocartelle. In tal caso, seleziona la casella "Recurse into subdirectories" (Ricorsione nelle sottodirectory).

Durante la modifica delle autorizzazioni nel client FTP, verifica di aver apportato le modifiche appropriate eseguendo di nuovo i controlli di compatibilità del programma di installazione: fai clic sul pulsante "Refresh these settings" (Aggiorna queste impostazioni) del programma di installazione ogni qualvolta necessario.\
&#x20;Quanto tutti gli indicatori appaiono in verde, puoi fare clic su "Next" (Avanti). Se non tutte le voci risultano in verde, verifica che venga visualizzato almeno il messaggio "PrestaShop compatibility with your system environment has been verified!" (La compatibilità di PrestaShop con l'ambiente di sistema è stata verificata) nella parte superiore della pagina.

**Informazioni sul negozio**

In questa pagina, puoi iniziare a personalizzare il tuo negozio: puoi assegnargli un nome, indicare la principale attività svolta e i dati personali del proprietario del negozio (in alcuni paesi si tratta di un'operazione obbligatoria) e così via.

Non utilizzare un segno di due punti nel nome del negozio, poiché potrebbe impedire il funzionamento di alcune funzionalità (ad esempio, potresti non essere in grado di inviare email).

Puoi sostituire il segno di due punti con un trattino se desideri avere due sezioni nel titolo. Ad esempio, utilizza "Negozio - Il miglior posto per fare acquisti" anziché "Negozio: il miglior posto per fare acquisti".&#x20;

\
In questa pagina, inoltre, devi scegliere la password per accedere al pannello di amministrazione del tuo negozio: scegli una password facilmente memorizzabile, senza sottovalutarne la sicurezza.

Fai clic su "Next" (Avanti) per continuare.

#### Passaggio 5: configurazione del sistema <a href="#installazionediprestashop1.7-passaggio5-configurazionedelsistema" id="installazionediprestashop1.7-passaggio5-configurazionedelsistema"></a>

In questa pagina è disponibile un modulo che ti consente di specificare dove si trova il server di database di PrestaShop, quale database utilizzare e altri dettagli. Tutte queste informazioni dovrebbero esserti state fornite dall'host web.

Compila tutti i campi con le informazioni di connessione del database fornite dall'host web:

* **Database server address** (Indirizzo server database): il nome host di MySQL Server. Può essere collegato al tuo nome di dominio (ad es. [http://sql.esempio.com](http://sql.esempio.com/)), collegato al tuo host web (ad es. [http://mysql2.alwaysdata.com](http://mysql2.alwaysdata.com/)) o essere semplicemente un indirizzo IP (ad es. 46.105.78.185).
* **Database name** (Nome database): il nome del database in cui desideri archiviare i dati di PrestaShop. Si può trattare del database esistente su MySQL Server o di quello creato utilizzando phpMyAdmin (o qualsiasi altro strumento SQL) nella sezione "Creazione di un database per il negozio" della presente guida.
* **Database login** (Accesso database): il nome dell'utente MySQL che ha accesso al tuo database.
* **Database password** (Password database): la password dell'utente MySQL.
* **Database engine** (Motore database): il motore del database è il cervello del tuo server di database. InnoDB è il motore predefinito, quindi ti consigliamo di utilizzare questo, tuttavia gli utenti più esperti possono scegliere di utilizzarne un altro. In genere, non è necessario modificare l'impostazione predefinita.
* **Tables prefix** (Prefisso tabelle): il prefisso delle tabelle di database. "`ps_`" è l'impostazione predefinita, che fa sì che le tabelle SQL di PrestaShop presentino nomi quali "`ps_cart`" o "`ps_customer`"; tuttavia se desideri installare più istanze di PrestaShop sullo stesso database, devi utilizzare un altro prefisso per ciascuna installazione. In ogni caso, ti suggeriamo di creare un unico database per singola installazione di PrestaShop, se l'host web lo consente. Un consiglio ancora più valido: crea un'unica installazione di PrestaShop e abilita la funzionalità multinegozio per gestire più negozi dallo stesso back-end di PrestaShop.
* **Drop existing tables** (Rilascia tabelle esistenti): disponibile solo in "Modalità sviluppatore". Quando reinstalli PrestaShop, puoi scegliere di rilasciare le tabelle di database di PrestaShop per avviare l'applicazione allo stato originario.

Fai clic sul pulsante "Test your database connection now!" (Verifica la connessione di database ora) per verificare di aver indicato le informazioni del server appropriate.

Fai clic su "Next" (Avanti): verrà avviata la configurazione del negozio, la creazione e la compilazione delle tabelle di database e così via. L'operazione potrebbe richiedere qualche minuto: attendi e non eseguire altre operazioni nel browser.

Vengono eseguite le seguenti operazioni:

* Creazione del file `settings.inc.php`, che viene compilato con le informazioni che hai specificato.
* Creazione delle tabelle di database.
* Creazione del negozio predefinito con le relative lingue predefinite.
* Compilazione delle tabelle di database.
* Configurazione delle informazioni del negozio.
* Installazione dei moduli predefiniti.
* Installazione dei dati dimostrativi (prodotti, categorie, utente, pagine CMS ecc.)
* Installazione del template grafico.

Al termine, il negozio risulta installato e pronto per la configurazione.

### Completamento dell'installazione <a href="#installazionediprestashop1.7-completamentodellinstallazione" id="installazionediprestashop1.7-completamentodellinstallazione"></a>

Come puoi leggere nella pagina finale del processo di installazione, è necessario eseguire ulteriori azioni prima di chiudere il programma di installazione.

Un metodo semplice per migliorare la sicurezza dell'installazione è eliminare alcuni file e cartelle principali. A tale scopo, puoi utilizzare il client FTP, direttamente sul server. Gli elementi da eliminare sono i seguenti:

* La cartella "/install" (obbligatorio).
* La cartella "/docs" (opzionale), a meno che non ti serva per verificare lo strumento di importazione con i file di importazione esemplificativi contenuti in questa cartella.
* Il file "[README.md](http://readme.md)" (opzionale).

Fai clic sul pulsante "Manage your store" (Gestisci il tuo negozio) per visualizzare l'area di amministrazione.

Un'alta modalità utile per proteggere l'installazione è quella di utilizzare un nome personalizzato per la cartella di amministrazione: modifica la cartella "admin" con un nome significativo per te, ad esempio "4dmin-1537" o "MySecReT4dm1n".\
&#x20;**Prendi nota del nuovo nome assegnato alla cartella "admin"**, poiché a partire da questo momento potrai accedere alle pagine di amministrazione utilizzando questo indirizzo!

Infine, per chiudere tutte le porte potenzialmente dannose, utilizza il client FTP per aggiornare le autorizzazioni dei file e delle cartelle su 664, o 666 se il tuo host lo richiede. Se risultano diritti di accesso che impediscono ad alcuni moduli di funzionare, ti consigliamo di ripristinare l'impostazione delle autorizzazioni su 755.

**Complimenti! L'installazione è stata completata.**

Accedi al back office di PrestaShop andando alla cartella "admin" appena rinominata e inizia a compilare il catalogo con prodotti, aggiungendo trasportatori, costi di spedizione, marchi e fornitori, modificando il template grafico e configurando tutte le impostazioni necessarie in base alle tue esigenze e preferenze. Per ulteriori informazioni, consulta il capitolo "[Primi passi con PrestaShop 1.7](../guida-utente/primi-passi.md)".

Ti consigliamo di eseguire il backup periodico di database e file, possibilmente su più di un computer, al fine di recuperare i dati in caso di problemi relativi ad hardware o sicurezza.
