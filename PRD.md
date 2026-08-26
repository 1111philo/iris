# Iris — Product Requirements

**Version 0.1.** A draft to argue with, not a contract.

**Point Iris at anything. Ask about it. Act on the answer. Built for blind people. New for
everyone.**

## Why

A blind person hits a wall several times a day. A PDF that reads as nothing. A form that needs
a stranger to fill it in. A ticket machine with no voice. A pill bottle that could be anything.
They stay up because removing them has never made money.

AI has made the visual world answerable. Today's tools describe a photograph and stop, belong to
someone else, and send what the camera caught to their servers. Build it for the person who
cannot see at all and you get what nobody had: ask what is in front of you, then act. Curb cuts
were built for wheelchairs; everyone uses them, and they never stopped working for wheelchairs.

Documents are the proving ground, not the destination.

## Who

A blind or low-vision person, anywhere, on the device they own. Then publishers, developers,
and anyone who cannot look right now — hands full, driving, in the dark, holding a language they
do not read.

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

### 3. Cheap devices, best tools

A cheap Android phone on a slow connection that drops — camera as well as screen — is what we
build for, and it caps nothing. The phone is where the answer arrives, not where the work
happens, so Iris uses the most accurate tools it can reach. What comes back is plain HTML that
works with JavaScript off, images referenced not inlined. Braille and large print are
first-class, not exports. There is always a path that runs on one rentable GPU, from files
anyone can download with no account and no wait.

## Privacy

Not kept, not trained on, not shown to anyone, unless the person plainly chooses it. Error
reports carry no content. What helped fix a bug in the open cannot be withdrawn, so we only ask
for what we could stand behind publishing. This covers what a person hands Iris, not what an
institution publishes. A camera catches more than it was aimed at, and its holder is least able
to check. Iris exists to remove the stranger in the middle. It must never become one.

## Cost and access

**Today Iris runs only on proprietary providers.** Changing that is Phase 1 work. Every release
publishes the free configuration's numbers beside the best. Paying buys speed, never better
answers or more rights. We never charge a person to read. Whoever runs an instance pays for it;
the public one runs on grants, and queues rather than closes.

## What Iris must do

- **Answer, don't just describe.** One description is never enough; a person asks again, closer.
- **Say where it could not read.** One marker per place with a reason, never a blanket
  disclaimer. Detection is by evidence, not the model's confidence.
- **Never stand in for the original.** Output says it is machine-made and links the source. Iris
  submits nothing without a step the person controls, and flags where a misreading cannot be
  undone: medical, legal, financial.
- **Act.** Reading a form is half of it. Where Iris can speak to a thing, the person tells it
  what to do and stays in charge.

## How we measure success

Blind people judge whether Iris is usable, paid for that work; a checker score never stands in.
There is no single success rate: [ROADMAP.md](ROADMAP.md) lists what each phase publishes, on a
public corpus fixed before we test. Someone outside this team sets Iris up in a day.

Only Phase 1 is a commitment. Architecture, models, funding, and hosting belong to each repo.
