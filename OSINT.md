

# Google Dorking

## Exact Match

```bash
"internal portal"
```

Searches for an exact phrase.

---

## Search Within a Domain

```bash
site:example.com
```

Restricts results to a specific domain.

Examples:

```bash
site:example.com login

site:example.com vpn

site:example.com admin
```

---

## File Discovery

### PDF

```bash
site:example.com filetype:pdf
```

### Word Documents

```bash
site:example.com filetype:docx
```

### Excel Documents

```bash
site:example.com filetype:xlsx
```

### PowerPoint

```bash
site:example.com filetype:pptx
```

---

## Title Searches

```bash
intitle:"index of"
```

Finds open directory listings.

Examples:

```bash
site:example.com intitle:"index of"

site:example.com intitle:"index of" backup

site:example.com intitle:"index of" passwords
```

---

## URL Searches

```bash
inurl:admin

inurl:login

inurl:portal

inurl:dashboard
```

Examples:

```bash
site:example.com inurl:admin

site:example.com inurl:login
```

---

## Text Searches

```bash
intext:"confidential"

intext:"internal use only"
```

Searches page content.

---

## Excluding Results

```bash
site:example.com -www
```

Exclude unwanted results.

Example:

```bash
site:example.com -www -shop
```

---

## OR Operator

```bash
site:example.com vpn OR remote
```

---

## Cached Pages

```bash
cache:example.com
```

View Google's cached version.

---

# Yandex

## Reverse Host Search

```bash
rhost:example.com
```

---

## File Discovery

```bash
mime:pdf

mime:docx

mime:xlsx
```

---

## Date Filtering

```bash
date:20240101..20241231
```

---

# Archive Recon

## Wayback Machine

Check:

- Old subdomains
    
- Old contact pages
    
- Old employee pages
    
- Legacy applications
    
- Previous infrastructure
    

Interesting findings:

```text
vpn.example.com
mail.example.com
legacy.example.com
dev.example.com
```

---

# Shodan

## Country

```bash
country:IN
```

## Product

```bash
product:nginx
```

## Port

```bash
port:443
```

## Operating System

```bash
os:Windows
```

## Network Range

```bash
net:192.168.1.0/24
```

---

## Useful Queries

### RDP

```bash
port:3389
```

### Jenkins

```bash
product:Jenkins
```

### Elasticsearch

```bash
product:Elasticsearch
```

### Citrix

```bash
product:Citrix
```

### Apache

```bash
product:Apache
```

---

# Useful OSINT Sites

## Certificate Transparency

```text
crt.sh
```

Used for:

- Subdomain discovery
    
- Historical certificates
    

---

## DNS Enumeration

```text
dnsdumpster.com
```

Used for:

- DNS records
    
- Subdomains
    
- Infrastructure mapping
    

---

## Breach Data

```text
haveibeenpwned.com
```

Used for:

- Breach verification
    
- Email exposure checks
    

---

# Workflow

1. Identify target domain
    
2. Search crt.sh
    
3. Enumerate subdomains
    
4. Check Wayback Machine
    
5. Search indexed documents
    
6. Review metadata
    
7. Check Shodan
    
8. Build infrastructure map
    
9. Correlate findings
    
10. Document everything