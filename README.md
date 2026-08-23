### Independent security researcher.

I build small, focused tools that help human researchers triage faster — heuristic or structurally-grounded, and honest about their own false positives. No model in the loop for detection, so nothing here can hallucinate a finding: every output traces back to a real commit, diff, git history, or published record a human can click and verify.

**Status:** all tools below are early-stage and independently developed. Read each one's `METHODOLOGY.md` before trusting a result — every one of them documents real bugs found during its own development, not just the happy path.

---

#### Tools

**[augur](https://github.com/VOE9/augur)** — three sections: `radar` flags commits in a local git clone that look like undisclosed security fixes; `harness` attempts an automatic differential AddressSanitizer proof for a real bug shape, deriving its own test input mechanically from the target function's source; `provenance` finds when a vulnerable pattern was actually introduced (structurally, not "last commit that touched the line" like classic SZZ) and maps it to the real tagged versions affected. Validated against a real, external repository's actual merged fix, independently re-checked by hand — see its `METHODOLOGY.md`.

**[cve-explain](https://github.com/VOE9/cve-explain)** — turns a CVE ID into a plain-language explanation grounded entirely in NVD, EPSS, and GHSA data — including the actual fix commit's diff, when one is linked.

**[regression-hunter](https://github.com/VOE9/regression-hunter)** — variant analysis: finds candidate files that may not have received a project's own previously-published security fix, seeded from that project's real advisory history.

**[silent-patch-finder](https://github.com/VOE9/silent-patch-finder)** — scans commit history for undisclosed security fixes: a defensive-shaped diff paired with a commit message that doesn't say so.

---

#### Selected upstream contributions

Small, verified fixes found by reading real projects' code and confirming the bug empirically before proposing anything — not by scanning at scale.

- [kaist-hacking/RTCON#2](https://github.com/kaist-hacking/RTCON/pull/2) — merged. Bounded an unchecked `memcpy` in crash-deduplication logic; reproduced the exact fault with AddressSanitizer before and after.
- [B2R2-org/B2R2#501](https://github.com/B2R2-org/B2R2/pull/501) — merged. Fixed a DEBUG/RELEASE behavioral divergence in the SSA lifter's root-selection logic; verified with the project's own real test suite.
- Open: [zardus/preeny#90](https://github.com/zardus/preeny/pull/90), [compsec-snu/petal#2](https://github.com/compsec-snu/petal/pull/2), [postech-compsec/swarmbox#13](https://github.com/postech-compsec/swarmbox/pull/13), [WOOSEUNGHOON/Centris-public#7](https://github.com/WOOSEUNGHOON/Centris-public/pull/7)

---

Every tool here produces *candidates for manual review*, never verdicts. Verification, judgment, and the actual report stay a human's job — on purpose.

---

Applying for a research-focused CS master's, Fall 2027 — interested in vulnerability discovery & security patch analysis.
