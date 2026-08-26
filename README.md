# Iris

**Point Iris at anything. Ask about it. Act on the answer.**

**Built for blind people. New for everyone.**

Documents are where we start. How the service converts one is in
[equalify-iris](https://github.com/EqualifyEverything/equalify-iris).

**This repo is the hub.** It holds the requirements, the roadmap, and the list of projects. The
code lives in the projects below.

---

## Start here

| Document | What it is |
| --- | --- |
| [PRD.md](PRD.md) | What Iris must do, and for whom |
| [ROADMAP.md](ROADMAP.md) | What we build, in what order |
| [Iris: Beyond Solving Blindness](https://philosophers.group/iris-beyond-solving-blindness/) | The vision the roadmap follows |

Three rules hold in every phase and every repo. [PRD.md](PRD.md) has the reasoning.

1. **Plain language.** What Iris returns, and everything we write about it.
2. **AGPL-3.0-or-later, and no vendor lock.** Run it, charge for it, fork it. Modify it and
   serve it over a network and you owe your users the source. Nothing in Iris may require a
   proprietary tool or service — a licence to run it is worthless if it only runs on one
   company's platform.
3. **Cheap devices, best tools.** A cheap phone on a bad connection is what we build for, and
   it caps nothing. The phone is where the answer arrives, not where the work happens. Always a
   path that runs on one rentable GPU — which is not true yet: today the service runs only on
   hosted, proprietary providers, and fixing that is Phase 1 work.

## Projects

A running list. It grows as the roadmap opens phases. Everything here is Phase 1.

| Project | What it is | State |
| --- | --- | --- |
| [equalify-iris](https://github.com/EqualifyEverything/equalify-iris) | The service. Images in, accessible HTML out. This is the core. | Active |
| [equalify-iris-bench](https://github.com/EqualifyEverything/equalify-iris-bench) | Benchmarks. Give it a CSV of PDF URLs; it reports success rate, latency, and cost per page against any deployment. | Active |
| [equalify-iris-wp](https://github.com/EqualifyEverything/equalify-iris-wp) | WordPress multisite plugin. Finds linked PDFs, converts them, publishes the accessible version. | Empty, unlicensed |
| [iris.equalify.uic.edu](https://github.com/UIC-OSF/iris.equalify.uic.edu) | Terraform for the UIC test deployment. One EC2 box behind Caddy. | Not public |

The plugin and the benchmarks both call the service. Terraform deploys it. They stay separate so
the service does not carry a plugin's dependencies, a benchmark's cached PDFs, or one
institution's deployment choices.

**Adding a project.** Open an issue here first. Say which phase it serves and why it is not part
of an existing project. The three rules apply from its first commit, and it gets a row above on
day one, whatever state it is in.

## Contributing

Project-wide issues — scope, priorities, decisions that cross projects — belong here. Bugs
belong in the project they affect.

## License

Copyright (C) 2026 Blake Bertuccelli-Booth. AGPL-3.0-or-later. See [LICENSE](LICENSE).

Relicensed from GPL-3.0 on 26 August 2026. Relicensing needs every copyright holder's agreement,
which the holders should record here themselves. No CLA, no copyright assignment.

The WordPress plugin is AGPL-3.0-or-later too. That works with WordPress core (GPLv2-or-later,
taken to GPLv3, via AGPLv3 §13), but it ships from its own repo rather than the WordPress.org
directory, which requires GPLv2-or-later.
