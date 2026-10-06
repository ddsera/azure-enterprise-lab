# Networking Notes (Week 1)

## Day 1: IP addresses and subnets
- A /24 means the first three numbers are the network part and the last
  number is the host part.
- Number of addresses = 2^(32 - prefix). Remember /24 = 256, then halve or double.
  /26 = 64, /22 = 1024, /16 = 65,536.
- A /22 holds four /24 subnets. 10.30.0.0/22 contains 10.30.0.0/24,
  10.30.1.0/24, 10.30.2.0/24 and 10.30.3.0/24.
- A /22 always starts on a clean boundary and covers four third-numbers.
  10.20.4.0/22 covers 4, 5, 6 and 7 (not 0 to 4).

## Mistakes I made and fixed
- I listed five third-numbers for a /22. A /22 covers exactly four,
  because 1024 / 256 = 4.

## Day 2: DNS and DHCP
- DNS (Domain Name System) translates names into IP addresses using records.
  A = name to IPv4, AAAA = name to IPv6, CNAME = alias, MX = mail,
  NS = name servers, TXT = free text/verification, SRV = service location.
- A name lookup checks the local cache, then the DNS server, which asks
  further servers until the owner of the domain answers.
- DHCP gives devices an IP address (Discover, Offer, Request, Acknowledge)
  plus a DNS server and a default gateway.
- In Azure, DHCP is built in. The default DNS address is 168.63.129.16.
  Set a VM's IP on its network interface, not inside the operating system.
- My Mac uses 192.168.1.1 (my router) as its DNS server. Home networks often
  use 192.168.x.x, which is why overlapping ranges are a real risk when
  connecting networks.

## Mistakes I made and fixed
- A /22 starting at 8 covers 8, 9, 10, 11 (I wrote 9 to 12). The starting
  number counts as the first.
