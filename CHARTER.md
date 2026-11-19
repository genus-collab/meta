# Topological String Lab: Community Charter

*Draft — prepared by Andrea Brini. Living version: https://claude.ai/artifact/M5YExuBKiRJXisd1VQvUZn*

## Mission and Scope

The **Topological String Lab** (**TS-Lab**) is an open-source public collaborative workspace for research in topological strings and enumerative geometry. The natural comparison is the Polymath model — a public workshop where research is done collectively and openly — rather than the Stacks Project, which assembles a foundation from established results.

The repository is not a preprint server. The PDFs it contains are working documents: in-progress, often AI-assisted, and not independently refereed. Curated, human-authored papers destined for arXiv emerge from a separate distillation process described below.

**Topical scope.** The collaboration's research is organised around four mutually reinforcing strands of inquiry, together aiming at a unified mathematical theory of topological strings.

- **Foundations** — mathematical formulations of topological strings. Examples include: gauged linear sigma models (GLSM) and logarithmic compactifications, GW and FJRW theories, quantum Lefschetz theorems, LG/CY correspondence, GIT wall-crossing
- **Solutions** — all-genus (perturbative) methods for Calabi-Yau threefolds. Examples include: BCOV theory, holomorphic anomaly equations, boundary data such as the conifold gap conjecture, GW/DT correspondence and MNOP-type results, DT wall-crossing and S-duality constraints on the partition function
- **Structures** — global and nonperturbative structure. Examples include: wavefunction interpretations of the topological string, BPS invariants as Stokes data for Riemann-Hilbert problems, resurgence analysis, open/closed wavefunctions and quantum mirror curves
- **Enhancements** — extensions and enrichments of curve counting theories. Examples include: refined, motivic and K-theoretic enumerative invariants, refined GW/DT/PT correspondences, 3D mirror symmetry, enumerative geometry of higher-dimensional Calabi-Yau varieties

A **Steering Committee (SC)** oversees the collaboration; terms of service are defined in § Governance. Each strand is looked after by a **Strand Moderator**, appointed by the SC. Cross-strand projects are welcome, and scope questions are resolved by the relevant Strand Moderator.

**Guiding principles.**

- The measure of the collaboration's success is growth in human understanding of its subject.
- Access to the repository will be public and open to all by default. All outputs (code; draft notes; progress reports) will be open-source as a rule. The public-domain nature removes artificial barriers to international collaboration, particularly where IP export-control restrictions apply to Maths as a STEM discipline.
- Early-career collaborators are central. A core objective of the collaboration is to give PhD students and postdocs a place to do ambitious work, with visible contribution and credit, and increased equity of access.
- AI-assisted or generated material will exclusively receive collective authorship by the collaboration. While the collaboration cannot *per se* democratise access to frontier AI tools, the shared nature of the repository allows all members to work and build upon and cross-validate the entirety of the research outputs produced by the collaboration, regardless of their origin.
- We anticipate many of the results of the TS-Lab to be AI-driven; however the human activity of the lab is not meant to reduce to a mere translation exercise of AI-generated results. Every kind of contribution that advances understanding will be recognised, with or without the use of AI. This includes joint training and dissemination activities (conferences; online seminars and working groups). Early-career researchers and PhD students will be central to this effort.
- Members of the collaboration will also coordinate, when and as appropriate, the creation of working groups to curate human-written curated surveys of topical results obtained in the TS-Lab. Unlike the rest of the content of the repository, surveys are conceived for submission to the arXiv and, potentially, to traditional peer-reviewed outlets. Authorship and credit for these surveys will be attributed to members of these working groups using the traditional rules of the mathematical community. Early-career researchers and PhD students will be central in driving this effort, and will obtain appropriate recognition through it.

## Repository Structure

The repository lives under a single GitHub organisation (**TS-Lab**). Within the organisation, content is split across thematic repos, a shared knowledge repo, and one administrative repo.

**Thematic repos** (one per research strand):

