# Formatting Review -- v1

## Scores

| Dimension | Weight | Score (1-10) | Weighted |
|---|---|---|---|
| Heading hierarchy | 1x | 7 | 7 |
| Code formatting | 1x | 4 | 4 |
| CTA placement | 2x | 4 | 8 |
| SEO readiness | 1x | 7 | 7 |
| Link strategy | 1x | 3 | 3 |
| Editorial compliance | 2x | 6 | 12 |
| Brand standards | 1x | 5 | 5 |
| Word count | 1x | 9 | 9 |

**Weighted total: 55 / 100**
**Normalized score: 5.5 / 10**

---

## Line-level feedback

### Heading hierarchy

- **Line 1:** Title uses H2, which is correct (no H1 in body). Good.
- **Lines 5, 11, 22, 53, 82, 111, 132:** All body sections use H2, maintaining a flat cascade. Acceptable, though H3 subsections would improve scannability in the longer sections.
- **Lines 111 and 124:** "Test results and what we learned" (H2) is immediately followed by "What we learned" (H2). These are redundant headings that should be merged into a single section.
- **Line 5:** "What is cc-fleet?" -- sentence case, correct.
- **Line 22:** "Building with UBI multi-stage Dockerfiles" -- "Dockerfiles" is fine, "UBI" is an acronym. Correct.
- **Line 53:** "OpenShift binary builds: from source to registry" -- sentence case with correct capitalization after colon. Good.

### Code formatting

- **Lines 47-51:** Inline backticks are used heavily: `` `CGO_ENABLED=0` ``, `` `-ldflags="-s -w"` ``, `` `chgrp -R 0` ``, `` `chmod -R g=u` ``, `` `USER 1001` ``, `` `ubi-minimal` ``. The rubric explicitly states "no backticks" in final output. These must be reformatted to use monospace styling or written out in prose without backtick markers.
- **Line 126:** Inline backtick on `` `CGO_ENABLED=0` ``.
- **Line 128:** Inline backticks on `` `version` ``, `` `cc-fleet version` ``, `` `--version` ``.
- **Line 134:** Inline backtick on `` `quay.io/aicatalyst/cc-fleet:latest` ``.
- Code blocks (lines 26-43, 57-69, 86-107, 137-139) use proper fenced syntax with language hints. The code is real and runnable. Good.

### CTA placement

- **Line 132-145:** CTA appears only at the very end of the post ("Try it yourself"). No CTA near the top or mid-article.
- No links to redhat.com anywhere in the CTA or elsewhere in the post. The rubric requires CTAs linked to redhat.com.
- The abstract specifies a CTA about the AutoPoC pipeline, which is present but not linked to any Red Hat property.

### SEO readiness

- **Line 1:** Title is "Containerizing cc-fleet: Bringing a Go CLI for LLM orchestration to OpenShift" -- 72 characters. Exceeds the 50-60 char ideal. Consider shortening.
- **Line 3:** First paragraph contains keywords: "containerizing," "Go CLI," "LLM providers," "Red Hat OpenShift," "UBI-based container images." Good keyword density.
- Target keywords are present but the title is too long for optimal SEO.

### Link strategy

- **Lines 142-145:** All 3 links point to github.com/aicatalyst-team, not redhat.com. No internal links to Red Hat properties (developers.redhat.com, access.redhat.com, docs.openshift.com).
- No links to Red Hat OpenShift documentation, UBI documentation, or Red Hat Developer resources.
- registry.access.redhat.com appears in code blocks (lines 28, 36) but not as editorial links.

### Editorial compliance

- **Oxford commas:** Present and consistent (lines 7, 9, 72, 122). Good.
- **Contractions:** Used well throughout: "don't" (line 3), "It's" (line 9), "doesn't" (line 47). Good.
- **Product names:** "Red Hat OpenShift" appears correctly at first mention (line 3). Subsequent mentions use just "OpenShift" (lines 49, 53, 55, 77), which is acceptable. However, "UBI" is never expanded to "Universal Base Image" on first use (line 3 says "UBI-based" without expansion; line 22 uses "UBI" again without expansion).
- **Line 3:** "LLM" is not expanded on first use. Should be "large language model (LLM)."
- **Line 9:** "CLI" is not expanded on first use. Should be "command-line interface (CLI)." (Note: "command-line tool" appears on line 7, which partially covers this, but the acronym CLI itself isn't formally introduced.)
- **Line 9:** "TUI" is not expanded. Should be "terminal user interface (TUI)."
- **Line 3:** "Red Hat OpenShift" -- correct. But "OpenShift AI" from the abstract's product list never appears in the post body.
- **Em dashes:** None found. Good.
- **Numerals:** "391" (line 9), "30+" (lines 9, 117, 122), "10" (line 118), "two minutes" (line 72). Line 72 should be "2 minutes" per the numerals-in-running-text rule.

### Brand standards

- No reference to Red Hat fonts or colors except in the Mermaid diagram theme variables (line 75: `primaryColor: '#EE0000'`), which correctly uses the Red Hat red.
- The Mermaid diagram (lines 74-80) includes Red Hat brand colors, which is a good touch.
- No mention of "Red Hat OpenShift AI" or "Open Data Hub," both listed as products in the abstract.

### Word count

- 972 words including code blocks. The rubric targets 800-1300 for tutorials. This is within range. Good.

---

## Editorial compliance checklist

| Rule | Status | Notes |
|---|---|---|
| Sentence case headings | Pass | All headings use sentence case correctly |
| Oxford commas | Pass | Consistently applied |
| No backticks | **Fail** | 8+ instances of inline backticks (lines 47-51, 126, 128, 134) |
| Full product name first mention | **Fail** | UBI, LLM, CLI, TUI not expanded on first use |
| Lowercase component descriptors | Pass | No issues found |
| No H1 in body | Pass | All body headings are H2 |
| Expand acronyms on first use | **Fail** | UBI, LLM, CLI, TUI unexpanded |
| Use contractions | Pass | Good use throughout |
| Numerals in running text | **Fail** | "two minutes" on line 72 should be "2 minutes" |
| No em dashes | Pass | None found |

---

## Summary

The draft has solid structural bones: clean heading hierarchy, well-formatted code blocks with real runnable commands, good use of contractions and Oxford commas, and appropriate word count. The main issues are:

1. **Backticks (blocking):** 8+ inline backtick instances must be removed. Rewrite these as prose or use a formatting approach compatible with the Red Hat Developer Blog CMS.
2. **Acronym expansion (blocking):** UBI, LLM, CLI, and TUI all need expansion on first use.
3. **CTA placement and linking (significant):** The CTA only appears at the end and links exclusively to GitHub. Add a CTA near the introduction and mid-article, and link to redhat.com properties (OpenShift docs, UBI docs, Red Hat Developer).
4. **Link strategy (significant):** Zero internal links to Red Hat domains. Add links to OpenShift documentation, UBI registry documentation, and developers.redhat.com resources.
5. **Duplicate heading (minor):** "Test results and what we learned" (line 111) and "What we learned" (line 124) should be merged.
6. **Product name gaps (minor):** The abstract lists "Red Hat OpenShift AI" and "Open Data Hub" as featured products, but neither appears in the post body. Align the post with the abstract or update the abstract.
7. **Title length (minor):** At 72 characters, the title exceeds the 50-60 char SEO ideal.
