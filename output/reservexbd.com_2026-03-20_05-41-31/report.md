# Attack Surface Mapping & Passive Reconnaissance Toolkit

- **Domain:** reservexbd.com
- **Date:** March 20, 2026 at 05:41 UTC
- **Version:** 1.0.0

## Executive Summary

- **Exposure Score:** 14/100
- **Exposure Level:** LOW EXPOSURE

## Score Breakdown

- SSL Issues: 0/20
- Missing Headers: 6/20
- DNS Issues: 3/15
- Admin Exposure: 3/15
- Tech Exposure: 1/10
- Wayback Risks: 0/10
- Surface Size: 1/10

## Findings

| ID | Category | Risk | Finding | Recommendation |
|---|---|---|---|---|
| HDR-001 | Security Headers | 🔴 HIGH | Content-Security-Policy header is missing | Implement a strict CSP policy tailored to required assets. |
| HDR-101 | Security Headers | 🔵 LOW | permissions-policy header is missing | Set a secure default for permissions-policy. |
| HDR-102 | Security Headers | 🔵 LOW | x-xss-protection header is missing | Set a secure default for x-xss-protection. |
| DNS-ORIGIN-001 | DNS | 🟠 MEDIUM | Potential origin IP exposure detected for CDN-protected infrastructure. | Restrict origin access to CDN egress ranges only. |
| DNS-DKIM-001 | DNS | 🔵 LOW | No DKIM hints discovered in queried TXT records. | Ensure DKIM selectors are configured for active mail domains. |

## Surface Highlights

- Subdomains discovered: 2
- Internal links mapped: 13
- API-like routes: 0
- Admin paths: 1

## Ethical Use

This report was generated passively for educational/authorized assessment purposes only.