I think for long time, new C language programmer is getting rare.
As I'm solving the Eudyptula Challenge, an idea came to me that similar challenge is necessary for C language.

I'm not sure what tasks are suitable and how mant tasks are necessary..actually I have no plan yet.
But I'll write some tasks from printing "hello-world" to making a class with a function pointer.
If you have an idea, please send me pull-request.

[discussion on reddit](https://www.reddit.com/r/linuxdev/comments/5r8k6g/new_service_like_the_eudyptula_challenge/)
* pnpbios
  * Writing your own daemon, your own PAM module, writing a custom network interface, writing your own shell

# task01

Use argc and argv to print "Hello world!".

```
$ print 3 "Hello world!"
1 Hello world!
2 Hello world!
3 Hello world!
```
# task??

Make a daemon that log a message "I'm running" every minute.

```
$ tail /var/log/syslog
Dec  5 10:52:25 username mydaemon[1058]: I'm running
Dec  5 10:57:25 username mydaemon[1058]: I'm running
Dec  5 11:02:25 username mydaemon[1058]: I'm running
Dec  5 11:07:25 username mydaemon[1058]: I'm running
```
# task??

Make a 1:1 chatting program for terminal

# task??

Make serial number certification program
* certificate a serial number file
* read .rc file to specify serial number format
* encode user information, user-account number, name, product id, in serial number
* decode the information from the serial number

```
$ cat spec.txt
# field length
account 4
name 16
product 4

$ encode-serial
account: 1234 <user-input>
name: gogostar <user-input>
product: 5678 <user-input>
abcd-defg-xxxx-xxxx <output>

$ decode-serial
serial: abcd-defg-xxxx-xxxx <input>
account: 1234
name: gogostar
product: 5678
````

# task20

make your own shell
* features
  * pipe, indirection
* design

