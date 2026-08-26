# Iris

**Iris turns anything you would have to look at — a page, a screen, a room — into something you
can ask. Built for blind people. New for everyone.**

Documents are where we start. How the service converts one is documented in
[equalify-iris](https://github.com/EqualifyEverything/equalify-iris).

**This repo is the hub for the whole Iris project.** It carries the product requirements, the
roadmap, and the map of which repo does what. It is not where the code lives — each moving
part keeps its own repo, listed below.

---

## Start here

| Document | What it is |
| --- | --- |
| [PRD.md](PRD.md) | Product requirements for Iris as a whole — the problem, who it's for, what it must do |
| [ROADMAP.md](ROADMAP.md) | Where the project is going, in what order, and what is done |
| [Iris: Beyond Solving Blindness](https://philosophers.group/iris-beyond-solving-blindness/) | The vision the roadmap follows — why documents are the proving ground and not the destination |

Per-component requirements and design live in each component's own repo. This repo holds the
requirements that span them.

Three rules hold everywhere in Iris, in every phase and every repo — they're set out in
[PRD.md](PRD.md):

1. **Plain language.** What Iris returns, and everything we write about it.
2. **AGPL-3.0-or-later.** Anyone may run it, anyone may charge for it, and anyone who modifies
   it and serves it over a network owes their own users the source.
3. **It runs on what people have.** A cheap phone on a bad connection is the reference, and
   any group can run all of Iris on one rentable GPU.

## Projects

A running list, not a finished architecture. Iris is built as separate projects, and this list
grows as the roadmap opens new phases. Everything here is Phase 1.

| Project | What it is | State |
| --- | --- | --- |
| [equalify-iris](https://github.com/EqualifyEverything/equalify-iris) | The service. Image-to-accessible-HTML pipeline and API. This is the core. | Active |
| [equalify-iris-bench](https://github.com/EqualifyEverything/equalify-iris-bench) | Benchmark harness. Give it a CSV of PDF URLs; it reports success rate, latency, and cost per page against any deployment. | Active |
| [equalify-iris-wp](https://github.com/EqualifyEverything/equalify-iris-wp) | WordPress multisite plugin. Finds PDFs linked from published pages, converts them, publishes the accessible version, and links to it from every PDF link. | Repo is empty and unlicensed |
| [iris.equalify.uic.edu](https://github.com/UIC-OSF/iris.equalify.uic.edu) | Terraform for the UIC test deployment. One EC2 box running the service behind Caddy. | Not publicly readable |

The plugin and the benchmark harness both call the service; Terraform deploys it.

They stay separate on purpose: the service does not carry a WordPress plugin's dependencies, a
benchmark's gigabytes of cached PDFs, or one institution's deployment choices. What they share
— the rules, the priorities, the sequencing — lives here.

**Adding a project.** Open an issue here first. A new project needs a phase it serves and a
reason it is not part of an existing one. The three rules apply to it from its first commit,
and it gets a row above on its first day, whatever state it is in.

## Contributing

Issues that concern the project as a whole — scope, priorities, cross-component decisions —
belong here. Bugs and changes in a specific component belong in that component's repo.

## License

Copyright (C) 2026 Blake Bertuccelli-Booth. Licensed under the GNU Affero General Public
License, version 3 or later (`AGPL-3.0-or-later`). See [LICENSE](LICENSE).

This repo was relicensed from GPL-3.0 to AGPL-3.0-or-later on 26 August 2026. Relicensing
needs every copyright holder's agreement, so that agreement should be recorded here by the
holders themselves. There is no CLA and no copyright assignment; contributions come in under
the same licence they go out under.

The WordPress plugin is AGPL-3.0-or-later too. That is compatible with WordPress core
(GPLv2-or-later, taken to GPLv3, via AGPLv3 §13), but it means the plugin is distributed from
its own repo rather than the WordPress.org directory, which requires GPLv2-or-later
compatibility.
