# Release Readiness Audit — GitHub Account `HeziLiu`

**Scope:** All public repositories under the GitHub account [HeziLiu](https://github.com/HeziLiu) (4 public repositories at audit time, including 2 forks).
**Checked per repository:** (1) git tags, (2) repository security advisories on record.
**Method:** Every repository was queried directly via the GitHub API; a repository returning no tags and/or no advisories is recorded explicitly as "none" — an empty result is a finding, not a gap in coverage.

---

## Headline findings

- **Repositories with no published tags: all four (4/4).**
  `Little-rookie`, `Big-Buzzard`, `CodingInterviewChinese2`, and `awesome-chatgpt-prompts-zh` each return **zero git tags**. None of the public work in this account currently carries any published tag, so there are no version markers (e.g. `v1.0.0`) available to anchor a release or a consumer-facing reference point.
- **Repositories carrying repository security advisories: none (0/4).**
  No repository in the account has a repository security advisory on record. Note: this reflects GitHub *repository security advisories* (maintainer-published advisories about that repository's own code); it is not a statement about upstream dependency vulnerabilities in forks.
- **Release-readiness read:** nothing in the account is currently versioned by tag, so any "release" conversation starts from a clean tagging baseline. No blocking security advisories exist on the repositories themselves.

---

## Per-repository results

### 1. `HeziLiu/Little-rookie` (original)

- URL: https://github.com/HeziLiu/Little-rookie
- Description: "Undergraduate coursework"
- Language: Java · Default branch: `master`
- **Git tags: none** — no tags have been published.
- **Repository security advisories: none** — no advisories on record.

### 2. `HeziLiu/Big-Buzzard` (original)

- URL: https://github.com/HeziLiu/Big-Buzzard
- Description: "For future...."
- Default branch: `master`
- **Git tags: none** — no tags have been published.
- **Repository security advisories: none** — no advisories on record.

### 3. `HeziLiu/CodingInterviewChinese2` (fork)

- URL: https://github.com/HeziLiu/CodingInterviewChinese2
- Description: 《剑指Offer》第二版源代码 ("Sword Finger Offer" 2nd edition source code)
- Language: C++ · Default branch: `master`
- **Git tags: none** — no tags exist on this fork (tag list is empty; any upstream tags were not carried into this fork's refs).
- **Repository security advisories: none** — no advisories on record.

### 4. `HeziLiu/awesome-chatgpt-prompts-zh` (fork)

- URL: https://github.com/HeziLiu/awesome-chatgpt-prompts-zh
- Description: ChatGPT 中文调教指南 (Chinese-language ChatGPT prompt guide)
- Default branch: `main`
- **Git tags: none** — no tags have been published.
- **Repository security advisories: none** — no advisories on record.

---

## Follow-up recommendations

1. **Tag something.** For any repository intended for release, cut and push at least an initial semver tag (`v0.1.0`) so consumers and CI have a fixed reference.
2. **Original vs fork split.** The two original repositories (`Little-rookie`, `Big-Buzzard`) are the release candidates; the two forks carry upstream code and should stay in sync with their upstreams or be explicitly retired from release scope.
3. **Advisory posture.** With zero repository security advisories anywhere, there is nothing to remediate at the repository level today — the remaining risk surface is dependency-level (out of scope for this audit).