- `foundations` — log GLSM and GW/FJRW theories, quantum Lefschetz theorems, LG/CY correspondence and GIT wall-crossing
- `solutions` — BCOV theory, holomorphic anomaly equations, all-genus solutions on CY3s, conifold gap conjecture, GW/DT correspondence and DT wall-crossing
- `structures` — nonperturbative completions of topological strings, BPS invariants and Riemann-Hilbert problems, resurgence analysis, open/closed wavefunctions and quantum mirror curves
- `enhancements` — refined and K-theoretic invariants, motivic DT theory, 3D mirror symmetry, enumerative geometry of CY fourfolds

**Administrative repo**: `meta` — governance documents (this charter), LaTeX style template, project proposal issue template, CI configuration, and the master index of all projects across all thematic repos.

**Shared knowledge repo**: `atlas` — a curated, cross-strand collection of the collaboration's conjectures, open questions, examples, counterexamples and computed invariants (Gopakumar–Vafa/BPS invariants, DT and PT counts, partition functions, and the like). Each entry records its status label (see § AI Use and Methodology), its conventions and normalisations, its provenance (the project that produced it), and the code that reproduces it; the collection is searchable. Its purpose is to keep the collaboration's growing output navigable, to people and to AI systems alike, and to track which questions are open, partially resolved or settled. It is maintained by a standing infrastructure working group.

**Project directory structure.** Each project occupies a self-contained subdirectory within its thematic repo:


```

projects/

 <project-name>/

 README.md # scope, status, methodology, contributors

 main.tex # LaTeX source

 output/main.pdf # compiled output (committed)

 code/ # Mathematica notebooks, SageMath scripts, Lean files

 data/ # tables, computed invariants

 transcripts/ # archived AI transcripts and reasoning traces, where terms permit

```


Projects spanning multiple thematic areas are placed in the most relevant repo, with a cross-reference note in the other repos' `INDEX.md`.

CI runs on every push to compile LaTeX and validate that `output/main.pdf` is current. The `INDEX.md` at each thematic repo root catalogues all projects with title, status, and a one-line description.

**Licences and About page.** Every repo displays its licence in its root directory: by default CC BY 4.0 for text and PDFs, an OSI-approved licence for code, and CC0 or CC BY for data (see Open Questions). The organisation's profile carries an About page stating who maintains it, what it is for, how contributed material may be used (including whether, and on what terms, it may be used to train AI models), and how to contact the SC.

## Project Lifecycle

A project moves through three stages: **Proposed**, **Active**, and **Complete**. Status is tracked in the thematic repo's `INDEX.md` and in the project's own `README.md`.

**1. Proposed.** Any community member may propose a project by opening a GitHub Issue in the relevant thematic repo using the standard proposal template (maintained in `meta`). The template asks for: a one-paragraph description of the mathematical question, the expected outputs (PDF, code, tables), and an indication of which AI tools are anticipated. The Strand Lead acknowledges the proposal within [N] days. Proposals are not gatekept: the bar for opening a project is low. The Strand Lead may suggest a different thematic repo or flag overlap with an existing project.

**2. Active.** The proposer (or any volunteer) opens a PR creating `projects/<project-name>/` with an initial `README.md` and skeleton `main.tex`. Once merged, the project is Active. Development proceeds through collaborative commits and PRs. There is no fixed timeline for active projects.

**3. Complete.** A project is marked Complete when its authors judge that the PDF represents a coherent and self-contained body of results, all code reproduces the stated outputs, and the methodology statement in `README.md` is accurate. The Strand Lead reviews and merges a final PR updating `INDEX.md`. Completed projects are candidates for the distillation pipeline (see § From Workshop to Publication).

Projects may be archived (without being marked Complete) if they stall or are superseded. The community does not delete projects; the historical record is preserved.

## Authorship and Attribution

This repository operates on a collective authorship model, following the precedent of Polymath. The workshop is open, and the competitive norms of individual attribution are deliberately set aside within it. Individual credit comes through two channels: talks, and the distilled surveys that go to arXiv.

