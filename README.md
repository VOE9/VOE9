### Independent security researcher.

I build small, focused tools that help human researchers triage faster — heuristic, source-grounded, and honest about their own false positives. No model in the loop for detection, so nothing here can hallucinate a finding: every output traces back to a real commit, diff, or published record a human can click and verify.

**Status:** all three tools below are early-stage and independently developed. Read each one's `METHODOLOGY.md` before trusting a result.

---

**[cve-explain](https://github.com/VOE9/cve-explain)** — turns a CVE ID into a plain-language explanation grounded entirely in NVD, EPSS, and GHSA data.

**[regression-hunter](https://github.com/VOE9/regression-hunter)** — variant analysis: finds candidate files that may not have received a project's own previously-published security fix, seeded from that project's real advisory history.

**[silent-patch-finder](https://github.com/VOE9/silent-patch-finder)** — scans commit history for undisclosed security fixes: a defensive-shaped diff paired with a commit message that doesn't say so.

---

Every tool here produces *candidates for manual review*, never verdicts. Verification, judgment, and the actual report stay a human's job — on purpose.
