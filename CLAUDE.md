# Project context

Plain-language checklists that help child welfare, legal and clinical professionals
(CASAs, GALs, judges, magistrates, case managers, clinicians) judge whether AI-assisted
research and AI tools are ethical. Built on the ETHICS framework:

Lee, J. Y., Pace, G. T., Cha, H., Rao, S., Hahm, H. C., An, R., & Denby-Brinson, R. (2025).
ETHICS: An ethical framework for artificial intelligence (AI) use in social work research.
*Journal of the Society for Social Work and Research, 16*(4), 699-711. https://doi.org/10.1086/739116

The owner (Joyce Lee) wrote the framework. Its six principles: **Equity, Transparency,
Human-Centeredness, Integrity, Collaboration, Safety.** Every checklist must cover all six.

## Audience and style rules
- Busy non-technical professionals. Plain language, no jargon, minimal text.
- Screening aid, not a verdict or professional advice (keep the footer disclaimer).
- Answers stay in the browser only (localStorage). No data leaves the device.

## Files
- `ai-tool-checklist.html` - "AI Tool Quick Check": 18 questions (3 per principle) for assessing
  a predictive model, chatbot or other AI tool. Single self-contained file. All wording is in
  the block between `EDIT HERE` and `END OF EDIT-HERE SECTION`. **This is the public page.**
- `ai-research-checklist.html` - "Is This AI-Assisted Research Ethical?": 24 questions (4 per
  principle) for assessing AI-assisted studies. Wording lives in `var PRINCIPLES`
  (`t`=question, `h`=hint, `a`=follow-up).
- `EDITING-GUIDE.md` - how the owner edits the checklists on GitHub without help.
- `index.html`, `GITHUB_PAGES_SETUP.md` - unrelated older OSU PhD admissions FAQ page. Leave alone.

## Deployment
- `.github/workflows/deploy.yml` publishes ONLY `ai-tool-checklist.html` (copied to `_site/index.html`)
  to GitHub Pages at https://jyelee2021.github.io/Test/ on push to the two `claude/...` branches.
  Do not change it to publish the whole repo.
- The `github-pages` environment restricts deploy branches; this branch had to be allowed in
  Settings > Environments > github-pages.
- Taking it down: disable Pages in repo Settings > Pages.
- Private preview copies were published as Claude artifacts (owner-only). They only change when
  republished. After editing, re-publish the file to keep the preview in sync.

## Design decisions
- Results logic: a "No" on a `key: true` question shows a red "Stop and ask first". Otherwise
  a caution/good message depends on how many No / Not sure answers there are.
  Key questions (tool check): human final decision; checked for wrong/made-up answers;
  harms weighed in writing; sensitive data protected.
- Environmental impact (in the framework under Equity) was left out to keep the list short.
- The framework targets researchers doing the work; questions were reworded for readers
  and users of the research.

## Open items
- Owner was checking that the public link shows the tool checklist, not the old admissions FAQ
  (likely a cache issue; try a private window or `?v=2`).
- Owner will keep editing wording directly on GitHub; help with wording, adding questions, or
  a plain-language review is welcome.