**Workshop PDFs (GitHub).** Project PDFs carry no individual author names. They are works of the community, credited to the TS-Lab Collective. Git history records every contributor's commits and is the durable record of individual participation.

**ArXiv surveys.** The collaboration's arXiv outputs are distilled surveys, which carry named authorship. Authors are the members of the distillation working group who did the human writing, mathematical verification and editorial work of turning workshop material into a publication-ready survey. Every author should understand the survey in detail and be able to answer technical questions about it. Each survey includes a methodology section describing how its results were obtained, including the extent of any AI involvement, cites the workshop projects it draws on, and acknowledges the broader TS-Lab community. Working groups decide their own author list; the community does not adjudicate these decisions.

**Data and code.** Code and data files in `code/` and `data/` subdirectories may carry individual attribution in their file headers, at the contributor's discretion.

**Contributions.** The collaboration values the full range of work that advances understanding, not only proving theorems: conjectures and new questions, partial progress, independent re-derivations, turning AI-generated arguments into readable mathematics, exposition, code and data, formalisation, checking others' work, mentoring and organising.

**Talks.** Within the collaboration, are recognised chiefly by presenting the work they did: in the collaboration seminar, at the annual workshop, and at external venues. The seminar archive, with named speakers, recordings and notes, is the community's public record of who has done what. Strand Leads ensure that speaking slots go to those who did the work, with priority for PhD students and early-career members; senior members writing references for junior collaborators draw on this record.

## AI Use and Methodology

AI tools are welcome in this workshop, and the collaboration helps members who want to use them to use them well. Their use is not required. Contributions made without AI are valued equally, and no stage of the project lifecycle, route to verification, or membership tier depends on using them. Whatever methods are used are reported with the same transparency.

**Methodology statement.** Every project `README.md` must include a Methodology section stating:

- Which AI tools were used (by name and approximate version where known).
- What they were used for: calculations, literature search, drafting prose, generating or checking code, suggesting proof strategies, etc.
- What human verification was performed on AI-generated content.
- Where any archived AI transcripts are kept.

This statement is updated as the project evolves. There is no stigma attached to extensive AI use, nor to none.

**AI transcripts.** Where an AI system produced a substantial calculation, argument or proof strategy, the relevant transcript or reasoning trace is committed to the project's `transcripts/` directory, where the tool's terms permit. The route a model takes sometimes contains insight that the polished argument hides; an archived trace lets others learn from it and makes the provenance of a result auditable.

**Verification and claim status.** Every claim in a project PDF carries one of five status labels: *conjectural*; *numerically supported*; *AI-proposed, unchecked*; *proved (human-checked)*; or *formally verified*. A claim may be labelled proved only once it has been checked by at least one human contributor independent of the argument's originator, by an independent calculation, a check in a computer algebra system, or a careful reading of the argument; the verifier and method are recorded in the `README.md`. A project may be marked Complete with claims still labelled conjectural or AI-proposed, provided the labels are accurate. The labels travel with any result contributed to the atlas, so that readers inside and outside the collaboration can see at a glance what is known and how.

**Scope.** This policy applies to workshop PDFs. Working groups producing arXiv papers are expected to hold those to standard publication norms, which may be stricter; this charter does not prescribe them beyond the methodology section required under Authorship and Attribution.

## Computational Standards

**Directory conventions.** Code lives in `projects/<name>/code/`, data in `projects/<name>/data/`. Each `code/` subdirectory must contain a `README.md` specifying: the language and version, any dependencies or packages, and instructions to reproduce the main outputs. Mathematica notebooks (`.nb`) should be accompanied by a plain-text export (`.m` or `.wl`) to allow diff-readable version control.

**Reproducibility.** The standard is: a competent user following the `code/README.md` should be able to reproduce all tables and computations cited in `main.pdf`. This is a goal, though not a hard gate for the Proposed or Active stages. It is required for the Complete stage.

