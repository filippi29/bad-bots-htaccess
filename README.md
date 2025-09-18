# Bad Bot Prevention for .htaccess

This repository contains snippets to block malicious bots and scrapers using `.htaccess` (Apache).

## Contents

- **`htaccess-full.conf`**  
  A full list with hundreds of User-Agents from known bad bots.  
  !!! The original list comes from another creator (publicly shared project), but I have added my own rules on top of it to make it more complete and up to date.

- **`htaccess-light.conf`**  
  A smaller and lightweight version, ideal for small personal sites or portfolios.  
  !!! It only includes the most common and harmful bots (e.g., `curl`, `wget`, `sqlmap`, `HTTrack`, `python-requests`).

## How to Use

1. Copy the content of the file you want (`htaccess-full.conf` or `htaccess-light.conf`).  
2. Paste it into your `.htaccess` file on your Apache server.  
3. **Always test in staging first**

## Why Use This?

- Protects against scraping tools such as `wget`, `curl`, `HTTrack`.  
- Blocks penetration testing tools like `sqlmap` and `nikto`.  
- Reduces unnecessary traffic and log spam from known bots.  
- Lightweight solution for sites without a CDN or dedicated firewall.

## Note

While these snippets are useful, the best practice for larger projects is to rely on **firewall rules** (e.g., Cloudflare, mod_security, fail2ban) for better performance and flexibility.
