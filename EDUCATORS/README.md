# Educators — OPENLAW

**Project:** OPENLAW  
**Category:** LEGAL_TECH  
**Upstream:** see BENCH.json  
**Pinned commit:** `7988e555824d170528aae719df5bf00644a9ae52`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `d222fae50ab68c2d9a647c33cc90df48495f71bbe573de9e72011b7393bd375d`  
**Date:** October 2026

## Teaching with OPENLAW

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `d222fae50ab68c2d9a647c33cc90df48495f71bbe573de9e72011b7393bd375d` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