**Lean and formalisation.** Lean 4 formalisations can be encouraged where the necessary background exists and formalisation adds value. At the time of writing, much of the collaboration's subject matter (moduli of stable maps, virtual fundamental classes, DT invariants) is not yet available in formal libraries.

**Data.** Computed tables of invariants (GW invariants, DT counts, partition functions, etc.) committed to `data/` should be in a plain-text format (CSV, JSON, or similar) with a header or companion file documenting the conventions, normalisation, and computation method. Tables of general interest are also contributed to the atlas repo, with provenance linking back to the project.

## From Workshop to Publication

The GitHub repository is the *workshop* (public, raw, iterative, collectively attributed). The arXiv is the *front store* (curated, human-authored, and carrying individual attribution). The pipeline between them is the -- for lack of a better word -- *distillation *process.

**Identifying distillation targets.** Any community member may propose a distillation by opening an issue in the `meta` repo identifying a cluster of completed (or near-complete) workshop projects that form a coherent mathematical narrative. The proposal should state: the intended scope and thesis of the arXiv paper, which projects are the primary sources, and an initial list of working group members.

**Distillation.** The working group writes the arXiv paper from scratch, in human prose, using the workshop PDFs as source material. The arXiv paper is not an assembly of workshop sections; it is a new, coherent document written to publication standards. The working group verifies all results independently before submission. The workshop projects are cited as source material in the arXiv paper.

**Forms of output.** The typical distilled output is a survey: a coherent, human-written account of a body of workshop results. A working group may also produce lecture notes, a documented data release to the atlas, or a software package. Turning a large body of AI-assisted workshop material into checked, readable mathematics that reveals its structure is central intellectual work.

**Relationship to arXiv.** Workshop PDFs are the messy creative projects, and may contain AI-generated outputs in slop-form. These will never go to the arXiv. The arXiv submission is the polished human-written output. The two channels serve different functions and audiences. The existence of a workshop project does not constitute prior publication of its results for arXiv purposes.

**Volume.** The expectation is that arXiv submissions are few relative to the number of workshop projects. The workshop may contain O(100) active or completed projects at any time; a successful year might produce O(5–10) arXiv papers from distillation. Quality and depth, not volume, govern what is distilled; members are encouraged to put the depth of a piece of work ahead of the rate at which papers are produced.

**Journal submission.** Distilled arXiv papers may be submitted to journals at the working group's discretion. This charter does not govern that process.

## Working Groups

Working groups are the mechanism for collaborative focus within the broader community. They are informal, self-organising, and not subject to approval.

**Formation.** A working group forms when at least two community members commit to working together on a defined scope — either a workshop project or a distillation. Formation is announced by opening an issue in the relevant thematic repo (for a project working group) or in `meta` (for a distillation working group), using the working group template. No approval is required.

**Scope.** A working group defines its own scope and operating norms. It may set its own communication channels (Zulip stream, email list, shared document), meeting cadence, and internal decision-making process. The community does not prescribe these.

**Responsibilities.** A working group is responsible for: keeping its project's `README.md` and status up to date; ensuring the methodology statement is accurate; and, for distillation working groups, delivering a paper that meets publication standards before arXiv submission.

**Dissolution.** A working group dissolves when its scope is complete or when its members decide to discontinue. Stalled working groups may be flagged by any community member; the Strand Lead may archive the associated project after [N] days without activity.

**Overlap and priority.** Multiple working groups may work on related topics simultaneously. The community norm is to communicate early about potential overlap. When groups discover substantial overlap, the default is to merge.

## Sketch of a programme for community activities

The below is an ambition, contingent on

