# Attack Surface Mapping & Passive Reconnaissance Toolkit

- **Domain:** sagarbiswas-multihat.github.io
- **Date:** March 20, 2026 at 05:52 UTC
- **Version:** 1.0.0

## Executive Summary

- **Exposure Score:** 24/100
- **Exposure Level:** LOW EXPOSURE

## Score Breakdown

- SSL Issues: 0/20
- Missing Headers: 14/20
- DNS Issues: 5/15
- Admin Exposure: 0/15
- Tech Exposure: 2/10
- Wayback Risks: 0/10
- Surface Size: 3/10

## Findings

| ID | Category | Risk | Finding | Recommendation |
|---|---|---|---|---|
| HDR-001 | Security Headers | 🔴 HIGH | Content-Security-Policy header is missing | Implement a strict CSP policy tailored to required assets. |
| HDR-004 | Security Headers | 🟠 MEDIUM | X-Frame-Options header is missing | Set X-Frame-Options to DENY or SAMEORIGIN. |
| HDR-005 | Security Headers | 🔴 HIGH | CORS policy allows wildcard origin (*) | Restrict CORS origins to trusted domains. |
| HDR-103 | Security Headers | 🔵 LOW | x-content-type-options header is missing | Set a secure default for x-content-type-options. |
| HDR-104 | Security Headers | 🔵 LOW | referrer-policy header is missing | Set a secure default for referrer-policy. |
| HDR-105 | Security Headers | 🔵 LOW | permissions-policy header is missing | Set a secure default for permissions-policy. |
| HDR-106 | Security Headers | 🔵 LOW | x-xss-protection header is missing | Set a secure default for x-xss-protection. |
| DNS-SPF-001 | DNS | 🟠 MEDIUM | SPF record missing or malformed. | Publish a valid SPF record to reduce spoofing risks. |
| DNS-DMARC-001 | DNS | 🟠 MEDIUM | DMARC record missing or invalid. | Configure DMARC with monitoring and enforcement policy. |
| DNS-DKIM-001 | DNS | 🔵 LOW | No DKIM hints discovered in queried TXT records. | Ensure DKIM selectors are configured for active mail domains. |

## Surface Highlights

- Subdomains discovered: 0
- Internal links mapped: 32
- API-like routes: 0
- Admin paths: 0

## Ethical Use

This report was generated passively for educational/authorized assessment purposes only.