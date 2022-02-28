# binary-encryption
Original code about binary encryption from phrack
DacryFile 的存根则是一个简单的注入到被保护的二进制文件中的解密程序。 
DacryFile采用 RC4加密算法，从二进制文件的.text节一直加密到 text 
段的结尾。解密存根是一个用汇编语言和 C 语言写的简单程序，并不具备 
用户级执行的功能，只能够对加密过的代码进行解密。存根会被插入到 data 
段末尾，跟病毒插入寄生代码的机制类似。执行程序的入口点会被指向存 
根，在执行二进制程序时，存根会对程序的 text 段进行解密，然后将控制 
权交给原始的程序入口点![image](https://user-images.githubusercontent.com/40137669/155923273-459bf2ca-c106-404d-95c0-1c928e011858.png)