**Collaboration seminar series.** The collaboration runs a regular online seminar — weekly or biweekly — as the primary mechanism for keeping the full community informed about developments across all strands. The seminar has three modes: *invited talks* by external speakers on topics relevant to the collaboration; *project status talks* by working group contacts and PhD students reporting on active projects; and *teaching talks*, in which a community member introduces a technique or result likely to be useful across strands, including hands-on sessions on computational, AI and formalisation tools for members who want them. Project status talks are the centrepiece: every active working group is expected to give a status update once per term, coordinated with the relevant Strand Lead. The structure mirrors the analysis-status talks used in large experimental physics collaborations, ensuring that no sub-area of the community drifts out of contact with the whole. PhD student talks are a central feature, not a secondary track. Questions arising from a talk are put to the speaker before anyone puts them to an AI model. Talks are recorded and archived in the meta repo, with session notes committed after each meeting.

**Seminar coordination.** The seminar is organised by a Seminar Coordinator, a rotating annual role well-suited to a postdoctoral researcher or advanced PhD student. The Coordinator maintains the schedule, issues invitations, ensures that each active working group presents at the required frequency, and maintains the archive of recordings and session notes. The role is explicitly credited in the community’s annual report and in any funding acknowledgements.

**Annual collaboration workshop.** Once per year the collaboration holds a week-long in-person workshop, rotating location across the three blocs. The programme includes: plenary strand reports (Strand Leads synthesising the year’s progress and cross-strand connections); working group sessions (shorter status talks on individual projects, typically given by PhD students and postdocs); and unstructured working time for launching new projects and cross-strand discussion. Workshop proceedings — the PDF outputs produced during and immediately after the event — are committed to the relevant thematic repos under the collective name and serve as the primary record of the community’s scientific output for that year.

**Monthly coordination meetings.** Strand Leads convene a monthly virtual meeting, open to all community members, at which each gives a brief update on activity in their strand: recently completed projects, upcoming milestones, and anything requiring community attention. The meeting is an information-sharing forum, not a decision-making body; SC decisions are posted asynchronously in the meta repo. Notes are committed to the meta repo within 48 hours of each meeting.

**PhD student programme.** PhD students are central participants in the collaboration’s scientific life, not auxiliary contributors. In practice: PhD students are expected to lead project working groups, give project status talks in the seminar series, and present at the annual workshop on individual project progress. Each PhD student contributor has a named contact among the Strand Leads or senior community members, responsible for ensuring they receive adequate support and visibility within the collaboration. The collaboration explicitly supports PhD students in presenting its work at external venues, coordinated through the meta repo’s conference-appearances issue tracker.

**Protecting early-career members.** The uncertainties of this period of change fall hardest on PhD students and postdocs, and senior members are expected to carry them rather than pass them down. Concretely: early-career members are first in line for seminar and external speaking slots, funded travel and pooled tool access; a PhD student's project is not absorbed into a larger effort or distilled without their consent and an offer of a place in the distillation working group; and senior members writing references for junior collaborators describe their collaboration work in full (verification, formalisation, data, exposition and distillation), not only their papers.

**Onboarding and entry points.** Each Strand Lead maintains a list of starter problems with accessible explanations, suitable for new members and PhD students. The annual workshop opens with an onboarding day covering repository practice, the methodology and verification conventions, and hands-on use of computational, AI and formalisation tools.

**External representation.** The SC designates one or two collaboration spokespeople, responsible for representing the community at external conferences, in communications with other research communities, and in any formal reporting to funding bodies. Spokespeople maintain a public-facing activity summary, updated at least annually and committed to the meta repo. Strand Leads, working group contacts, and PhD students are all encouraged to present collaboration work at external venues; major conference appearances are coordinated through the meta repo to avoid duplication and ensure adequate coverage.

**Public engagement.** The collaboration maintains a public page of open problems in its area with accessible explanations, and treats expository talks, videos and writing for non-specialist audiences as recognised contributions. Selected problems may be opened to participation from outside the collaboration, with moderated discussion and clear entry points.

## Governance

**Steering Committee.** The collaboration is governed by a Steering Committee (SC) of 7–9 members, representative across the North America, Europe, and East Asia blocs with no single bloc holding an absolute majority. The founding SC is constituted by the founding contributors; subsequent SC members are elected by core community members with staggered two-year terms, so that no more than half the committee turns over in a single election cycle. The SC operates async-first: most decisions are made by posting a proposal in the meta repo as an issue with a fixed comment window; monthly video calls handle matters requiring real-time discussion. SC members may hold designated strand affinities — informal responsibility for staying informed about a strand and liaising with its Lead — without acting as research directors for it.

