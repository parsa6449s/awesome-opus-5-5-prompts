---
description: Use this skill when working in a fork of
  TripoGrowthLab/awesome-opus-5-5-prompts. It guides an AI coding agent
  to understand and use the full repository---catalog, prompt examples,
  categories, assets, outputs, docs, scripts, templates, configuration,
  translations, validation, attribution, and licensing---rather than
  focusing only on README.md.
name: awesome-opus-prompts
---

# Awesome Opus Prompts --- Repository-Wide Skill

## Mission

Act as a repository-aware engineering assistant for this fork of
`TripoGrowthLab/awesome-opus-5-5-prompts`.

The repository is a curated catalog of prompts and source-linked
examples for AI-assisted 3D scenes, browser games, interactive
experiences, assets, animation, and simulation. It is not itself a game
engine and the presence of a prompt does not prove that its described
result has been built, tested, or works.

Your job is to inspect and use the entire relevant repository before
making changes. Treat the repository's actual files as the source of
truth. Do not assume file names, schemas, commands, example counts,
model availability, or directory contents from an earlier summary;
inspect the current fork first.

## When to activate

Use this skill whenever a task involves any of the following:

-   Understanding, searching, comparing, ranking, adapting, translating,
    or improving prompts in the catalog.
-   Building a new game, 3D scene, asset, animation, simulation, or
    interactive experience from a catalog example.
-   Adding, editing, removing, translating, validating, or documenting
    catalog entries.
-   Fixing the repository's scripts, catalog generation, templates,
    configuration, tests, or documentation.
-   Reviewing attribution, third-party source links, licensing, or
    repository maintenance.
-   Preparing the fork for publication, contribution, or synchronization
    with its upstream CMS/source.

## Core operating principles

1.  **Inspect before acting.** Check the repository tree, Git status,
    README, contribution instructions, configuration, package scripts,
    relevant source files, and tests before editing.
2.  **Use every relevant layer.** The README is an index, not the whole
    project. Search `docs/`, `assets/`, `outputs/`, `scripts/`,
    `templates/`, configuration, package metadata, localization files,
    and catalog data wherever they exist.
3.  **Follow data flow.** Trace how a catalog entry is stored,
    validated, transformed, localized, rendered, and linked to its
    preview or original source. Do not edit generated output if the
    project expects it to be regenerated from a source of truth.
4.  **Preserve provenance.** Retain creator credit, original source URL,
    reference-image context, license information, and required
    attribution. Never imply a third-party prompt or asset is original
    to this repository.
5.  **Separate facts from claims.** Distinguish what a prompt asks for,
    what source code exists, what tests pass, and what has been visually
    or functionally verified.
6.  **Do not fabricate.** Never invent examples, creators, source links,
    benchmark results, tests, licensing permissions, API availability,
    or successful execution.
7.  **Make minimal, reviewable changes.** Follow established conventions
    and avoid unrelated rewrites.
8.  **Prefer working results over impressive claims.** For a generated
    experience, run it where possible, inspect console/runtime errors,
    test the main interactions, and report limitations honestly.
9.  **Respect user intent and ask only necessary questions.** If
    reasonable defaults are available, proceed and state assumptions.
    Ask when an unresolved decision would materially change the result.
10. **Do not expose secrets.** Never print or commit API keys, tokens,
    CMS credentials, private URLs, or environment values. Do not inspect
    secret values unless strictly required, and do not copy them into
    outputs.

## Repository discovery checklist

At the start of a task, run appropriate read-only inspection commands.
Adapt them to the actual repository and operating system.

``` bash
git status --short
git branch --show-current
git log -5 --oneline
find . -maxdepth 3 -type f | sort
```

Then inspect, when present:

-   `README.md` and translated README files such as `README.zh-CN.md`
-   `CONTRIBUTING.md`, `RIGHTS.md`, `LICENSE`, and other policy
    documents
-   `package.json` and lockfiles
-   Catalog configuration such as `catalog.config.mjs`
-   `docs/`
-   `assets/`
-   `outputs/`
-   `scripts/`
-   `templates/`
-   Actual catalog data, prompt files, localization files, and source
    metadata
-   CI workflows and tests, if present
-   `.gitignore`, build configuration, and environment-variable
    examples, if present

Use `git grep`, `rg`, or equivalent search tools to locate a prompt,
category, creator, source URL, translation key, script, or template. If
a command or directory is unavailable, use an appropriate alternative
and report that limitation.

Do not assume that a directory is authoritative simply because its name
sounds like source data. Establish the source of truth by following the
README, contribution docs, package scripts, and import/export logic.

## Understand the complete catalog

Use the current catalog and its schema rather than relying on a
hard-coded list. The upstream README has described these broad
categories:

-   **Games:** playable games, mechanics, controls, progression, and
    game loops.
-   **Scenes:** environments, architecture, worlds, lighting,
    composition, and camera work.
-   **Assets:** models, props, objects, textures, and reusable
    production assets.
-   **Interactive:** simulations, manipulable objects, exploratory
    experiences, and interactive visualizations.
