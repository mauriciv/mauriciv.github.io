---
layout: post
title: "DNS, a mini introduction"
---

Every website you visit resides on a sever (which is just a fancy name for a computer that "serves" content to other computers. Confusingly, it is also the name given to the *software* inside a computer that handles web requests, like Apache) and in order for your machine to get in touch with a server and ask for a web page, it needs to know the server's IP address. So you just need to type the IP address of the server in your browser!

... Yeah, that's not how we do it. Humans are terrible at remembering arbitrary sequences of numbers. It is easier for us to remember "github.com" than 192.30.253.112 .

So how does your computer get the IP address it needs?

From a name server.

A name server is just a machine that stores domain names and their corresponding IP addresses.

The name servers of the world constitute what is know as DNS (Domain Name System).

When you type "www.google.com" in a browser, your computer asks a name server for an IP address matching what you typed. If the server doesn't have the address, it asks *another* name server for the address, and so forth. (By the way, if you are wondering how does your computer know the IP address of the first server in the chain, it is specified in your computer's network configuration)

I simplified things quite a lot, there are different types of name servers (authoritative, recursive), different software to manage the server ([bind9](http://www.bind9.net/), [dnsmasq](http://www.thekelleys.org.uk/dnsmasq/doc.html)) but that is DNS in a nutshell.
