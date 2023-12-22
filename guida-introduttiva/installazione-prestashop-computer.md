# Installazione di PrestaShop sul tuo computer

Puoi installare PrestaShop sul computer locale, per verificarlo prima di investire denaro in un server e nome di dominio oppure per personalizzare il negozio in locale prima di applicare le modifiche all'installazione di PrestaShop già disponibile on-line.

Prima di installare qualsiasi applicazione web in locale, devi installare l'ambiente adeguato, nello specifico il server web Apache, l'interprete di linguaggio PHP, i server di database MySQL e possibilmente lo strumento phpMyAdmin. Si tratta del cosiddetto AMP: Apache+MySQL+PHP. È disponibile per molti sistemi operativi, che aggiungono un'altra lettera all'acronimo: WAMP (Windows+Apache+MySQL+PHP), MAMP (Mac OS X+...) e LAMP (Linux+...)

## Scelta di un pacchetto AMP <a href="#installazionediprestashopsultuocomputer-sceltadiunpacchettoamp" id="installazionediprestashopsultuocomputer-sceltadiunpacchettoamp"></a>

Questa operazione richiede di avere competenze abbastanza tecniche; per fortuna, esistono molti pacchetti preconfezionati che è possibile installare in tutta semplicità. Non escludono certamente la necessità di avere competenze tecniche, tuttavia dovrebbero semplificare notevolmente il lavoro. Poiché tutti i componenti dei pacchetti sono open source, nella maggior parte dei casi si tratta di programmi di installazione gratuiti. Di seguito è disponibile una selezione di programmi di installazione AMP gratuiti:

* EasyPHP: [http://www.easyphp.org/](http://www.easyphp.org/) (Windows)
* MAMP: [http://www.mamp.info/](http://www.mamp.info/) (Mac OS X)
* WampServer: [http://www.wampserver.com/en/](http://www.wampserver.com/en/) (Windows)
* XAMPP: [http://www.apachefriends.org/en/xampp.html ](https://www.apachefriends.org/it/index.html)(Windows, Mac OS X, Linux, Solaris)

Scegli il pacchetto che preferisci, quindi avvialo.

## Verifica del corretto funzionamento <a href="#installazionediprestashopsultuocomputer-verificadelcorrettofunzionamento" id="installazionediprestashopsultuocomputer-verificadelcorrettofunzionamento"></a>

Prima di procedere ulteriormente con il tutorial di installazione di PrestaShop, verifica che tutti i componenti del pacchetto AMP funzionino correttamente:

* **Il server web deve essere attivo e in esecuzione**. L'accesso dovrebbe essere disponibile tramite il browser, digitando "127.0.0.1" nella barra degli indirizzi.

[http://127.0.0.1](http://127.0.0.1/) è l'host locale, ovvero "il tuo computer": si tratta di un indirizzo di loopback che indirizza il browser al server web locale.\
[http://127.0.0.1](http://127.0.0.1/) e [http://localhost](http://localhost/) sono sinonimi: puoi utilizzare indifferentemente l'uno o l'altro, poiché entrambi indirizzano alla cartella principale del server web locale.

È possibile che alcuni server web non vengano avviati poiché le relative porte di connessione (in genere la porta 80) sono già utilizzate da un'altra applicazione.

Di solito, ciò si verifica quando si utilizza Skype. Per impedire a Skype di bloccare l'esecuzione del server web locale, vai alle impostazioni avanzate di Skype (Strumenti > Opzioni > Avanzate > Connessione) e deseleziona l'opzione "Usa le porte 80 e 443 per le connessioni in ingresso aggiuntive". Riavvia Skype, quindi avvia di nuovo il server web locale.

* **Il server di database deve essere attivo e in esecuzione**. MySQL è la posizione in cui vengono archiviati tutti i dati di PrestaShop. Il pacchetto AMP dovrebbe segnalarti in modo chiaro se MySQL è in esecuzione o meno.
* **Lo strumento phpMyAdmin deve essere accessibile**. Si tratta dell'applicazione web che ti consente di gestire i dati archiviati in MySQL. La sua ubicazione varia in base al pacchetto AMP scelto: potrebbe essere [http://127.0.0.1/phpmyadmin](http://127.0.0.1/phpmyadmin) (XAMPP, WampServer, MAMP), [http://127.0.0.1/mysql](http://127.0.0.1/mysql) (EasyPHP) o un altro percorso. Consulta la documentazione del pacchetto: potrebbe contenere un pulsante phpMyAdmin che ti consente di aprire l'URL corretto nel browser.

## Ricerca della cartella principale del server web locale <a href="#installazionediprestashopsultuocomputer-ricercadellacartellaprincipaledelserverweblocale" id="installazionediprestashopsultuocomputer-ricercadellacartellaprincipaledelserverweblocale"></a>

Dopo aver verificato che il pacchetto è stato installato correttamente e che tutti i suoi componenti sono in esecuzione, devi individuare la cartella principale del server web locale,

ovvero la cartella locale in cui archiviare i file dell'applicazione, che può essere confrontata con la cartella principale del tuo server on-line; per accedere al suo contenuto, digita [http://127.0.0.1](http://127.0.0.1/).

Il percorso locale effettivo della cartella varia notevolmente in base al pacchetto AMP, e può essere personalizzato:

* EasyPHP: `C:\easyphp\www`
* MAMP: `/Applications/MAMP/htdocs/`
* WampServer: `C:\wamp\www`
* XAMPP: `C:\xampp\htdocs` o `/Applications/xampp/htdocs`

## Ricerca delle informazioni utente di MySQL <a href="#installazionediprestashopsultuocomputer-ricercadelleinformazioniutentedimysql" id="installazionediprestashopsultuocomputer-ricercadelleinformazioniutentedimysql"></a>

Per installare PrestaShop, infine, devi conoscere il nome utente e la password principali di MySQL.

**La maggior parte dei pacchetti utilizza il nome utente "root" senza richiedere di specificare una password**, tra cui EasyPHP, MAMP, WampServer e XAMPP.

Consulta la documentazione del pacchetto.

## Nota finale prima del tutorial di installazione <a href="#installazionediprestashopsultuocomputer-notafinaleprimadeltutorialdiinstallazione" id="installazionediprestashopsultuocomputer-notafinaleprimadeltutorialdiinstallazione"></a>

Al termine, puoi seguire le sezioni restanti della presente Guida introduttiva e avviare l'installazione di PrestaShop.

Quando installi PrestaShop, tieni presente quanto segue:

* I file non devono essere caricati in un software web tramite un software FTP (ad esempio FileZilla): ti basterà spostarli nella cartella locale appropriata, come indicato sopra.
* Non devi creare un nome di dominio locale: PrestaShop è disponibile tramite l'indirizzo di loopback indicato sopra, ovvero [http://localhost](http://localhost/) oppure [http://127.0.0.1](http://127.0.0.1/). Anche PrestaShop è disponibile a questo indirizzo aggiungendo il nome della sua cartella, ad esempio [http://localhost/prestashop](http://localhost/prestashop) o [http://127.0.0.1/prestashop](http://127.0.0.1/prestashop) se PrestaShop si trova nella sottocartella `/prestashop/` della cartella principale locale. Quando accedi a questo indirizzo per la prima volta, dovresti essere indirizzato automaticamente all'installazione di PrestaShop, ovvero [http://localhost/prestashop/install](http://localhost/prestashop/install) oppure [http://127.0.0.1/prestashop/install](http://127.0.0.1/prestashop/install).

\
Hai letto tutto attentamente? Ora attieniti alle istruzioni contenute nella normale guida di installazione, cominciando direttamente dalla sezione "Creazione di un database per il negozio": [Installazione di PrestaShop](installazione-prestashop.md).
