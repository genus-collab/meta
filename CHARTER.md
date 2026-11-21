# GENUS (Geometry, Enumeration, Strings): Charter v1.0

19 Nov 2026 · Andrea Brini

## Mission and Scope

**GENUS** is a public-domain collaborative workspace for research in topological strings and enumerative geometry. Its ambition is to coordinate and enhance the efforts of the global research community working on the subject, through a single shared platform. The natural comparison is the Polymath model — a public forum where research is done collectively, collaboratively, and openly.

The workspace will rely on a GitHub organisation with multiple repositories. The organisation is not a preprint server, and the PDFs and code they contain are rather work-in-progress documents – which we anticipate may often be AI-assisted and/or AI-driven. Authorship of the entirety of the content posted to the repositories will, by default, be collectively shared across the entire collaboration (“*The GENUS collaboration*”).

A selection of curated human-authored papers destined for arXiv may emerge from a separate distillation process, described below, with traditional authorship norms. In the short-to-mid term, we plan to extend the workspace to a broader community effort consisting of a series of joint activities, including an online regular seminar and conferences.

### Guiding principles

GENUS is inspired by the recommendations of the [CMSA-Harvard summit on Mathematical Research in the Age of AI](https://cmsa.fas.harvard.edu/media/2026/10/Summit-on-Math-Research-in-the-Age-of-AI.pdf).

- The measure of the collaboration's success is growth in human understanding of its subject.
- All the content of the GitHub organisation (code, draft notes, progress reports) will be open-source and available on the public domain (CC-BY-4.0). Members of the collaboration **waive personal authorship** on their outputs, with attribution shared across the collaboration (*The GENUS collaboration*) at the point of upload.
- Early-career people are central to the collaboration. A core objective of GENUS is to give PhD students and postdocs a place to do ambitious work, with visible contribution and credit, and increased equity of access.
- While the collaboration cannot *per se* democratise access to frontier AI tools, the shared nature of the repository allows all members to work on, build upon, and cross-validate the entirety of the research outputs produced by the collaboration, regardless of their origin.
- We anticipate many of the results of GENUS to be AI-driven. However, the human activity of the lab is not meant to reduce to a translation exercise of AI-generated results. Every kind of contribution that advances understanding will be recognised, with or without the use of AI. This will in the future include joint training and dissemination activities (conferences, online seminars, and working groups). Early-career researchers and PhD students will be central to this effort.
- Members of the collaboration will also coordinate, when and as appropriate, the creation of working groups to write curated, human-written surveys of topical results obtained within GENUS. Unlike the rest of the content of the repository, surveys will be conceived for submission to the arXiv and, potentially, to traditional peer-reviewed outlets. Authorship and credit for these surveys will be attributed to members of these working groups using the traditional rules of the mathematical community. Early-career researchers and PhD students will again be central in driving this effort.

The design of the collaboration addresses three central issues of the AI-transition in mathematical research.

- **Equity of fruition of AI-resources**. The collaboration doesn’t come with its own funding, nor does it have a direct relationship with any frontier lab. In particular, *access* to AI tools and tokens will necessarily be uneven across its membership. But *fruition and attribution* will be collective and homogeneous across the lab, regardless of entry barriers to compute resources.
- **International collaboration**. The public-domain nature of the repos removes artificial barriers to international collaboration, particularly where IP export-control restrictions apply to STEM disciplines.
- **Protection of the talent pipeline**. The development of PhD students and postdocs will be at the centre of the collaboration. Early career researchers will drive working groups, seminars, and the preparation of selected outward-facing traditional research outputs with named authorships, through which they will obtain appropriate recognition of their work.

### Topical scope

The collaboration's research is organised around four mutually reinforcing strands of inquiry, together aiming at a comprehensive mathematical understanding of topological string theory.

- **Foundations** — mathematical formulations of topological strings. Examples include: gauged linear sigma models (GLSM) and logarithmic compactifications, GW and FJRW theories, quantum Lefschetz theorems, LG/CY correspondence, GIT wall-crossing.
- **Solutions** — all-genus (perturbative) methods for Calabi–Yau threefolds. Examples include: BCOV theory, holomorphic anomaly equations, boundary data such as the conifold gap conjecture, GW/DT correspondence and MNOP-type results, DT wall-crossing and S-duality constraints on the partition function.
- **Structures** — global and nonperturbative structure. Examples include: wavefunction interpretations of the topological string, BPS invariants as Stokes data for Riemann–Hilbert problems, resurgence analysis, open/closed wavefunctions and quantum mirror curves.
- **Enhancements** — extensions and enrichments of curve-counting theories. Examples include: refined, motivic and K-theoretic enumerative invariants, refined GW/DT/PT correspondences, 3D mirror symmetry, enumerative geometry of higher-dimensional Calabi–Yau varieties.

## Repositories and Projects

GENUS is a single GitHub organisation with four thematic repos, one per strand (foundations, solutions, structures, enhancements); a shared knowledge repo, atlas, curating the collaboration's conjectures, examples and computed invariants together with their status and provenance; and an administrative repo, meta, holding this charter, templates and the master project index. Every repo displays its licence, and the organisation's About page states who maintains it and how contributed material may be used.

Each project is a self-contained directory holding its LaTeX source, compiled PDF, code, data and a README recording scope, status and methodology. Projects move through three stages. A project is **Proposed** when any community member opens an issue with the proposal template; the bar is deliberately low. It is **Active** once its directory is created, and work proceeds openly through commits and pull requests. It is **Complete** when its contributors judge the PDF to be a coherent body of results, its code reproduces the stated outputs, and its methodology statement is accurate. Stalled projects may be archived; nothing is deleted.

## Authorship, Credit and Publication

The repository is the **workshop**: public, raw, iterative, and collectively attributed. Workshop PDFs carry no individual author names: they are collectively credited to GENUS, with git history as a durable record of participation. Workshop PDFs may contain unpolished AI-generated output, and never go to the arXiv.

The arXiv and traditional journals are the **front store**. Working groups distil clusters of completed projects into human-written surveys, which carry named authorship under the usual conventions of the field. Every author is expected to understand the content of the survey in detail. Surveys will include a methodology section, cite the workshop projects they draw on, and acknowledge GENUS community. Distillation may also yield lecture notes, a data release or software. We expect a very small number of surveys relative to the number of projects/problems in the repositories.

Individual credit comes chiefly through these surveys and through internal seminar activity. The collaboration values the full range of work that advances understanding, including partial progress and experimentation, re-derivations, exposition, code and data, formalisation, checking and mentoring.

## AI Use and Verification

We anticipate that AI tools will be important in advancing progress for all of the strands, and that it will be unavoidable in driving the success of the more computational projects  (e.g. those naturally contained in the solutions repo). Yet, all kind of contributions will be valued, irrespective of AI-use.

Every project README includes a methodology statement recording which tools were used, for what, and what human verification was performed. Substantial AI transcripts are archived where the tool's terms permit.

Every claim in a workshop PDF carries a status label: *conjectural*, *numerically supported*, *AI-proposed, unchecked*, *proved (human-checked)* or *formally verified*. A claim counts as proved only once a contributor independent of its originator has checked it. Lean formalisation can be encouraged where the necessary background exists, though much of the collaboration's subject matter is not yet available in formal libraries.

## Working Groups and Community Activities

Working groups are informal and self-organising: any two or more members may form one around a project or a distillation, without approval. When groups discover substantial overlap, the default is to merge.

The following programme of activities is an ambition, to be realised as resources allow. A regular **online seminar** keeps the whole community informed across strands, combining invited talks, status talks from each active working group and teaching talks, with PhD student talks a central feature. A week-long **annual workshop**, rotating across North America, Europe and East Asia, brings together strand reports, working group sessions and time to launch new projects, and opens with an onboarding day for new members. Strand Leads hold a short monthly coordination meeting open to all. **PhD students** lead working groups and present their work, each with a named senior contact, and have priority for speaking slots, travel support and any pooled resources the collaboration secures. The SC designates spokespeople for external representation, and the collaboration maintains a public page of open problems.

## Governance and Conduct

A **Steering Committee (SC)** oversees the collaboration, and each strand is looked after by a **Strand Lead (SL)**, appointed by the SC. Cross-strand projects are welcome, and scope questions are resolved by the relevant SL.

**Steering Committee.** The SC has 7–9 members, balanced across the three geographic blocs. The founding SC consists of the founding contributors; later members are elected by core members on staggered terms. The SC works asynchronously through the meta repo. It amends the charter, appoints SLs, resolves escalated disputes, reviews the strand structure annually, seeks funding, and agrees any external partnerships on terms that keep research directions with the collaboration's members.

**Strand Leads.** Each strand has a SL and at least one deputy. This is a service role, not a research directorship. SLs review proposals, maintain the repo, uphold the methodology standards, coordinate the strand's part in the seminar and mentor junior contributors.

**Membership.** *Public contributors* receive write access on request. *Community members* register with a verified institutional affiliation and an SC seconder, and may propose projects and join working groups. *Core members*, nominated for sustained contribution, vote in SC elections and may serve as SLs.
