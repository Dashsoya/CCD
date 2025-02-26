# SPF (Sender Policy Framework)
Allows domain owner to specify which mail servers are authorized to send emails for that domain.

($dig "domain" TXT | grep spf)  
- $dig cyberdefenders.org TXT | grep spf

# DKIM (DomainKeys Identified Mail)
Email authentication system that allows the receving mail server to check that the email was indeed sent and authorized by the domain owner. (Validates the sending mail server's digital signature attached)

($dig "selector"._domainkey."domain" TXT | grep DKIM)  
- $dig google._domainkey.cyberdefenders.org TXT | grep DKIM


# DMARC (Domain-based Message Authentication, Reporting & Conformance)
Uses SPF and DKIM to verify the address in the "From" header is the actual sender of the message.

- Control: Provides domain owner complete control to set policy for subsequent actions when receiving mails that fail SPF/DKIM verification.

- Visibility: Provides domain owner visibility and reports on who is sending emails from their domains to ensure only legitimate emails are received.

($dig _darmc."domain" TXT | grep dmarc)  
- $dig _dmarc.nsa.gov TXT | grep dmarc  
- $dig _dmarc.google.com TXT | grep dmarc
