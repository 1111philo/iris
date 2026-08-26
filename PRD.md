# Iris — Product Requirements

**Version 0.1.** A draft to argue with, not a contract.

**Point Iris at anything. Ask about it. Act on the answer.**

**Built for blind people. Made for everyone.**

## Why

A blind person hits a wall several times a day. A PDF that reads as nothing. A form that needs
a stranger to fill it in. A ticket machine with no voice. A pill bottle that could be anything.

AI has made the visual world answerable. Today's tools describe a photograph and stop, belong to
someone else, and send what the camera caught to their servers. Iris takes follow-up questions,
acts on the answers, and runs on hardware the person controls.

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

### 3. Tools that work for everyone

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

## Cost and access

**Today Iris runs only on proprietary providers.** Changing that is Phase 1 work. Every release
publishes the free configuration's numbers beside the best. Paying buys speed, never better
answers or more rights. We never charge a person to read. Whoever runs an instance pays for it;
the public one runs on grants, and queues rather than closes.

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

## How we measure success

Blind people judge whether Iris is usable, paid for that work; a checker score never stands in.
There is no single success rate: [ROADMAP.md](ROADMAP.md) lists what each phase publishes, on a
public corpus fixed before we test. Someone outside this team sets Iris up in a day.

Only Phase 1 is a commitment. Architecture, models, funding, and hosting belong to each repo.
