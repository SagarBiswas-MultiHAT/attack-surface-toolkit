# Attack Surface Mapping & Passive Reconnaissance Toolkit

- **Domain:** google.com
- **Date:** March 20, 2026 at 05:47 UTC
- **Version:** 1.0.0

## Executive Summary

- **Exposure Score:** 17/100
- **Exposure Level:** LOW EXPOSURE

## Score Breakdown

- SSL Issues: 2/20
- Missing Headers: 11/20
- DNS Issues: 3/15
- Admin Exposure: 0/15
- Tech Exposure: 1/10
- Wayback Risks: 0/10
- Surface Size: 0/10

## Findings

| ID | Category | Risk | Finding | Recommendation |
|---|---|---|---|---|
| SSL-SAN-001 | SSL/TLS | 🟠 MEDIUM | SAN entries reveal internal/dev naming conventions. | Avoid exposing non-production hostnames in public certificates. |
| HDR-001 | Security Headers | 🔴 HIGH | Content-Security-Policy header is missing | Implement a strict CSP policy tailored to required assets. |
| HDR-003 | Security Headers | 🔴 HIGH | Strict-Transport-Security header is missing | Enable HSTS with an adequate max-age. |
| HDR-102 | Security Headers | 🔵 LOW | x-content-type-options header is missing | Set a secure default for x-content-type-options. |
| HDR-103 | Security Headers | 🔵 LOW | referrer-policy header is missing | Set a secure default for referrer-policy. |
| HDR-104 | Security Headers | 🔵 LOW | permissions-policy header is missing | Set a secure default for permissions-policy. |
| DNS-SPF-001 | DNS | 🟠 MEDIUM | SPF record missing or malformed. | Publish a valid SPF record to reduce spoofing risks. |
| DNS-DKIM-001 | DNS | 🔵 LOW | No DKIM hints discovered in queried TXT records. | Ensure DKIM selectors are configured for active mail domains. |

## Surface Highlights

- Subdomains discovered: 244
- Internal links mapped: 8
- API-like routes: 0
- Admin paths: 0

## Ethical Use

This report was generated passively for educational/authorized assessment purposes only.