**SC powers.** The SC has authority over: charter amendments (requiring a two-thirds SC majority and a [N]-day community comment period); appointment and removal of Strand Leads and Deputy Strand Leads; resolution of escalated disputes; the annual strategic review of whether the strand structure remains appropriate, including the power to open new strands or retire dormant ones; and designation of the collaboration spokesperson(s) for external representation. Day-to-day decisions — project acceptance, PR review, working group formation — remain at the Strand Lead and working group level.

**Strand Leads.** Each thematic repo has a Strand Lead and at least one Deputy Strand Lead, appointed by the SC. Strand Leads are responsible for: maintaining the GitHub repo (project proposal review, PR merges, INDEX.md upkeep); enforcing the charter's disclosure and verification standards within their strand; coordinating the strand's contribution to the collaboration seminar series; and mentoring junior contributors — particularly PhD students — working in their strand. Strand Lead is a service role, not a research directorship. Geographic diversity across blocs is encouraged in Lead and Deputy appointments; the same bloc should not hold both positions in a single strand.

**Membership tiers.** The collaboration has three membership tiers. *Public contributors* receive GitHub write access to any thematic repo on request to the relevant Strand Lead; the bar is deliberately low. *Community members* have declared affiliation with the collaboration — registered in the meta repo with a verified institutional affiliation and a seconder from any SC member — and may join working groups and propose projects. *Core members* are nominated by the SC on the basis of sustained documented contribution (completed project participation, working group leadership, seminar presentations, or equivalent), and are eligible to vote in SC elections and to serve as Strand Leads.

**Pooled resources and open participation.** Pooling resources is how the collaboration opens frontier research to everyone in the community. The SC seeks funding (from universities, funding agencies, philanthropy and partners) for compute, access to AI tools, administrative support and meeting costs, and holds AI and compute access centrally on behalf of the collaboration. Members draw on this pool through their working groups. Priority goes to early-career members and to members at institutions with fewer resources of their own. No member needs a personal frontier-model licence, a GPU allocation or institutional AI funding to take part. Computations run with pooled tools are committed to the open repositories, where anyone can read, check and build on them. The human core of the collaboration, the joint seminar and the preparation of the surveys, depends on none of these resources. Running a collaboration of this size is itself academic work; the SC reports its fundraising and allocation decisions in the annual report.

**External partnerships.** The SC may enter partnerships with AI laboratories, institutes, funding bodies and industry on behalf of the collaboration, on these terms: members of the collaboration set the research questions; each partnership includes concrete benefit for trainees, such as fellowships, compute or internships; repository content and members' interaction data are not supplied for model training except as the licences permit and after an explicit SC decision following community comment; and results obtained with a partner are reported under the collaboration's methodology rules.

**Disputes.** Disputes about project content, scope, attribution, or conduct are resolved hierarchically: first within the working group; then by the relevant Strand Lead (who may mediate before deciding); then by the SC, whose decision is final. Attribution disputes within a distillation working group are decided by that group; they escalate to the SC only if the group cannot reach agreement after a reasonable period. The SC may impose deadlines on escalated disputes to prevent indefinite deadlock.

**Charter amendments.** Proposed amendments are submitted as PRs against the charter in the meta repo. A community comment period of [N] days is observed before the SC votes; amendments require a two-thirds SC majority. Emergency amendments may be passed by unanimous SC vote with a shorter comment period, subject to ratification at the next scheduled coordination meeting.

## Code of Conduct

This community is built on the premise that mathematical research is better done collaboratively and openly. The norms that follow from that premise:

**Intellectual honesty.** Contributors represent their work accurately. AI-generated content is disclosed. Errors, once noticed, are corrected promptly and without defensiveness. A wrong calculation or a flawed argument is not a failure; an uncorrected or concealed one is.

