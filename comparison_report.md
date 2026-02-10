# Academic Website Template Comparison: AcademicPages (Jekyll) vs Wowchemy Starter (Hugo)

## Executive summary

Recommendation: Wowchemy (Hugo starter).

Short summary: Based on the repositories' metadata and the user's profile from memory, I recommend using the Wowchemy (Hugo-based) starter if you want a modern, feature-rich academic site with built-in academic layouts and better performance out of the box. AcademicPages (Jekyll) is an excellent lightweight alternative that integrates seamlessly with GitHub Pages and is simpler to maintain; choose it instead if you prefer a minimal Jekyll/GitHub Pages-first workflow.

---

## What I fetched from GitHub and memory

- User profile (from memory server): Junteng Liu. Key fields used below are listed in the Compatibility Analysis section. I used only the memory contents and did not add or invent personal details beyond that dataset. If a field required by the analysis was absent in memory I noted it explicitly.

- Repository metadata fetched (via GitHub API calls):
  - academicpages/academicpages.github.io
    - README.md blob sha: 8b8e0f182a2266684ead4c7fb43a35c69fe0ffde (file present in repo)
    - Latest commit listed by the API (most recent commit returned): 131f92f42395beb045a5afdde8124ec34e6ad8bf (author date: 2026-02-05T03:13:14Z)
    - Repo metadata: MIT license, 16,425 stars (stargazers_count), last pushed_at: 2026-02-05T03:13:14Z, topics include: jekyll, github-pages, academic-website
    - Noted repository files/folders observed: _config.yml, Gemfile, _publications, _posts, _talks, _teaching, _portfolio
  - wowchemy/starter-academic
    - README.md blob sha seen in the API listing: 61309231e15e8c98d2201e84229c1fb0ac7a98e8
    - Latest commit listed (as returned by the API): 7d5d875aa1dde734a2cdcc17418ac9974eddc83d (author date: 2026-02-08T01:28:59Z)
    - Repo metadata (from multiple starter forks and listings): many Hugo-based starter forks exist with MIT license and descriptions indicating "Wowchemy" or "Wowchemy starter Hugo academic"; the repository contents returned by the API include go.mod, hugoblox.yaml, netlify.toml, config/, content/, data/, static/, and package.json. These indicate a Hugo site scaffold with Netlify hosting config.

Note on README content fetch: while the GitHub API metadata and file listings were successfully read (file names, shas, folder structure, commit shas and timestamps, license and star counts), calls to retrieve README raw text content using the file-content endpoint encountered serialization errors in this environment. Therefore the report is based on observed repository metadata (file/folder presence, commit timestamps, topics, and license) returned by the GitHub API and on memory for the user profile. Where README-specific text would change a capability claim, I explicitly note uncertainty.

---

## Feature summary (concise bullets derived from repo contents/metadata)

- AcademicPages (academicpages/academicpages.github.io)
  - Generator: Jekyll (presence of _config.yml, Gemfile).
  - Default content types supported (observed in repo): posts (_posts), publications (_publications), talks (_talks), teaching (_teaching), portfolio (_portfolio), pages, assets.
  - Theming/customization approach: Jekyll templates + Sass (presence of _sass), layout files in _layouts; customization via _config.yml and Liquid templates.
  - Plugin/extension ecosystem: standard Jekyll ecosystem; designed to be GitHub Pages-friendly (topics include github-pages). Specific plugins are not listed in the API metadata; check README for recommended plugins (could not fetch README text reliably here).
  - License: MIT (repo license metadata).
  - Last upstream update (from commit metadata): latest commit shown 2026-02-05T03:13:14Z; repo updated_at 2026-02-10T08:51:28Z (API metadata).

