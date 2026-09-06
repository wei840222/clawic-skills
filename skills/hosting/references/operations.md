# Hosting Operations

## DNS and HTTPS

Choose one operating model:

- Delegate nameservers to the hosting provider for a simpler setup with less DNS control.
- Retain DNS with an independent provider and add the host’s A, AAAA, CNAME, or verification records for more control.

After every DNS change, confirm the intended records resolve and HTTPS serves the correct certificate. Plan a migration overlap because DNS changes can take time to propagate.

## Email

Web and email hosting are separate services. Keep MX, SPF, DKIM, and DMARC records with the mail provider’s documented setup. Confirm that web-host DNS changes preserve the existing mail records.

## Backups and Cost

Record file and database backup scope, frequency, retention, location, and restore owner. Test restoration before relying on it. Compare monthly and annual commitments, included usage, overage pricing, and add-ons against realistic traffic.

## Migration

Export portable content and data, document the running configuration, lower DNS TTL only when the provider guidance supports it, and keep the old service available until the new service and rollback path are verified.
