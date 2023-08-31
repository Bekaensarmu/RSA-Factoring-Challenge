RSA-Factoring-Challenge

Description

This project is designed to factorize as many numbers as possible into a product of two smaller numbers. It works perfectly for that except the case of bignums (numbers bigger than long long unsigned integers) please any contribution towards making this project work for bignums will be highly appreciated.

Information

The server generates two large prime numbers, and multiplies them together. This is called the "public key". This key is made available to any client which wishes to transmit data securely to the server. The client uses this "public key" to encrypt data it wishes to send. Now because this is an asymmetric algorithm, the public key cannot be used to decrypt the transmitted data, only encrypt it. In order to decrypt, you need the original prime numbers, and only the server has these (the "private key"). On receiving the encrypted data, the server uses its private key to decrypt the transmission.


In the case of you browsing the web, your browser gives the server its public key. The server uses this key to encrypt data to be sent to your browser, which then uses its private key to decrypt.

Tasks

0. Factorize all the things!


Factorize as many numbers as possible into a product of two smaller numbers.


julien@ubuntu:~/factors$ cat tests/test00 

4

12

34

128

1024

4958

1718944270642558716715

9

99

999

9999

9797973

49


239809320265259

julien@ubuntu:~/factors$ time ./factors tests/test00

4=2*2

12=6*2

34=17*2

128=64*2

1024=512*2

4958=2479*2

1718944270642558716715=343788854128511743343*5

9=3*3

99=33*3

999=333*3

9999=3333*3

9797973=3265991*3

49=7*7

239809320265259=15485783*15485773


real    0m0.009s

user    0m0.008s

sys 0m0.001s

julien@ubuntu:~/factors$ 


1. RSA Factoring Challenge

RSA Laboratories states that: for each RSA number n, there exist prime numbers p and q such that


julien@ubuntu:~/RSA Factoring Challenge$ cat tests/rsa-1

6

julien@ubuntu:~/RSA Factoring Challenge$ ./rsa tests/rsa-1

6=3*2

julien@ubuntu:~/RSA Factoring Challenge$ cat tests/rsa-2

77

julien@ubuntu:~/RSA Factoring Challenge$ ./rsa tests/rsa-2

77=11*7

julien@ubuntu:~/RSA Factoring Challenge$ [...]  

julien@ubuntu:~/RSA Factoring Challenge$ cat tests/rsa-15

239821585064027

julien@ubuntu:~/RSA Factoring Challenge$ ./rsa tests/rsa-15 

239821585064027=15486481*15485867

julien@ubuntu:~/RSA Factoring Challenge$ cat tests/rsa-16

2497885147362973

julien@ubuntu:~/RSA Factoring Challenge$ ./rsa tests/rsa-16

2497885147362973=49979141*49978553

julien@ubuntu:~/RSA Factoring Challenge$ [...]

Author

Bekaensarmu


