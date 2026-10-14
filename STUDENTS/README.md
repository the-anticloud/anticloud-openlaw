# Students — OPENLAW

**Project:** OPENLAW  
**Category:** LEGAL_TECH  
**Upstream:** see BENCH.json  
**Pinned commit:** `7988e555824d170528aae719df5bf00644a9ae52`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `d222fae50ab68c2d9a647c33cc90df48495f71bbe573de9e72011b7393bd375d`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `7988e555824d170528aae719df5bf00644a9ae52`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `d222fae50ab68c2d9a647c33cc90df48495f71bbe573de9e72011b7393bd375d`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