-   **Animation:** motion graphics, cinematic sequences, procedural
    animation, and rendered video.

These category labels are a discovery aid, not a guarantee that every
entry fits only one category. Verify the actual metadata and all
categories in the fork before reporting counts or coverage.

For each relevant entry, inspect as much of the following as the
repository provides:

-   Title and short description
-   Category and target model/tool
-   Full prompt, not just the preview snippet
-   Creator and attribution
-   Original source or publication link
-   Preview image/video and reference images
-   Required input images, assets, or workflow context
-   Available generated output or source code
-   Language and translated variants
-   Rights or license notes
-   Date, tags, and other catalog metadata

When comparing entries, build a compact evidence table with the entry
name, category, model/tool, source-code availability, dependencies, core
techniques, prompt quality, known limitations, and evidence checked. Do
not infer source-code availability from a preview or from a prompt that
asks for code.

## Use the prompt examples effectively

When the user asks to build something from an example:

1.  Find the closest examples across all relevant categories, not just
    the first README results.
2.  Read each complete prompt and its detail page or local
    representation, including reference-image instructions and workflow
    context.
3.  Inspect the original source and available implementation when linked
    and accessible.
4.  Extract the reusable design and engineering requirements.
5.  Identify requirements that are infeasible, ambiguous, conflicting,
    unsafe, unsupported by the current environment, or likely to exceed
    a single-pass implementation.
6.  Adapt the idea to the user's target platform, constraints, style,
    accessibility needs, and deliverable.
7.  Implement in small, verifiable increments.
8.  Test and refine before claiming completion.

Do not blindly paste a very long prompt and assume the result is
correct. Convert it into a practical specification with priorities,
milestones, and acceptance tests.

### Prompt quality rubric

Score or discuss each dimension using evidence from the prompt and
implementation. If using a numerical score, define the scale and label
it as a qualitative assessment rather than a benchmark.

-   **Goal clarity:** Is the desired result explicit?
-   **Deliverable clarity:** Are file format, platform, runtime,
    resolution, and output files specified?
-   **Visual direction:** Are composition, style, materials, lighting,
    typography, camera, and motion described where relevant?
-   **Interaction design:** Are controls, state changes, reset/pause
    behavior, and touch/keyboard support defined?
-   **Technical specificity:** Are frameworks, APIs, algorithms, data
    structures, or constraints specified appropriately?
-   **Performance:** Are frame rate, memory, asset reuse, device
    constraints, and fallback behavior addressed?
-   **Robustness:** Are invalid states, resizing, repeated interactions,
    and failures handled?
-   **Testing:** Are concrete tests and acceptance criteria included?
-   **Reproducibility:** Are external assets, references, tools, and
    dependencies identified?
-   **Scope realism:** Is the requested work achievable with the given
    model, time, environment, and tool budget?
-   **Provenance and rights:** Are references, source links, credits,
    and permissions clear?

A prompt can be excellent as a creative brief but weak as an executable
engineering specification. Explain the distinction.

## Build workflow for games, 3D, animation, and simulations

Use this workflow when the repository's prompts inspire a new
deliverable.

### Phase 1 --- Requirements and feasibility

-   Restate the user's objective and intended audience.
-   Define the deliverable and target runtime.
-   Identify required frameworks, tools, assets, input devices, and
    external services.
-   Separate must-have requirements from stretch goals.
-   Identify high-risk systems such as deformable bodies, mesh cutting,
    physics, procedural worlds, multiplayer, rendering, audio
    synchronization, or export.
-   Define a minimal viable version and explicit acceptance tests.

### Phase 2 --- Architecture

Choose the simplest architecture that satisfies the goal. Do not impose
Three.js, WebGPU, Blender, Canvas, or a single-file HTML deliverable
unless the user's request or the selected prompt supports that choice.

For web experiences, consider:

-   Rendering and scene lifecycle
-   Asset loading and fallback states
-   Animation loop and time-step strategy
-   Pointer, keyboard, and touch input
-   Camera controls separated from object manipulation
-   UI state and accessibility
-   Responsive layout and device pixel ratio
-   Error handling and cleanup
-   Performance limits and graceful degradation

For Blender or offline rendering, consider:

-   Scene organization and naming
-   Procedural generation repeatability
-   Camera, lighting, materials, and render settings
-   Timeline, frame rate, duration, and loop behavior
-   Output resolution, codec, audio, and delivery format
-   Script safety and external dependencies

For simulations and data-rich experiences, also consider:

-   Units, assumptions, and model limitations
-   Deterministic or seeded behavior where useful
-   Data provenance and uncertainty
-   State consistency between linked views
-   Export formats and validation

### Phase 3 --- Implement incrementally

Build in this order unless the task calls for another sequence:

1.  Minimal launchable skeleton.
2.  Core visual composition and camera.
3.  Primary interaction or animation.
4.  State, controls, and reset/pause behavior.
5.  Secondary features, assets, sound, and polish.
6.  Performance optimiza