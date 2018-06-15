# A challenge list on planning

## print "Hello world!" (Planning)

Use argc and argv to print "Hello world!".

```
$ print 3 "Hello world!"
1 Hello world!
2 Hello world!
3 Hello world!
```

## read directory and file (Planning)

make ls tools that just print names of specified directory.
* do not need to get no options

## command argument (Planning)

make ls tools with options and do command argument parsing with getopt, getopt_long
* short options: -l, -a, -d
* long options: --long, --all, --directory
* -l(--long) option prints size, permission, user id, last modified time.
* use getopt, getopt_long to process options

## multi-thread find (Planning)

make find program that has multi-threads
* get file-name and directory-name
* check how many directory exists in target directory
* creates threads as many as directories
* one thread finds a specified file in one directory
* compare performance of one-thread find

## make chat (Planning)

make a 1:1 chatting program for terminal
* make server & client
* support IPv4 and IPv6

## make ftp (Planning)

make ftp server & client
* server-side usage: ``ftp-server``
* client-side usage: ``ftp-client <IPADDR> <FILE-NAME>``
* print '#' characters to show file-transfer is working
* make server as daemon
* server should support multi-connection

## make streaming player (Planning)

clients send sequential images and server shows images
* convert a gif image into many jpeg images
* client sends the jpeg images
* server receives the jpeg images and shows
* server supports many windows, each windows shows images from a client
* use gtk or win32 APIs

## data-driven code (Planning)

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

## pool-based memory allocator (Planning)

make a pool-based memory allocator
* create pool as many as number of CPUs in your system
* each thread allocates memory from a pool of its own CPU
* apply your allocator to any multi-thread program and compare performance
  * ``LD_PRELOAD=${PATH}/lib/libyourallocator.so.1 app``

## make a shell (Planning)

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

## More challenges (Planning)

Remember! Design is more than the implementation. Think *scalability*!
* http://www.cprogramming.com/challenge.html
* https://www.hackerrank.com/c-programming-test-1
* https://www.lix.polytechnique.fr/~liberti/public/computing/prog/c/C/PROBLEMS/problems.html

[discussion on reddit](https://www.reddit.com/r/linuxdev/comments/5r8k6g/new_service_like_the_eudyptula_challenge/)
* pnpbios
  * Writing your own daemon, your own PAM module, writing a custom network interface, writing your own shell

topics:
* file IO
  * creating ls
* concurrent
* network
  * making chatting program
* memory
  * make pool-based memory allocator
* error handling
* toolchain: preprocessor, compiler, linker
* cache
* assembly
* performance
* syncronization
