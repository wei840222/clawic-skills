# Domain Management Research & Best Practices

## Domain Name System Security Extensions (DNSSEC)

DNSSEC adds cryptographic signatures to DNS data, allowing validating resolvers to verify the origin authenticity and integrity of signed DNS responses. ICANN publishes root-zone DNSSEC information, and its technical documentation explains the chain of trust from the root zone to signed delegations.

- **Root zone and trust chain:** ICANN manages the root-zone key-signing-key ceremony and publishes technical material for DNSSEC validation.
- **Deployment:** Major generic TLD registries can support DNSSEC, but a domain only gains end-to-end validation when its parent delegation and authoritative zone are configured correctly.
- **Operational caution:** Enable DNSSEC only when the registrar, DNS operator, and rollover process are understood; an incorrect DS record can make a domain unreachable to validating resolvers.

Sources:

- ICANN, *DNSSEC* — https://www.icann.org/resources/pages/dnssec-what-is-it-why-important-2019-03-05-en
- ICANN, *Root Zone DNSSEC* — https://www.iana.org/dnssec

## ICANN and Registrar Ecosystem

- **ICANN:** Coordinates policy for the DNS namespace and accredits registrars under the Registrar Accreditation Agreement.
- **Transfers:** ICANN's Transfer Policy covers registrar changes and transfer locks, including the common 60-day change-of-registrant and transfer restrictions.
- **Registration data:** Registration Data Policy governs collection, transfer, and publication of registration data; privacy and redaction practices vary by registry and jurisdiction.

Sources:

- ICANN, *Transfer Policy* — https://www.icann.org/resources/pages/transfer-policy-2016-06-01-en
- ICANN, *Registrar Accreditation* — https://www.icann.org/resources/pages/accreditation-2012-02-25-en
- ICANN, *Registration Data Policy* — https://www.icann.org/resources/pages/registration-data-policy-2024-02-21-en

## Additional Domain Security Best Practices

- **Registrar lock:** `clientTransferProhibited` is an EPP status that prevents a registrar from processing a transfer until it is removed.
- **WHOIS/RDAP data:** Use the registrar's privacy controls where available and confirm the authoritative registration-data service through RDAP.

Sources:

- ICANN, *EPP Status Codes* — https://www.icann.org/resources/pages/epp-status-codes-2014-06-16-en
- ICANN, *Registration Data Lookup Tool (RDAP)* — https://lookup.icann.org/en
