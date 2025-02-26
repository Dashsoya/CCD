# SPF (Sender Policy Framework)

($dig "domain" TXT | grep spf)  
- $dig cyberdefenders.org TXT | grep spf

# DKIM (DomainKeys Identified Mail)

($dig "selector"._domainkey."domain" TXT | grep DKIM)  
- $dig google._domainkey.cyberdefenders.org TXT | grep DKIM


# DMARC (Domain-based Message Authentication, Reporting & Conformance)

($dig _darmc."domain" TXT | grep dmarc)  
- $dig _dmarc.nsa.gov TXT | grep dmarc  
- $dig _dmarc.google.com TXT | grep dmarc
