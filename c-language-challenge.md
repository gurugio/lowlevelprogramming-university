I think for long time, new C language programmer is getting rare.
As I'm solving the [Eudyptula Challenge](http://eudyptula-challenge.org/), an idea came to me that similar challenge is necessary for C language.

Usually book authors create some exercises carefully for each chapter in their books.
They hope that many readers solve the exercises and have got the alive wisdom.
You will get the dead kwowledge via reading text, but the alive wisdom via solving exercises and creating code.
Only some people solve the exercises and a few people solve the exercises correctly.

Here is a paradox.
If you are able to solve the exercises correctly, and have insight to the purpose of author, you are already having enough wisdom and do not need to read the book.
If you are not able to solve the exercises correctly, you are not able to get the wisdom via the book.

Here is a solution.
If somebody shows you a solution, you cannot realize Tao.
But if somebody review your solution and present the right direction, you will be able to realize Tao.
[Tao (The Way) that can be spoken of is not the Constant Tao’](https://en.wikipedia.org/wiki/Tao_Te_Ching)

[Do not satisfy with reading text. Start creating code.](http://www.taoism.net/living/2007/200701.htm)

# exercises of ["The C programming language: 2nd"](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)

0. Skip chapter 1 that introduce C language in one chapter and is not for C beginner
1. Solve the exercise 2-1
2. Submit a source into your github repository
3. Send me an issue including the address of your source
4. I or somebody will review your source
5. Change the code and review again
6. Repeate to the last exercise

# Following challenges are not started yet.

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