- Wowchemy starter (wowchemy/starter-academic)
  - Generator: Hugo (presence of go.mod, hugoblox.yaml, config/, content/, data/ — typical of Hugo starters).
  - Default content types supported (observed in repo): content/ and data/ suggest support for pages, publications, projects, talks; many Hugo Wowchemy starters include rich academic sections (publications, courses, talks) — presence of structured content/data directories supports this.
  - Theming/customization approach: Hugo themes and configuration (hugoblox/hugoblox-like YAML/TOML params), templating with Go templates; clearly prepared for modular site blocks.
  - Plugin/extension ecosystem: Hugo shortcodes, Wowchemy modules/blocks; netlify.toml present for Netlify deployment. Specific plugin lists are in README (could not fetch raw text reliably here).
  - License: MIT (many starter forks and metadata show MIT license in listing).
  - Last upstream update (commit metadata observed): commit shown 2026-02-08T01:28:59Z in API results (note: some forks and mirrors exist; this timestamp reflects the API listing returned here and may correspond to a particular maintained fork or the starter repository's HEAD).

---

## Side-by-side feature matrix

Note: entries are derived from repo metadata (file/folder presence, topics, license, and commit dates). If a capability usually advertised in the README could not be confirmed from metadata alone it is marked "Likely / See README" and I document that raw README text was not retrievable in this environment.

| Dimension | AcademicPages (Jekyll) | Wowchemy starter (Hugo) |
|---|---:|---|
| Generator | Jekyll (Liquid, Ruby) | Hugo (Go templates) |
| Ease of installation (local) | Low–Medium — install Ruby + Bundler; run jekyll serve. Familiar for GitHub Pages users. | Medium — install Hugo (extended sometimes), node/pnpm for asset toolchain may be needed; run hugo server. |
| Built-in support for publications/bibliography | Explicit folder _publications present — strong out-of-the-box support for listing publications. | Content/data structure present; Wowchemy starters are built for publications (observed content/data directories) — strong out-of-the-box support in Wowchemy variants. |
| Support for math and code highlighting | Jekyll supports code highlighting (Rouge) and math via MathJax or plugins (depends on config). | Hugo supports code highlighting (Chroma) and math via MathJax/KaTeX shortcodes or configuration; Wowchemy commonly includes math support in theme. |
| Multilingual support | Possible via Jekyll multilingual plugins but less common by default (not obvious from metadata). | Hugo has built-in multilingual support; Wowchemy starters typically support multilingual setups (likely). |
| Performance (build speed) | Slower for large sites (Ruby/Jekyll) — fine for small sites. | Faster builds (Hugo is known for very fast builds). |
| Hosting compatibility | Works directly with GitHub Pages (Jekyll is native to GitHub Pages). | Works well with Netlify, GitHub Pages (with extra build step), GitLab Pages; netlify.toml present suggests Netlify. |
| Availability of ready academic layouts | Yes — templates and directories for publications, talks, teaching are present. | Yes — Wowchemy is explicitly designed as an academic site framework with many ready layouts and modular sections. |
| Community / maintenance activity | High popularity (16k+ stars). Repo active (recent commits 2026-02). | Wowchemy ecosystem widely used; multiple forks and starter repos observed. Latest commit timestamps in API results indicate recent activity (2026-02 in the listing used). |

---

## Compatibility analysis with your profile (memory-driven)

I used only the user profile stored in the memory server. Key data points for Junteng Liu (from memory):

- Name / role: Junteng Liu — First-year PhD candidate at HKUST NLP Group (PhD in Computer Science, 2024–Present).
- Education: B.Eng. (SJTU, graduated June 2024).
- Research areas / interests: Natural Language Processing, Machine Learning, LLM reasoning and RL, hallucination in VLMs, truthfulness and interpretability of LLMs.
- Internships and positions: Research Intern at MINIMAX (Feb 2025–Present), Research Intern at Tencent WXG (Jun–Sep 2024), Research Intern at Shanghai AI Lab (Jun–Dec 2023).
- Publications (explicitly listed in memory):
  1. "SynLogic: Synthesizing Verifiable Reasoning Data at Scale for Learning Logical Reasoning and Beyond" (2025) — First author; ArXiv; has GitHub code repo.
  2. "On the Perception Bottleneck of VLMs for Chart Understanding" (2025) — First author; ArXiv; has GitHub code repo (Vision4Chart).
  3. "On the Universal Truthfulness Hyperplane Inside LLMs" (EMNLP 2024) — First author; has GitHub code repo (Universal_Truthfulness_Hyperplane).
  4. "In-Context Sharpness as Alerts: An Inner Representation Perspective for Hallucination Mitigation" (ICML 2024) — Co-author.
  5. "C-Eval: A Multi-Level Multi-Discipline Chinese Evaluation Suite for Foundation Models" (NeurIPS 2023) — Co-author.
  6. "Composing Parameter-Efficient Modules with Arithmetic Operations" (NeurIPS 2023) — Co-author.
- Contact links in memory: email jliugi@connect.ust.hk; GitHub username Vicent0205; Google Scholar and X handle also present in memory.
- Hosting preferences: None explicitly stored in memory.

Compatibility mapping:

- Publications: AcademicPages has an explicit _publications folder (observed) which makes it straightforward to add the publications listed in memory as individual markdown entries (one file per publication). Wowchemy/Hugo starters commonly use a structured data file (YAML/JSON/TOML under data/ or content/publication/) and provide listing templates. From the observed repo contents:
  - AcademicPages: _publications directory present — each publication can be a markdown file with metadata (date, title, authors, venue, links to PDF/code). So all six publications listed in memory can be supported out-of-the-box with little manual work.
  - Wowchemy (Hugo): content/ and data/ folders present; Wowchemy starters usually provide built-in publication blocks and citation handling; the publications in memory can be added via the starter's publications/data format or via BibTeX import depending on the specific starter. Likely out-of-the-box support but you will need to place the entries in the correct data format (slightly more structured than AcademicPages' simple markdown files, depending on the starter variant).

