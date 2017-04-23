Da lungo, penso che nuovi programmatori C siano più rari.
Nel frattempo che affronto la Eudyptula Challenge, ho realizzato che una simile sfida &egrave; necessaria per il linguaggio C.

non sono sicuro quali esercizi sono adatti e quanti task siano necessario...in realt&agrave; non ho ancora un piano.

Ma indicherò alcuni esercizi da stampare "Ciao mondo" al creare una classe tramite un puntatore di funzione.

Se avete un idea, potete inviarmi una pull request.

[discussione su reddit](https://www.reddit.com/r/linuxdev/comments/5r8k6g/new_service_like_the_eudyptula_challenge/)
* pnpbios
  * Scrivi il tuo demone personale, il tuo modulo PAM personale, scrivi un'interfaccia di rete personalizzata, scrivi la tua shell

Argomenti:
* file IO
  * crea ls
* concorrenza
* rete
  * crea il tuoo programma di chat
* memoria
  * crea il tuo allocatore pool di memoria
  * gestione degli errori
* toolchain: preprocessore, compilatore, linker
* cache
* assembly
* prestazioni
* sincronizzazione


# stampa "Ciao mondo!"

Usa argc e argv per stampare "Ciao mondo!".

```
$ print 3 "Ciao mondo!"
1 Ciao mondo!
2 Ciao mondo!
3 Ciao mondo!
```

# leggi cartelle e file
Crea uno strumento come ls che semplicemente stampi il nome della cartella selezionata.

# argomenti per la riga di commando

Crea uno strumento come ls che accetti opzioni ed effettua il parsing degli argomenti per la riga di commando tramite getopt, getopt_long
* opzioni brevi: -l, -a, -d
* opzioni lunghe: --long, --all, --directory
* l'opzione -l(--long) stampa dimensione, permessi, nome utente, data di ultima modifica.
* usa getopt, getopt_long per elaborare le opzioni

# cerca multi-thread

crea un programma di ricerca file che usa multipli thread
* preleva il nome file e il nome della cartella
* verifica quante cartelle esistono nella cartella scelta
* crea un thread per ogni cartelladirectories
* un thread cerca un specifico file in una cartella
* confronta le performance del precedente cerca con un singolo thread

# crea chat

crea una programma di chat 1:1 per il terminale
* crea server e client
* supporta IPv4 e IPv6

# crea ftp

crea server e client ftp
* invocazione lato server: ``ftp-server``
* invocazione lato client: ``ftp-client <IPADDR> <FILE-NAME>``
* stampa i caratteri '#' per mostrare l'andamento sul trasferimento del file
* crea il server come demone
* il server dovrebbe supportare connessioni multiple

# crea un riproduttore multimediale

i client inviano immagini sequenziali e il server mostra le immagini
* trasforma un'immagine gif in multiple immagini jpeg
* il client invia le immagini jpeg
* il server riceve le immagini jpeg e le mostra
* il server supporta molte finestre, ogni finestra mostra le immagini da un client
* usa le API gtk o win32

# Codice focalizzato sui dati

Crea un programma di certificazione dei numeri seriali
* certificate un codice seriale
* leggi il file spec.rc per specificare il formato del codice seriale
* codifica le informazioni dell'utente, il numero dell'account utente, il nome e l'id del prodotto nel numero seriale
* decodifica le informazioni dal numero seriale
* il codice seriale è scritto in Base64.
* usa qualsi algoritmo di criptazione
```
$ cat spec.rc
# lunghezza dei campi
account-utente 4
nome-utente 16
id-del-prodotto 4

$ codifica-seriale spec.rc
account-utente: 1234 <input-utente>
nome-utente: gogostar <input-utente>
id-del-prodotto: 5678 <input-utente>
abcd-defg- <output>

$ decodifica-seriale
seriale: abcd-defg-xxxx-xxxx <input>
account: 1234
nome: gogostar
prodotto: 5678
```

# allocatore di memoria basato su pool

crea un allocatore di memoria basato su pool
* crea un allocatore di memoria basato su pool per ogni CPU nel tuo PC
* ogni thread alloca memoria da un pool assegnato a s&egrave; stesso
* Utilizza il tuo allocatore in qualsias programma multi thread e confronta le prestazioni
  * ``LD_PRELOAD=${PATH}/lib/libyourallocator.so.1 app``

# crea una shell

crea la tua shell
* feature
  * pipe
  * redirezioni
  * esecuzione in background
  * stdin, stdout, stderr
```
$ miashell
QUESTA-E-LA-MIASHELL> ls
a b c
QUESTA-E-LA-MIASHELL> ls > file.txt
QUESTA-E-LA-MIASHELL> cat ls
a b c
QUESTA-E-LA-MIASHELL> ls | cat > file.txt
QUESTA-E-LA-MIASHELL> asdf 2> errore.txt
QUESTA-E-LA-MIASHELL> cat errore.txt
commando non trovato
```

# Altre sfide

Nota bene! La struttura e&grave; molto di pi&ugrave; che la semplice implementazione. Rifletti sulla *scalabilit&agrave;*!
* http://www.cprogramming.com/challenge.html
* https://www.hackerrank.com/c-programming-test-1
* https://www.lix.polytechnique.fr/~liberti/public/computing/prog/c/C/PROBLEMS/problems.html
