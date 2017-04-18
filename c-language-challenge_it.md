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
* client sends the jpeg images
* server receives the jpeg images and shows
* server supports many windows, each windows shows images from a client
* use gtk or win32 APIs

# data-driven code

Make serial number certification program
* certificate a serial number file
* read spec.rc file to specify serial number format
* encode user information, user-account number, name, product id, in serial number
* decode the information from the serial number
* serial code is printed in BASE64 code.
* use any encryption algorithm

```
$ cat spec.rc
# field length
user-account 4
user-name 16
product-id 4

$ encode-serial spec.rc
user-account: 1234 <user-input>
user-name: gogostar <user-input>
product-id: 5678 <user-input>
abcd-defg- <output>

$ decode-serial
serial: abcd-defg-xxxx-xxxx <input>
account: 1234
name: gogostar
product: 5678
```

# pool-based memory allocator

make a pool-based memory allocator
* create pool as many as number of CPUs in your system
* each thread allocates memory from a pool of its own CPU
* apply your allocator to any multi-thread program and compare performance
  * ``LD_PRELOAD=${PATH}/lib/libyourallocator.so.1 app``

# make a shell

make your own shell
* features
  * pipe
  * redirection
  * background running
  * stdin, stdout, stderr
```
$ myshell
THIS-IS-MYSHELL> ls
a b c
THIS-IS-MYSHELL> ls > files.txt
THIS-IS-MYSHELL> cat ls
a b c
THIS-IS-MYSHELL> ls | cat > files.txt
THIS-IS-MYSHELL> asdf 2> error.txt
THIS-IS-MYSHELL> cat error.txt
command is not found
```

# Altre sfide

Nota bene! La struttura e&grave; molto di pi&ugrave; che la semplice implementazione. Rifletti sulla *scalabilit&agrave;*!
* http://www.cprogramming.com/challenge.html
* https://www.hackerrank.com/c-programming-test-1
* https://www.lix.polytechnique.fr/~liberti/public/computing/prog/c/C/PROBLEMS/problems.html