- Code repositories / links: Both templates let you link to code repos and add project/case-study pages. Memory indicates the user has GitHub repos per publications; both templates will support linking to these. Wowchemy often has a "projects" or "portfolio" section and card layouts that look polished by default; AcademicPages also includes _portfolio.

- Math, equations, and code snippets: As an NLP/ML researcher you probably need math and code highlighting. Both templates (from observed files and typical capabilities) support code highlighting and math (AcademicPages via Jekyll configuration for Rouge/MathJax; Wowchemy via Hugo Chroma + MathJax or KaTeX support). If you frequently show math, Wowchemy tends to make it straightforward; AcademicPages requires adding MathJax configuration (still straightforward).

- Hosting and workflow preference: Memory does not specify hosting preference. If you want to host directly via GitHub Pages without a CI build step, AcademicPages (Jekyll) is the simplest. If you're comfortable with a build step (Hugo build on Netlify or GitHub Actions) and want faster build times and more modern features, Wowchemy is better.

- Internationalization / multilingual: Memory does not list a need for multiple languages. If you later need it, Hugo (Wowchemy) has built-in multilingual features, while Jekyll requires plugins and more manual setup.

Summary of mapping: both templates cover the user's needs (publication lists, code links, talk/teaching pages). AcademicPages is slightly simpler for direct GitHub Pages hosting and simple markdown-based publication entries; Wowchemy offers richer polished layouts and faster builds and is the better long-term choice if you prefer a modern look and modular academic blocks.

---

## Migration effort estimate (realistic, based on observed repo structure and typical setup steps)

Estimates assume a technically competent user comfortable with command line, Git, and basic config edits.

- AcademicPages (Jekyll)
  - Effort: Low–Medium
  - Time estimate: ~4–12 hours
  - Main steps:
    1. Clone the template repo or use it as a GitHub Pages template.
    2. Install Ruby, Bundler, and required gems (from Gemfile); run bundle install.
    3. Edit _config.yml (site title, description, author, contact email), and _pages for About/CV.
    4. Add publications as files under _publications/ (one markdown file per publication) using the repo's example format.
    5. Add projects (portfolio) and talk entries to _portfolio and _talks if needed.
    6. Test locally with bundle exec jekyll serve and iterate on layout tweaks.
    7. Push to GitHub (enable Pages if not already) and confirm site builds.
  - Notes: Straightforward if you prefer GitHub Pages and markdown-focused workflow. Math requires adding MathJax config; bibliography styles may need manual templating if you want advanced citation formatting.

- Wowchemy starter (Hugo)
  - Effort: Medium
  - Time estimate: ~8–20 hours (shorter if already familiar with Hugo/Wowchemy; longer if customizing heavily)
  - Main steps:
    1. Install Hugo (recommended: latest extended version) and any node/pnpm tooling if the starter includes JS assets.
    2. Clone the starter repo or generate a site from Wowchemy starter template.
    3. Review config files (config/_default or config.toml / hugoblox.yaml) and set site params (title, author, email, social links).
    4. Add publications in the expected data/content format (data/publications.yml or content/publication/ depending on the starter). Convert your six publications into that format (or import BibTeX if supported).
    5. Populate projects, talks, teaching pages in content/ using the starter's example content.
    6. Test locally with hugo server -D and tweak theme params and shortcodes for math/code rendering.
    7. Choose hosting: Netlify (recommended flow with netlify.toml present) or GitHub Pages via CI (GitHub Actions) to build the site and publish the public/ folder.
  - Notes: Wowchemy provides polished UI blocks and more built-in academic features; learning Hugo's front matter and content structure is the main initial overhead.

---

## Recommendation and justification

Recommendation: Use the Wowchemy (Hugo) starter.

Why: For a research-active PhD candidate with multiple conference/journal publications, code repositories, and a need for polished project and publications pages, Wowchemy offers the most feature-rich, modular, and visually polished starting point. The repository listings I inspected show the typical Hugo starter structure (go.mod, config directories, content and data directories, and netlify.toml) that indicate a modern static-site generator workflow with built-in academic sections and Netlify-friendly deployment. Hugo's performance and built-in multilingual support are useful if the site grows (many publications, projects, posts). While AcademicPages is excellent for a minimal, GitHub Pages-first workflow and explicitly contains a _publications folder (making publication entry trivial), Wowchemy's layouts and modular blocks will make your publications, projects, and code links look more polished with less custom CSS work.

