# [ROKSO list](https://www.spamhaus.org/rokso/)

Test address verifiers:

```sh
$ nslookup 2.0.0.127.zen.spamhaus.org 1.1.1.1
Server:		1.1.1.1
Address:	1.1.1.1#53

Non-authoritative answer:
Name:	2.0.0.127.zen.spamhaus.org
Address: 127.0.0.2
Name:	2.0.0.127.zen.spamhaus.org
Address: 127.0.0.10
Name:	2.0.0.127.zen.spamhaus.org
Address: 127.0.0.4

$ nslookup dbltest.com.dbl.spamhaus.org 1.1.1.1
Server:		1.1.1.1
Address:	1.1.1.1#53

Non-authoritative answer:
Name:	dbltest.com.dbl.spamhaus.org
Address: 127.0.1.2

```

### Issues

Getting random:

```sh
$ nslookup 2.0.0.127.zen.spamhaus.org 1.1.1.1
Server:		1.1.1.1
Address:	1.1.1.1#53

Non-authoritative answer:
Name:	2.0.0.127.zen.spamhaus.org
Address: 127.255.255.254

```

... ie, using public DNS server in lookup. Not sure how to handle that.
