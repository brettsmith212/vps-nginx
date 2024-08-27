# VPS Nginx Proxy

1. DNS Configuration:
   For each domain, you'll need to set up an A record in your DNS settings. An A record maps a domain name to an IPv4 address.

   For all three domains, set the A record to point to xx.xx.xxx.xxx:

   example1.com -> A record -> xx.xx.xxx.xxx
   example2.com -> A record -> xx.xx.xxx.xxx
   example3.com -> A record -> xx.xx.xxx.xxx

   You don't specify the port in DNS records.

2. Reverse Proxy:
   Since you want to map different domains to different ports on the same IP address, you'll need to set up a reverse proxy server (like Nginx or Apache) on your server at xx.xx.xxx.xxx. The reverse proxy will listen on port 80 (HTTP) and/or 443 (HTTPS) and forward requests to the appropriate internal port based on the domain name.

3. SSL/TLS (Optional but recommended):
  If you want to use HTTPS, you'll need to obtain SSL certificates for your domains and configure your reverse proxy to use them.

4. Firewall:
  Ensure that your server's firewall allows incoming traffic on ports 80 and 443 (if using HTTPS).
