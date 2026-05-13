# Thesis project guide

## What this project is

PhD thesis by Wannan ("Winnie") Yang, NYU Neuroscience, advised by György Buzsáki.

 Stapled format — each substantive chapter is an adapted previously-published paper.
 
  Working title TBD. 
  
  Introduction modeled structurally on Sam Zheng's 2025 Buzsáki-lab thesis (located in `Others/thesis_samzheng.pdf`). NOT modeled on Ji-An Li's 2025 UCSD thesis (also in `Others/`); Ji-An's intro takes a listing-with-framing approach Winnie explicitly does not want.

## The argument

The dissertation makes a single load-bearing claim:

> *Memory in both biological and artificial systems is best understood and shaped through inside-out methods — where the system's own internal dynamics, rather than external labels or supervision, generate the discovery and the learning signal. I demonstrate this principle in two substrates: episodic memory in the biological brain, and self-knowledge in large language models.*

(Note: the working thesis statement above currently names only two substrates. With HyperAgents now confirmed for Part III, the statement needs revision to incorporate emergent memory in LLM agents as a third substrate. The three-substrate framing maps onto inside-out at three levels of abstraction: circuit-level in the brain, model-level in single LLMs, and system-level in LLM agents.)

The unifying lens is **inside-out**, drawn from Buzsáki's *The Brain from Inside Out* (2019, in `Others/inside_out.pdf`) and from Sam Zheng's methodological reformulation in his 2025 thesis. Inside-out has two operational modes that this dissertation extends:

- **Inside-out analysis** — latent-first instead of label-first. Extract latent structure from the system's activity rather than relying on  pre-defined, experimenter-chosen labels.

- **Inside-out training** — internal signal instead of external supervision. Construct the learning signal from the system's own internal representations rather than from external corpora, benchmarks, human preferences, or rewards. 

The dissertation's intellectual move beyond Sam and beyond the Buzsáki book is the second mode — applying inside-out to *training*, not just analysis. This shows up most clearly in CASAL.

## Structure

Front matter follows convention: title, approval, dedication, epigraph, TOC, list of figures, list of tables, acknowledgements, vita (with publications), abstract.

Three planned parts:

**Part I — Episodic memory in the biological brain.** Four papers:
- Sun, Yang, Martin, Tonegawa. *Nat Neurosci* (2020). Event-specific rate remapping cells — events as transferable units. Co-author #2. — `Papers/sun_2020.pdf`
- Yang, Sun, Buzsáki. *NeurReps / NeurIPS workshop* (2023). "Changes in the geometry of hippocampal representations across brain states." UMAP analysis of awake / NREM / REM hippocampal geometry. Awake supports both pattern separation and analogy-like generalization; NREM recapitulates awake manifold without template-matching; REM does NOT (first reported UMAP analysis of hippocampal REM). **First author.** Methodologically explicit inside-out paper — the Methods section makes the label-first vs latent-first critique in its own voice. — `Papers/73_Changes_in_the_geometry_of_.pdf`
- Yang, Sun, Huszár, Hainmueller, Kiselev, Buzsáki. *Science* (2024). SPW-R-driven memory selection. **First author flagship.** — `Papers/selection.pdf`
- Zutshi, Apostolelli, Yang, Zheng, Dohi, Balzani, Williams, Savin, Buzsáki. *Nature* (2025). Hippocampal activity aligned with action plans. Co-author #3. — `Papers/Zutshi_2025.pdf`

**Part II — Self-knowledge in large language models.** Two papers:
- Yang, Yang, Garcia-Olano, Sun, Buzsaki. "How LLMs Lie: Rotation of Truth Direction as a Universal Motif." Co-first author. Inside-out *analysis*. — `Papers/deception.pdf`
- Yang, Qiu, Yu, Zhang, Yang, Kokhlikyan, Cancedda, Garcia-Olano. "Hallucination Reduction with CASAL." ICLR 2026. First author. Inside-out *training*. — `Papers/Hallucination_Reduction.pdf`

