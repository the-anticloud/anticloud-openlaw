# Independent Insurance — OPENLAW

**Project:** OPENLAW  
**Category:** LEGAL_TECH  
**Upstream:** see BENCH.json  
**Pinned commit:** `7988e555824d170528aae719df5bf00644a9ae52`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `d222fae50ab68c2d9a647c33cc90df48495f71bbe573de9e72011b7393bd375d`  
**Date:** October 2026

## Why AI-specific cover matters

Deploying AI in a regulated sector creates liability surfaces that ordinary
technology cover does not reach: inference liability, audit-trail liability,
data-breach liability and IP-infringement liability.

## How this project's architecture reduces insurable risk

| Risk | Cloud AI | OPENLAW with AIOSS |
|---|---|---|
| Audit-trail loss | high — vendor-controlled logs | low — append-only chain, verifiable offline |
| Data breach in transit | high — data transits external servers | low — no external endpoint |
| Compliance violation | high — cannot satisfy air-gap requirements | low — structural |
| IP liability | moderate | low — pinned provenance chain |

## Evidence package for an insurer

- AIOSS chain verification for head `d222fae50ab68c2d9a647c33cc90df48495f71bbe573de9e72011b7393bd375d`
- The 16-check register with per-check evidence hashes
- Framework control mapping in `BENCH.json`

## Contact

lois@0-1.gg
