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
