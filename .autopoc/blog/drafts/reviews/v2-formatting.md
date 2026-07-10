# Formatting Review -- v2

## Scores
| Dimension | Raw (1-10) | Weight | Weighted |
|---|---|---|---|
| Heading hierarchy | 8 | 1x | 8 |
| Code formatting | 9 | 1x | 9 |
| CTA placement | 6 | 2x | 12 |
| SEO readiness | 7 | 1x | 7 |
| Link strategy | 6 | 1x | 6 |
| Editorial compliance | 8 | 2x | 16 |
| Brand standards | 8 | 1x | 8 |
| Word count | 8 | 1x | 8 |
| **Total** | | | **74 / 100 -> 7.4** |

## Line-Level Feedback

### Heading hierarchy
- **Location**: Lines 24, 28, 50, 61, 105, 124, 163, 198, 206
- **Issue**: All headings are H2, forming a clean cascade with no H1 in the body and no skipped levels. Headings are in sentence case, which is correct. However, the title heading (line 24) "Containerizing cc-fleet: a Go command-line tool for LLM orchestration meets OpenShift" should capitalize the first word after the colon per sentence case rules ("a" -> "A").
- **Suggestion**: Change to "Containerizing cc-fleet: A Go command-line tool for LLM orchestration meets OpenShift". Also consider whether H3 subheadings would help break up the longer sections (e.g., "What we learned" could benefit from H3s for each lesson).

### Code formatting
- **Location**: Code blocks throughout
- **Issue**: All code is in proper fenced code blocks with language identifiers (dockerfile, bash, yaml, mermaid). No inline backticks found in prose text, which is correct per the changelog. Code is real and runnable. The CLI output blocks (lines 175-183, 188-194) lack a language identifier; they should use a generic identifier or none, which is acceptable.
- **Suggestion**: No changes needed. This is well-handled.

### CTA placement
- **Location**: Lines 206-219 (end only)
- **Issue**: The CTA appears only at the end of the post. The rubric requires CTAs near top, mid, and closing for a score of 10. There is no early CTA (e.g., a link to Red Hat OpenShift AI or UBI documentation in the first few sections) and no mid-post CTA. The closing CTA links to OpenShift AI correctly, but "OpenShift builds" and "UBI base images" are mentioned without hyperlinks.
- **Suggestion**: Add a link to Red Hat OpenShift AI or UBI docs in the "Building with Universal Base Image multi-stage Dockerfiles" section (natural placement). Add a mid-article link in the "OpenShift binary builds" section, e.g., linking "binary build strategy" to OpenShift documentation. Make "OpenShift builds" and "UBI base images" in the final sentence into actual hyperlinks.

### SEO readiness
- **Location**: Title (line 24)
- **Issue**: The title is 76 characters ("Containerizing cc-fleet: a Go command-line tool for LLM orchestration meets OpenShift"), which exceeds the 50-60 character recommendation. Keywords "containerizing," "Go," "OpenShift" are present, which is good. The keyword "containerize" appears in the first paragraph.
- **Suggestion**: Shorten the title. Consider: "Containerizing a Go CLI tool on OpenShift" (41 chars) or "Containerizing cc-fleet: Go CLI meets OpenShift" (48 chars). The subtitle detail can move into the opening paragraph.

### Link strategy
- **Location**: Lines 217-219
- **Issue**: There are 2 links total: one to GitHub (external, not a competitor) and one to redhat.com (OpenShift AI). The post lacks internal links to other Red Hat resources. Key terms that should link to Red Hat docs: "Universal Base Images (UBI)" (first mention, line 63), "binary build strategy" (line 107), "OpenShift builds" (line 219), "UBI base images" (line 219). The GitHub links are appropriate for the artifacts.
- **Suggestion**: Add links to:
  - UBI documentation at first mention (line 63)
  - OpenShift binary builds documentation (line 107)
  - Make the final sentence's references into actual hyperlinks

### Editorial compliance
- **Location**: Line 26
- **Issue**: Grammatical error: "a tool that tightly coupled" should be "a tool that's tightly coupled."

- **Location**: Line 26
- **Issue**: Acronyms are expanded on first use: LLM (line 26), TUI (line 26), CLI (line 32), UBI (line 63). Good.

- **Location**: Lines 30, 32, 217
- **Issue**: Oxford commas are used consistently ("managing provider profiles, routing API keys through pluggable secret backends, and spawning teammate sessions"; "the Dockerfile, Kubernetes manifests, and the full PoC report"). Good.

- **Location**: Throughout
- **Issue**: Contractions used appropriately ("It's," "doesn't," "That's," "don't"). Good.

- **Location**: Line 14 (abstract mentions "Open Data Hub")
- **Issue**: "Open Data Hub" appears in the abstract but not in the blog post. If it's a relevant product, it should be mentioned; if not, it shouldn't be in the abstract. Minor concern only.

### Brand standards
- **Location**: Mermaid diagrams
- **Issue**: All 3 Mermaid diagrams include the `%%{init}%%` directive with Red Hat brand colors (#EE0000, #A30000, #6A6E73, #F0F0F0, #0066CC). This is correct. The image placeholder also references the correct hex codes.
- **Suggestion**: No changes needed.

### Word count
- **Location**: Whole post
- **Issue**: Approximately 757 words of prose content (excluding code blocks, Mermaid diagrams, image placeholders, and the changelog comment). The rubric suggests 800-1300 for tutorials. At 757, this is slightly under the low end but close enough that the post doesn't feel thin. Including code and diagrams, total content is around 1347 words, which is appropriate.
- **Suggestion**: The additional prose suggested in other dimensions (CTA links, limitation acknowledgments, binary build explanation) would bring the word count into the 800+ range naturally.

## Editorial Compliance Checklist
- [x] Sentence case headings
- [x] Oxford commas
- [x] No inline backticks
- [x] Full product name on first mention (Red Hat OpenShift, Red Hat Universal Base Images)
- [x] Acronyms expanded on first use
- [x] Contractions used
- [x] No em dashes
- [x] Numerals in running text ("391 Go source files," "30+ internal packages")
- [ ] Capitalize after colon in title (line 24: "a" should be "A")
- [ ] Grammar fix needed (line 26: "that tightly coupled")
- [x] No H1 in body

## Summary
The single most important formatting change: add CTAs at top and mid-post. The current post only has a CTA at the end. Linking "Universal Base Images (UBI)" to Red Hat docs when first mentioned (line 63) and linking "binary build strategy" to OpenShift docs (line 107) would address both the CTA placement score and the link strategy score simultaneously.
