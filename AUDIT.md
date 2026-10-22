# Release Readiness Audit

Portfolio-review audit of every repository under the GitHub account **HeziLiu**, compiled live from the GitHub API on 2026-07-15.

## Inventory

- Repositories found: **4**
- Original repositories: 2 — `Little-rookie`, `Big-Buzzard`
- Forks: 2 — `CodingInterviewChinese2`, `awesome-chatgpt-prompts-zh`
- Repositories with a latest release: **0**
- Repositories with any git tag: **0**
- Repositories with GitHub Actions workflows: **0**

## Headline conclusions

1. **No releases anywhere.** None of the 4 repositories has a published GitHub Release, so there is no tag-and-title record to show for any project.
2. **No git tags anywhere.** All 4 repositories return an empty tag list, so there are no version markers anchoring a release.
3. **No CI at all.** None of the 4 repositories has any GitHub Actions workflow on record, so there are no Actions runs — passing or failing — to report. There are no CI runs to gate a release on.

---

## Little-rookie

https://github.com/HeziLiu/Little-rookie

- **Type:** original repository
- **Description:** Undergraduate coursework
- **Primary language:** Java
- **Default branch:** `master`
- **Latest release:** none (no published releases)
- **Git tags:** none (empty tag list)
- **GitHub Actions:** no workflows — this repository has no workflows at all

## CodingInterviewChinese2

https://github.com/HeziLiu/CodingInterviewChinese2

- **Type:** fork
- **Description:** 《剑指Offer》第二版源代码
- **Primary language:** C++
- **Default branch:** `master`
- **Latest release:** none (no published releases)
- **Git tags:** none (empty tag list)
- **GitHub Actions:** no workflows — this repository has no workflows at all

## awesome-chatgpt-prompts-zh

https://github.com/HeziLiu/awesome-chatgpt-prompts-zh

- **Type:** fork
- **Description:** ChatGPT 中文调教指南。各种场景使用指南。学习怎么让它听你的话。
- **Primary language:** not reported
- **Default branch:** `main`
- **Latest release:** none (no published releases)
- **Git tags:** none (empty tag list)
- **GitHub Actions:** no workflows — this repository has no workflows at all

## Big-Buzzard

https://github.com/HeziLiu/Big-Buzzard

- **Type:** original repository
- **Description:** For future....
- **Default branch:** `master`
- **Latest release:** none (no published releases)
- **Git tags:** none (empty tag list)
- **GitHub Actions:** no workflows — this repository has no workflows at all

---

## Recommendations

1. **Cut initial semver tags** on the original repositories (`Little-rookie`, `Big-Buzzard`) to create version anchors.
2. **Add a basic CI workflow** (e.g., a build/lint Action) so future releases have a passing run to point at.
3. **Keep forks out of release scope** — `CodingInterviewChinese2` and `awesome-chatgpt-prompts-zh` are upstream mirrors and should not be release targets.
