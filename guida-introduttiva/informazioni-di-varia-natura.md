# Informazioni di varia natura

## Conserva una versione di test! <a href="#informazionidivarianatura-conservaunaversioneditest" id="informazionidivarianatura-conservaunaversioneditest"></a>

Dopo aver completato la configurazione del negozio in base alle tue preferenze e prima di renderlo ufficialmente disponibile al pubblico di acquirenti, ti consigliamo **vivamente** di installare una versione di test locale sul tuo PC (utilizzando [WAMP](http://en.wikipedia.org/wiki/Comparison\_of\_WAMPs) per Windows, [MAMP](https://it.wikipedia.org/wiki/MAMP) per Mac, [LAMP](https://it.wikipedia.org/wiki/LAMP) per Linux o [XAMPP](https://www.apachefriends.org/it/index.html) per tutte le piattaforme menzionate) oppure in qualsiasi posizione del tuo server di hosting.

Questa seconda istanza tornerà utile come ambiente di preproduzione in cui puoi apportare tutte le modifiche future al negozio on-line di PrestaShop, senza influire sulla versione pubblicata sul web. In questo modo, se si dovesse verificare un errore, il negozio sul web resterà intatto.

Dopo aver verificato che la versione di test funziona correttamente, copia la versione di test sulla versione web. Ti consigliamo di eseguire questa operazione in orari non di picco e dopo aver temporaneamente disabilitato il negozio dal back office di PrestaShop.

## Verifica della libreria GD <a href="#informazionidivarianatura-verificadellalibreriagd" id="informazionidivarianatura-verificadellalibreriagd"></a>

La [libreria GD](http://www.boutell.com/gd/)consente a PrestaShop di rielaborare le immagini che hai caricato, specialmente per ridimensionarle.

In un'installazione predefinita di PHP, la libreria GD deve essere attivata; in caso contrario, le istruzioni di Windows standard sono le seguenti:

1. Nella directory principale della cartella PHP, apri il file `php.ini`.
2. Elimina i commenti dalla riga `extension=php_gd2.dll` (circa a metà del file, in mezzo a un lungo elenco di estensioni) rimuovendo ";" all'inizio della riga.
3. Riavvia i servizi PHP.

Se non disponi di accesso al file `php.ini` (come spesso accade nel caso di hosting condiviso), contatta il tuo host spiegando le tue esigenze di hosting.

## Attivazione di PHP5 <a href="#informazionidivarianatura-attivazionediphp5" id="informazionidivarianatura-attivazionediphp5"></a>

In molti casi, i server dedicati o condivisi dispongono sia di PHP 4 che PHP 5, ma solo PHP4 è attivato per impostazione predefinita.

Per installare PrestaShop, è necessario che PHP 5 sia attivato. Se tenti di eseguire PrestaShop con PHP 4, visualizzerai numerosi errori, incluso questo messaggio molto comune:

```
Parse error: parse error, unexpected T_STATIC, expecting T_OLD_FUNCTION or T_FUNCTION or T_VAR or '}' in [php file] on line X.
```

Non esitare a segnalare un bug relativo ai suggerimenti necessari per far sì che PrestaShop funzioni correttamente sul tuo servizio di hosting sul forum [Forge](http://forge.prestashop.com/) di PrestaShop (devi disporre di un account). Lo aggiungeremo alla presente guida non appena ricevuto.

\
Di seguito è disponibile un elenco di procedure di cui siamo attualmente a conoscenza...

### 1&1 IONOS <a href="#informazionidivarianatura-1-and-1ionos" id="informazionidivarianatura-1-and-1ionos"></a>

Aggiungi la seguente riga al tuo file `.htaccess`:

```
AddType x-mapp-php5 .php
```

Per la ricompilazione dell'URL, aggiungi le seguenti righe:

```
Options +FollowSymLinks
RewriteEngine On
```

```
```

### [Free.fr](http://free.fr) <a href="#informazionidivarianatura-free.fr" id="informazionidivarianatura-free.fr"></a>

Aggiungi la seguente riga al tuo file `.htaccess`:

```
php 1
```

### OVH <a href="#informazionidivarianatura-ovh" id="informazionidivarianatura-ovh"></a>

Aggiungi la seguente riga al tuo file `.htaccess`:

```
SetEnv PHP_VER 5
```

Per disattivare i registri globali:

```
SetEnv REGISTER_GLOBALS 0
```

### GoDaddy <a href="#informazionidivarianatura-godaddy" id="informazionidivarianatura-godaddy"></a>

Per visualizzare la versione di PHP:

1. Accedi ad Account Manager (Gestione account).
2. Dalla sezione Products (Prodotti), fai clic su Web Hosting (Hosting web).
3. Accanto all'account di hosting che desideri utilizzare, fai clic su Launch (Avvia).

Nella sezione Server, viene visualizzata la versione di PHP.

Per modificare la versione di PHP:

1. Dal menu Content (Contenuto), seleziona Programming Languages (Linguaggi di programmazione).
2. Seleziona la versione di PHP che desideri utilizzare, quindi fai clic su Continue (Continua).
3. Fai clic su Update (Aggiorna).

L'applicazione delle modifiche può richiedere fino a 24 ore.

### Hosting condiviso di Lunarpages <a href="#informazionidivarianatura-hostingcondivisodilunarpages" id="informazionidivarianatura-hostingcondivisodilunarpages"></a>

1. Accedi a cPanel. Dovrebbe trovarsi in [http://www.(your\_domain).(com/net/org/etc)/cpanel](http://www.\(your\_domain\).\(com/net/org/etc\)/cpanel).
2. Inserisci il nome utente e la password del tuo account nella casella visualizzata.
3. Viene mostrata una nuova pagina. Vai alla riga di icone in basso nella pagina e fai clic sull'icona "Enable/Disable PHP 5" (Abilita/Disabilita PHP 5".
4. Viene mostrata una nuova pagina. Fai clic su "Add PHP 5 To Your Account!" (Aggiungi PHP 5 al tuo account).

La richiesta di modifica del linguaggio viene inviata. Attendi fino a 24 ore prima che la modifica venga elaborata dal server di hosting.