**Credit.** Ideas and results that build on others' contributions are acknowledged, even informally, in commit messages or README notes. This applies within the community as well as to external sources. External results are cited accurately.

**Constructive engagement.** Critique of mathematical content is welcome and expected. Personal criticism, dismissiveness, or bad-faith engagement is not. Strand Leads may remove contributors who persistently violate this norm, subject to SC review.

**Unreleased ideas.** Using AI tools, or any other means, to exploit a colleague's unreleased ideas (including work in progress shared in the seminar, at the workshop, or in an open repository) is not acceptable. The repositories are public so that work can be shared early; that openness depends on no one racing others to their own results.

**Errors in the literature.** AI tools will expose errors in published work, including the collaboration's own. Before drawing conclusions, establish the significance of an error: a local slip and a gap that undermines a main argument call for different responses. Contact the authors first, as has always been the norm.

**Choice of methods.** Members' choices about whether and how to use AI tools are respected. No one is pressed to adopt, or to abandon, a way of working.

**Open science.** The repository is public. This is a feature, not a constraint. Contributors should not commit material they are not authorised to make public (e.g., unpublished results belonging to collaborators outside this community who have not consented).

**Scope of this document.** This code of conduct governs behaviour within the GitHub organisation and in community communication channels affiliated with it. It does not govern contributors' conduct elsewhere.

## Open Questions

The following items require a community decision before this charter is finalised. Each is flagged with a placeholder in the relevant section above.

- **Thematic repo list.** The four repos proposed (`foundations`, `solutions`, `structures`, `enhancements`) mirror the four research strands of the collaboration. Are these the right granularity? Should any be split further — e.g. should resurgence and RH methods have their own repo within Structures, or should refined invariants and 3D mirror symmetry sit in separate repos within Enhancements? Is a catch-all repo for cross-strand projects needed?
- **Proposal acknowledgement window.** The Project Lifecycle section reserves `[N]` days for a Strand Lead to acknowledge a project proposal. What is a realistic number given expected Strand Lead bandwidth?
- **Stall threshold.** The Working Groups section reserves `[N]` days of inactivity before a Strand Lead may archive a stalled project. What threshold is appropriate?
- **Charter amendment comment period.** The Governance section reserves `[N]` days for community comment on proposed charter amendments. What is the right window?
- **Founding Steering Committee.** The founding SC is constituted by the founding contributors. Who are these named individuals? What is the minimum threshold of core members that will trigger the first election cycle?
- **Initial Strand Leads.** Who are the initial Strand Leads and Deputy Strand Leads for each of the four thematic repos? (May overlap with the founding SC.)
- **AI verification floor.** The current text requires at least one human verifier per mathematical claim before a project is marked Complete. Is this the right bar? Should it be stricter (e.g., two independent verifiers for key results) or is a lighter-touch norm more appropriate for the workshop context?
- **Communication channels.** What are the official community communication channels affiliated with the GitHub organisation (Zulip, mailing list, etc.)?
- **Seminar frequency and format.** The charter proposes a weekly or biweekly online seminar. What cadence is realistic given the size and geographic spread of the collaboration? Should strand-level seminars supplement, or replace, a single collaboration-wide seminar?
- **PhD student representation in governance.** Should the core membership criteria include an explicit pathway for PhD students? Should the SC include at least one member who is a junior researcher (PhD student or postdoc)?
- **Licences.** Which licences apply to text and PDFs, code, and data? The charter proposes CC BY 4.0 for text, an OSI-approved licence for code, and CC0 or CC BY for data; the choice between permissive and share-alike licences for code is open.
- **Use of repository material for AI training.** Should the licences and About page permit, restrict or condition the use of repository content and members' interaction data for training AI models? This bears on both the licence choice and the terms of any partnership.
- **Claim status labels.** Are the five status labels the right set, and how are they rendered in PDFs (margin tags, colour, a claims table)?