**Part III — Emergent memory in LLM agents.** One paper confirmed:
- Zhang, Zhao, Yang, Foerster, Clune, Jiang, Devlin, Shavrina. "HyperAgents." arXiv, March 2026. **Co-first author** (one of three). Internship work at Meta (FAIR / Meta Superintelligence Labs). Introduces self-referential agents that combine task agent and meta agent into a single editable program ("metacognitive self-modification"); extends the Darwin Gödel Machine into DGM-Hyperagents. **Memory connection:** persistent memory *emerges* as one of the agent's self-discovered improvements — not designed in, but learned by the system as a useful self-modification that accumulates across runs and transfers across domains. The agent's own memory of prior reasoning and self-modifications becomes the supervision signal for further improvement (system-level inside-out — the agent's internal record drives its own learning, with no external curator). — `Papers/hyperagents.pdf`

Note: `73_Changes_in_the_geometry_of_.pdf` is NOT a Part III candidate — it is the 2023 NeurReps brain paper now slotted into Part I.

**Final chapter — Discussion / Future Directions.** Planned. Ji-An's thesis lacks one and Winnie wants this addition. Should compare across chapters, surface tensions, and sketch what comes next.

## Committee

Thesis committee:
- **Dmitry Rinberg** (NYU CNS) — systems neuroscience, olfaction.
- **Zhe Chen** (NYU Langone) — computational neuroscience, Bayesian methods, neural data analysis.
- **Dayu Lin** (NYU Langone) — social/emotional behavior neuroscience.
- **Christine Constantinople** (NYU CNS) — decision-making, value-based behavior, prefrontal cortex.
- **Eric Oermann** (NYU Langone) — neurosurgeon-scientist, AI/ML in clinical neuroscience.

External examiner:
- **Ellie Pavlick** (Brown / Google) — NLP, LLM interpretability.

Implications for framing:
- The committee spans systems neuroscience, computational/methodological neuroscience, behavior, clinical AI, and LLM interpretability — a deliberate neuroscience-to-AI bridge that mirrors the thesis's own structure.
- Pavlick as external is well-matched for Part II (self-knowledge in LLMs); the deception and CASAL chapters should be defensible at her level of technical depth.
- Oermann adds a clinical/AI-safety lens that may matter for how the LLM and agent chapters frame deployment and risk.
- Constantinople and Rinberg ground Part I in mainstream systems neuroscience; the inside-out / latent-first methodology should be presented in a way that's defensible without assuming the committee shares Buzsáki's polemic priors.

## Where files live

- `Papers/` — published papers being adapted into chapters.
- `Others/` — reference theses (Sam Zheng's, Ji-An Li's) and Buzsáki's *Brain from Inside Out*.
- `New_York_University_PhD_Dissertation_Latex/` — official NYU GSAS LaTeX template (2025 version, satisfies NYU GSAS submission requirements). Key files: `thesis.tex` (main document), `abstract.tex`, `defs.tex` (custom macros), `thesis.bib` (BibTeX bibliography), `chapters/` (one `.tex` file per chapter, included via `\input`), `figures/`. Per the template's README, the convention is one chapter per `.tex` file.
- `guidance/` — official NYU GSAS dissertation formatting documents (Formatting Guide, 2025 Formatting Guidelines, Submission Checklist, Submitting Your Dissertation, oral defense form). Authoritative for any submission-format question.
- `intro/` — Markdown drafts for Chapter 1 (introduction), one `.md` file per section (e.g., `1_1.md`, `1_2.md`). This is the canonical location for intro drafts; do NOT save them to `drafts/` or any other folder.

## Format

**Workflow: Markdown for drafting, LaTeX for the canonical thesis. No Overleaf, no Pandoc.**

Winnie drafts in Markdown (`.md`) for fast, distraction-free idea formulation with AI assistance. When a draft is ready to land, Claude reads the Markdown content and edits the corresponding LaTeX file in `New_York_University_PhD_Dissertation_Latex/` directly, following the template's existing conventions and macros. There is no separate conversion tool in the loop.

This means:
- *Don't* suggest Overleaf as a primary workflow. It's not part of this project.
- *Don't* run Pandoc as a conversion step. Claude reads Markdown and writes matching LaTeX in place.
- *Don't* impose generic conversion rules on the LaTeX. Match the template's existing patterns — chapter heading style, section structure, macros from `defs.tex`, citation conventions from `thesis.bib`.

**Workflow when landing a draft:**
- Draft and refine the chapter/section together in Markdown.
- When ready, Claude edits the corresponding `.tex` file in `New_York_University_PhD_Dissertation_Latex/chapters/` in place.
- If it's a new chapter, also update `thesis.tex` to add the `\input{chapters/ch_*.tex}` line.
- Citations use BibTeX keys from `New_York_University_PhD_Dissertation_Latex/thesis.bib`.
- The NYU template handles all front matter, page numbering, and submission-format requirements.

**LaTeX file editing rule:**
- When editing files inside `New_York_University_PhD_Dissertation_Latex/` (`thesis.tex`, `defs.tex`, `abstract.tex`, `chapters/*.tex`, `thesis.bib`), always edit the existing files in place. Do **not** create parallel versions, copies, or "edited" variants outside the template directory. The canonical state of the thesis must always live where it can be compiled — duplicating files leads to drift and broken cross-references. If a major rewrite is in progress, branch the work in Markdown drafts (`.md`) instead, then update the LaTeX file in place when ready.

**Setup tasks deferred until needed (not blocking drafting):**
- Install a LaTeX distribution (MacTeX or BasicTeX on macOS) for the final PDF compile (one-time).
- Set up a reference manager that exports to BibTeX (Zotero with Better BibTeX is a common choice). Output `.bib` should target `New_York_University_PhD_Dissertation_Latex/thesis.bib` or be merged into it.
- Customize `defs.tex` with any project-specific macros (acronyms, term shortcuts) when they accumulate.

## LaTeX figure caption rule

Always use the two-argument caption form so the List of Figures shows only the figure title, not the full legend:

```latex
\caption[Short title only]{Full legend text with all panel descriptions.}
```

The short title (optional argument) is what appears in the List of Figures. It should be the bold title of the figure stripped of any trailing period. The full legend goes in the mandatory argument as usual.

## Style and voice — the rules

See `docs/sam_style_prompt.md` for the full style reference.

**Structure: interleaved argument, not chapter listing.**
- For Chapter 1 specifically: alternate between conceptual sections and chapter previews. Each chapter preview is an *instance* of the conceptual point that immediately preceded it.
- The conceptual line builds across the intro — each section deepens the previous.
- Avoid the stapled-thesis pattern of "Chapter 2 demonstrates X. Chapter 3 demonstrates Y." Each chapter should arrive under a conceptual umbrella that has already been opened.

**Voice: first person, discovery-process narrative.**
- Use "I" (and "we" where collaborative) throughout the intro and discussion.
- Frame chapter previews as discoveries, not deliverables: "I found Y, which surprised me because Z" — not "Chapter X demonstrates Y."
- Show the *process* — what was puzzling, what blocked you, what cleared it. Don't sanitize the path; methodological detours and surprises are features.
- Tone: warmly curious. Not modest to the point of hedging, not confident to the point of coldness.

**Opening and closing.**
- Open with a concrete scene or moment — a historical discovery, a puzzle, an image — before stating the argument. Let the scene earn the claim.
- End open, not closed. Gesture toward what remains mysterious or unresolved. Avoid "In conclusion, this chapter demonstrated X, Y, Z."

**Sentences and rhythm.**
- Mix sentence lengths deliberately. Short punchy sentences land hardest after a longer buildup: *"This identity is simple but deep."*
- Name surprises as surprises. Say "strikingly," "the big reveal is," "interestingly" when something is genuinely unexpected — don't bury it in technical prose.
- Ask the question the reader is silently asking, then answer it. Rhetorical questions work when they're honest.

**Concrete anchors.**
- Every abstract claim gets a concrete example that carries real weight — not a decorative illustration, but the argument made tangible.
- Quotes and outside references should feel lived-with, not looked up. If you bring in a philosopher or a parable, show how you've digested it.

**Terminology.**
- "inside-out" (hyphenated, lowercase except sentence-initial). NOT "inside out" or "Inside-Out."
- "outside-in" likewise.
- "self-knowledge" is the framing for Part II — NOT "deception," "lying," or "parametric memory" alone.
- "episodic memory" for Part I — more specific and defensible than "memory in brains."
- "SPW-R" or "sharp wave ripple" — match the usage in `Papers/selection.pdf`.

## Things to avoid

- Don't write Ji-An-style chapter listings. The intro is an argument, not a table of contents.
- Don't pitch the dissertation as "three projects I worked on." Pitch it as one argument demonstrated in three substrates.
- Don't reduce the deception paper to "lying." Frame it as discovering internal self-knowledge representation.
- Don't conflate "memory in LLMs" with parametric memory only. The Part II framing is *self-knowledge*.
- Don't oversimplify the brain–LLM bridge. The bridge is methodological (inside-out applies to both); it is not a claim that LLMs are like brains. Be precise about what is and isn't being claimed.
- Don't use emojis or marketing-style formatting in the thesis.
- Don't use `---` horizontal rule dividers in Markdown drafts. They make the writing feel AI-generated. Section headings (`###`) and prose transitions carry the structure; dividers are redundant and should be omitted entirely.
- Avoid em dashes (`—`) in prose. Heavy em dash use is an AI writing tell. Restructure the sentence instead: use a comma, a colon, a new sentence, or tighter phrasing.

## Active context (as of 2026-05-04)

- §1.1 ("The thread") drafted in `intro/1_1.md` and landed in `ch_introductory.tex`. Covers the four Part I brain papers.
- §1.2 ("The hidden thread") drafted in `intro/1_2.md`. Covers the inside-out vs. outside-in framework (Buzsáki), with subsections: "You get what you measure" (Shannon / epistemological argument), "When the label fails" (yang2024selection / UMAP on awake data), "When the template fails" (yang2023nreps / UMAP on sleep data). Additional subsections in progress.
- §1.3 and beyond still to be drafted.
- The order within Part II is provisionally **deception → CASAL** (discovery → application).
- Part III now has HyperAgents confirmed (co-first author, March 2026 arXiv, Meta internship). The working thesis statement still names only two substrates and needs revision to include emergent memory in LLM agents.
- Part III may stay as a single-paper part, or expand if Winnie has additional agent work she wants to include — open question.
- Decisions still open: discussion-chapter length and content; whether Sun 2020 qualifies as a thesis chapter under NYU's authorship rules (or whether it becomes extended background in Chapter 1); ordering within Part I now that there are four papers — chronological order (Sun 2020 → NeurReps 2023 → Yang 2024 → Zutshi 2025) is one option; an inside-out depth ordering that puts Yang 2024 last as the flagship is another.
- Reference manager not yet documented here.

## Chapter LaTeX filenames

Each paper chapter maps to a `.tex` file in `New_York_University_PhD_Dissertation_Latex/chapters/` and a figures folder in `New_York_University_PhD_Dissertation_Latex/figures/`. The supplementary/extended data appendix for each chapter goes in a matching `_si.tex` file.

| Paper (full title) | Chapter file | SI file | Figures folder |
|---|---|---|---|
| "Hippocampal neurons represent events as transferable units of experience" — Sun, Yang, Martin, Tonegawa. *Nat Neurosci* (2020) | `ch_sun2020.tex` | `ch_sun2020_si.tex` | `figures/ch_sun2020/` |
| "Changes in the geometry of hippocampal representations across brain states" — Yang, Sun, Buzsáki. *NeurReps / NeurIPS workshop* (2023) | `ch_nreps2023.tex` *(not yet created)* | `ch_nreps2023_si.tex` | `figures/ch_nreps2023/` |
| SPW-R-driven memory selection — Yang, Sun, Huszár et al. *Science* (2024) | `ch_selection2024.tex` *(not yet created)* | `ch_selection2024_si.tex` | `figures/ch_selection2024/` |
| Hippocampal activity aligned with action plans — Zutshi, Apostolelli, Yang et al. *Nature* (2025) | `ch_zutshi2025.tex` *(not yet created)* | `ch_zutshi2025_si.tex` | `figures/ch_zutshi2025/` |
| "How LLMs Lie: Rotation of Truth Direction as a Universal Motif" — Yang et al. | `ch_deception.tex` *(not yet created)* | `ch_deception_si.tex` | `figures/ch_deception/` |
| "Hallucination Reduction with CASAL" — Yang et al. *ICLR 2026* | `ch_casal.tex` *(not yet created)* | `ch_casal_si.tex` | `figures/ch_casal/` |
| "HyperAgents" — Zhang, Zhao, Yang et al. *arXiv* (2026) | `ch_hyperagents.tex` *(not yet created)* | `ch_hyperagents_si.tex` | `figures/ch_hyperagents/` |

The Introduction is `ch_introductory.tex` and the final chapter is `ch_conclusion.tex` (titled "Concluding Discussion" in `thesis.tex`).

Figure image files for `ch_sun2020` are already copied to `figures/ch_sun2020/` (fig1.jpg–fig7.jpg for main figures; extended_fig1.jpg–extended_fig10.jpg for supplementary).

## Useful references

- Buzsáki, *The Brain from Inside Out* (Oxford UP, 2019). Especially Chapter 1, "The Problem." → `Others/inside_out.pdf`
- Sam Zheng, 2025 NYU Buzsáki-lab thesis. The structural model for Chapter 1. Especially §§1.1–1.9. → `Others/thesis_samzheng.pdf`
- Ji-An Li, 2025 UCSD thesis, "Bridging Biological Learning and Deep Learning." Useful as a stapled-thesis example, but the intro style is the *anti-model* — explicitly NOT what Winnie wants. → `Others/Dissertation__Bridging_Biological_Learning_and_Deep_Learning.pdf`


## Ducomentation

- [Architecture](docs/Architecture.md) - Structure of the thesis and the purpose of each chapter.
- [Changelog](docs/changelog.md) - Version history.
- [Project status](docs/project_status.md) - Current progress.
- Update files in the docs folder after major milestones and major additions to the project.
- Use the /update-docs slash command when update the docs
