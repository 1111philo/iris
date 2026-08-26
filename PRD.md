# Iris — Product Requirements

**Version 0.1.** A draft to argue with. Not a contract yet.

**Point Iris at anything. Ask about it. Act on the answer.**

**Built for blind people. Made for everyone.**

## Why

A blind person hits a wall several times a day. A PDF that reads as nothing. A form that needs
a stranger to fill it in. A ticket machine with no voice. A pill bottle that could be anything.

AI has made the visual world answerable. Be My AI is the best of what exists — free to blind
users, and genuinely good. It is also closed, runs on one company's model, sends what the camera
caught to that company's servers, describes a photograph and stops, and publishes no accuracy
numbers anyone can check. Iris takes follow-up questions, acts on the answers, runs where its
operator chooses, and publishes what it gets wrong.

We start by making PDFs and other documents accessible. That is the proving ground, not the
destination.

## Who

Blind people first. Everyone else benefits from an interface that enhances vision.

Blind people hold the veto: when a change helps anyone else at their cost we do not ship it, and
blind reviewers decide when that happened.

## The three rules

Every phase, every part. A proposal that breaks one gets changed, not excused.

### 1. Plain language

Our writing and Iris's output both let a person find what they need, understand it, and use it.
Iris labels its three acts. It **transcribes** words that exist, never rewording them — OCR is
transcription with an error rate we publish. It **infers** structure, marking where it is
unsure. It **describes** what has no words, in its own voice. Numbers are transcribed or marked
unreadable, never guessed. Language and direction travel as markup, and every word Iris adds is
in the person's own.

### 2. AGPL-3.0-or-later

Every file we write, recorded in each repo. Dependencies keep their own licences; weights and
what Iris reads are not covered. Plain GPL is not enough: its duties trigger on distribution,
and a hosted service never distributes. Anyone may run Iris or charge for it; anyone who
modifies it and serves it over a network owes their users the source. What is released stays
free.

A licence to run Iris is worthless if Iris only runs on one company's platform. Nothing in Iris
may require a proprietary tool or service. Every hosted provider is a swappable option behind
an interface, never a dependency, and every part deploys on infrastructure its operator picks.
Cloud-specific deployments are examples, not the path.

### 3. Powerful tools for everyone

Nobody is shut out by their device, their connection, or their money, and nobody gets a lesser
Iris for it. We build for a cheap Android phone on a slow connection that drops — camera as
well as screen — and that caps nothing: the phone is where the answer arrives, not where the
work happens, so Iris uses the most accurate tools it can reach. What comes back is plain HTML
that works with JavaScript off, images referenced not inlined. Braille and large print are
first-class, not exports. There is always a path that runs on one rentable GPU, from files
anyone can download with no account and no wait.

## Privacy

Not kept, not trained on, not shown to anyone, unless the person plainly chooses it. Error
reports carry no content. What helped fix a bug in the open cannot be withdrawn, so we only ask
for what we could stand behind publishing. This covers what a person hands Iris, not what an
institution publishes. A camera catches more than it was aimed at, and the person holding it
cannot check. Iris must not become the stranger it exists to remove.

## What Iris must do

- **Answer, don't just describe.** A person asks follow-up questions until they have what they
  came for.
- **Say where it could not read.** One marker per place with a reason, never a blanket
  disclaimer. Detection is by evidence, not the model's confidence.
- **Never stand in for the original.** Output says it is machine-made and links the source. Iris
  submits nothing without a step the person controls, and flags where a misreading cannot be
  undone: medical, legal, financial.
- **Act.** Where Iris can speak to a thing, the person tells it what to do and stays in charge.
  Reading a form is not finishing it.

## Speed

Iris is built agentically: agents write it, people review it. That is the design, not a
shortcut. The distance between a blind person hitting a wall and a shipped fix should be hours,
and the rules above are what make that safe to do at speed — a fix that breaks one does not
ship. The tools that exist have had years and still stop at describing.

We go from reading documents, to operating devices, to sight itself, as fast as the work allows.
[ROADMAP.md](ROADMAP.md) sequences it.

## The demo

Iris becomes an app that can see the world, and we show it to Stevie Wonder.

He drove the Marrakesh Treaty through the UN to end the book famine for blind readers, and told
the Grammys that every single thing should be accessible to every single person with a
disability. He has been asking for this for forty years. He has not asked us, and owes us
nothing.

Everything in this document is the work up to that demo. If it does not convince him, it is not
finished.

Only Phase 1 is a commitment. Architecture, models, funding, and hosting belong to each repo.
