# Netflix and CTF
- - -
**Description**

I don't like watching anything other than TV shows about Space Heroes.

**Author:** v10l3nt

**File Location**

Pcap can be found in ctf-writeups/Space-Heroes/files/netflix-and-chill.pcap

- - -

Examining the HTTP traffic and following the stream, we can see POST requests showing keypresses. We can clear things up by selecting to see only the client messages, 10.10.100.139:51426 -> 10.10.100.124:8060.

Scrolling down we will see output like this:
```
  

POST /keypress/Lit_s HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_h HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_c HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_t HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_f HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_%7B HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_T HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_1 HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_m HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_3 HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_- HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_i HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_s HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_- HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_t HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_h HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0

  

POST /keypress/Lit_3 HTTP/1.1

Host: 10.10.100.124:8060

User-Agent: python-requests/2.27.1

Accept-Encoding: gzip, deflate

Accept: */*

Connection: keep-alive

Content-Length: 0
```

Each keypress/Lit_ event tells us what letter is being written. There are some TV shows in here but reading further down we will encounter the flag written out one character at a time.

- - -
**Flag**

shctf{T1m3-is-th3-ultimat3-curr3Ncy}