# PWN Tools

pwntools is a python libary for writing exploits.

> importing
from pwn import *

> when writing an exploit for a binary exploitation: addresses like this or with p64()
address = p32(0xb33f69)

> open a connection
r = remote(<host>, <port>)

> waiting for specific string until the program resumes
r.recvuntil("Please wait")

> send payload
r.sendline(<payload>)

> save repsonse
response = r.recvall(4096)

> close connection
r.close()
