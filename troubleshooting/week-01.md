# Troubleshooting: Week 1

## Name does not resolve, but the IP works
- **Symptom:** a user opens http://10.1.0.20 but not
  http://files.corp.example.com.
- **Likely cause:** DNS, not the network. The server is reachable, so the
  name is not being translated.
- **Checks:** run nslookup on the name; check which DNS server the client
  uses; look for a missing or wrong A record; clear the local DNS cache.
- **Prevention:** keep DNS records documented and monitor the DNS servers.