If your absolute priority is zero-configuration GitHub Pages hosting and you prefer to avoid Hugo and a build pipeline, pick AcademicPages. If you prefer a modern site, better performance, and nicer out-of-the-box academic layouts, pick Wowchemy (my recommended choice).

---

## Implementation checklist for the recommended template (Wowchemy / Hugo starter)

Follow these steps (ordered). Example commands assume a Unix-like shell and that you will host from a GitHub repo and deploy via Netlify or GitHub Actions.

1. Install Hugo (extended if needed):
   - macOS (Homebrew): brew install hugo
   - Linux: follow Hugo install instructions from https://gohugo.io/getting-started/installation/
2. Clone the starter repo into a new local directory:
   - git clone https://github.com/wowchemy/starter-academic.git my-site
   - cd my-site
3. Start the local server to inspect the starter (may require installing node/pnpm if the starter uses asset pipelines):
   - hugo server -D
   - Visit http://localhost:1313 to preview.
4. Edit site config (config/_default or config.toml / hugoblox.yaml): set site title, author name, email, GitHub handle (Vicent0205), Google Scholar link, and other social links.
   - Example: set author email to jliugi@connect.ust.hk and github = "Vicent0205" in params file.
5. Add publications (convert the six publications from memory): place them where the starter expects (either data/publications.yml or content/publication/). Use the starter's example entries as templates. Include fields: title, year/date, authors, venue, links (PDF, code repo), and DOI/arXiv link if available.
6. Add a Projects / Code section linking to your repositories (and add project pages where you want to explain SynLogic, Vision4Chart, Universal_Truthfulness_Hyperplane). Use the starter's portfolio/project example markdown files.
7. Add About / CV pages: fill in an About page and a downloadable CV PDF (add to static/ and link from site navigation).
8. Check math and code rendering: if you use math, enable MathJax/KaTeX per the starter's params; ensure code highlighting (Chroma) is enabled in config.
9. Test the site locally, iterate on layout/theme params to achieve desired look.
10. Push to a new GitHub repository (create one under your account), and connect to Netlify or add GitHub Actions to run hugo build and publish to GitHub Pages or your preferred host.
    - Netlify: connect the Git repo in Netlify dashboard; the included netlify.toml should help.
    - GitHub Actions (if using GitHub Pages): create a workflow building Hugo and pushing public/ to gh-pages branch (or use actions that deploy Hugo sites).
11. Verify production site and add analytics or other widgets as desired.

Estimated total hands-on time: 8–20 hours depending on familiarity with Hugo and the level of design customization.

---

## References (links + metadata)

- AcademicPages (Jekyll template): https://github.com/academicpages/academicpages.github.io
  - README.md blob sha (as returned by API listing): 8b8e0f182a2266684ead4c7fb43a35c69fe0ffde
  - Latest commit (from API listing): 131f92f42395beb045a5afdde8124ec34e6ad8bf (author date: 2026-02-05T03:13:14Z)
  - License: MIT (from repo metadata)
  - Observed files/folders used for analysis: _config.yml, Gemfile, _publications, _posts, _talks, _teaching, _portfolio

- Wowchemy starter: https://github.com/wowchemy/starter-academic
  - README.md blob sha (from API listing): 61309231e15e8c98d2201e84229c1fb0ac7a98e8
  - Latest commit (from API listing): 7d5d875aa1dde734a2cdcc17418ac9974eddc83d (author date: 2026-02-08T01:28:59Z)
  - License: MIT (observed in multiple starter forks and listing)
  - Observed files/folders used for analysis: go.mod, hugoblox.yaml, config/, content/, data/, netlify.toml, static/

Note on data provenance and limitations: I was able to retrieve repository listings, file names and shas, commit SHAs and timestamps, license, stars and topics via the GitHub API. Attempts to fetch README raw text via the file-content endpoint encountered serialization errors in this environment; because of that I relied on file/folder presence and repo metadata for capabilities. Where README text would add critical detail, I marked uncertainty. If you want the exact README body text inserted into the report, I can re-attempt retrieval (or you can grant/confirm access) and I will update the report.

---

## If any step failed during this task

- I encountered serialization errors when calling the GitHub file-content endpoint for retrieving raw README.md text (calls to fetch README content reported an internal "Object of type AnyUrl is not JSON serializable" error). Despite that, the API returned repository listings, file names and blob SHAs, commit SHAs/timestamps, license and stars. I documented the missing README raw text retrieval above and built the feature analysis from the available metadata and file/folder structure.

---

If you want, I can now:
- Add example publication files converted from the memory entries (I can create sample markdown entries for the six publications and place them in a template repo you control), or
- Re-run README raw fetch attempts (to include exact README excerpts) and update the report.

