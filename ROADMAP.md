# Iris — Roadmap

Sequencing across all Iris repos. See [README.md](README.md) for the repo map.

This roadmap is deliberately coarse. The near phases are concrete because we're in them; the
far phases are directions, not commitments. It follows the arc laid out in
[**Iris: Beyond Solving Blindness**](https://philosophers.group/iris-beyond-solving-blindness/)
— documents are the proving ground, not the destination.

Every phase below is bound by the three rules in [PRD.md](PRD.md): plain language,
AGPL-3.0-or-later, and it runs on what people already have. A phase that can only be reached
by breaking one of them is not on this roadmap yet.

---

## Phase 1 — Documents can be read

*Where we are now.*

Convert inaccessible documents into accessible HTML. A PDF that a screen reader can't use
becomes a real web page that it can. Prove the core claim: that software can interpret visual
information accurately enough to be trusted.

- Image-to-accessible-HTML service, AGPL-3.0-or-later
- Output that loads on a cheap phone over a bad connection and needs no JavaScript to read
- A configuration built only from freely licensed weights and self-hostable software. **This
  does not exist yet** — the service ships hosted-provider adapters only, and closing that gap
  is Phase 1 work.
- Per page, published every release on a public corpus fixed before we test: fidelity against
  a human transcript, reading-order and table correctness, invented-content rate,
  dropped-content rate, time, and cost with the hardware it assumes. Free configuration and
  best configuration, side by side. A release that raises invented content does not ship.
- Deployment anyone can stand up in under a day, on one rentable GPU

**Open gaps in Phase 1, as of this writing.** The WordPress plugin repo is empty and carries
no licence. The deployment repo is not publicly readable. Until both are fixed, the PRD's
"someone outside this team sets Iris up from the public repos" cannot be met.

## Phase 2 — Documents can be completed

Reading a form is half of it. A blind person handed an airline form, a TSA form, an intake
form needs to fill it in and send it back — without a third party in the middle.

- Reverse path: accessible HTML back into the original document
- Filled, signed, submitted, without sighted assistance
- Delivered as a public app, not just a service for developers

## Phase 3 — Documents at scale, everywhere they live

The billions of documents already published, in the systems people already use. The work here
is reach, not new capability.

- Integration into the platforms that host documents (CMSes, portals, repositories)
- Conversion as an automatic property of publishing, invisible to editors
- Institutions running it across their whole footprint

## Phase 4 — The agents outgrow documents

Iris improves itself through an agentic feedback loop: when content isn't articulated
properly, an agent writes a fix and submits it for review. As document problems are exhausted,
that loop turns outward to problems that aren't documents.

- Interpretation generalizes past the page
- Self-extension becomes the primary way capability grows. Iris proposes repairs for its own
  errors; a maintainer approves them, and a blind reviewer approves any that touch what a
  reader receives.
- The corpus of "things Iris can read" stops being a list we maintain

## Phase 5 — Any interface, spoken to

Point Iris at a screen — phone, kiosk, ATM, appliance, ticket machine — and talk to it. If it
can also speak to the device, it can operate it.

- The person says: *Send this email. Buy this ticket. Turn the heat down. Show me my balance.*
- No screen reader, no per-device accessibility settings, no waiting on manufacturers
- Iris as the accessibility interface: a universal layer between people and the visual
  technology around them

New hardware never becomes the only way in. Everything from here on has to keep working for
someone holding an ordinary phone, or it is just an expensive product with our name on it.

## Phase 6 — SightOS

Reading evolves into an operating system for sight. Not a tool you open, but the thing
standing between a person and the visual world, everywhere, all the time.

- Identity and consent handled by biomarkers rather than typed credentials — which the
  privacy rule in [PRD.md](PRD.md) does not currently permit. Either that rule changes with
  its reasons written down, or this does.
- The computer small enough to be worn, private enough that the data goes nowhere
- Sight as a service the person controls

## Phase 7 — Sight itself

The far end. A device you pop in each morning, or choose to have permanently implanted, that
narrates the world — and eventually connects directly to the visual cortex. Blindness
eradicated rather than accommodated.

This is science fiction today. It's on the roadmap because it's the direction the earlier
phases point, and because advances in AI and computing keep shortening the distance.

---

*What comes after solving blindness is an open question. We'll get there and find out.*
