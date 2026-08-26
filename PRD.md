# Iris — Product Requirements

**Version 0.1.** A draft to argue with, not a contract.

**Iris turns anything you would have to look at — a page, a screen, a room — into something
you can ask. Built for blind people. New for everyone.**

## Why Iris exists

A blind person hits a wall several times a day. A PDF that reads as nothing. A form that needs
a stranger's help to fill in. A ticket machine with no voice. A medicine bottle that could be
anything. These barriers stay up because removing them has never made money: the cost falls on
whoever publishes, the harm on whoever reads.

AI has made the visual world answerable for the first time. The tools that describe a
photograph today stop at describing, belong to someone else, and send what the camera caught to
their servers. Build this properly for the person who cannot see at all and you get something
nobody had: you can ask what is in front of you, then act on the answer. Curb cuts were built
for wheelchairs; everyone uses them, and they never stopped working for wheelchairs.

Documents are where we start: the proving ground, not the destination.

## Who it is for

Iris is built for a blind or low-vision person, anywhere, on the device they already own.
Everything else follows from that — the people and institutions who publish what that person
needs, the developers who extend Iris, and everyone who cannot look right now: hands full,
driving, in the dark, or holding a page in a language they do not read.

Blind people hold the veto. When a change helps anyone else at their cost we do not ship it,
and blind reviewers decide whether it has.

## The three rules

They hold in every phase, for every part. A proposal that breaks one gets changed, not excused.

### 1. Plain language

Our documents, interfaces, and errors let a person find what they need, understand it, and use
it. So must what Iris returns. Iris does three things and labels which is which. It
**transcribes** words that exist, never rewording them — OCR is transcription with an error
rate we publish. It **infers** structure, marking where it is unsure. It **describes** what has
no words, in its own voice, so a person can tell whose words are whose. Numbers are transcribed
or marked unreadable, never inferred.

### 2. AGPL-3.0-or-later

Every file we write, recorded in each repo and not only here. Dependencies keep their own
compatible licences; model weights and whatever Iris reads are not covered. Plain GPL is not
enough: its duties trigger on distribution, and a hosted service never distributes. Anyone may
run Iris. Anyone may charge for it. Anyone who modifies it and serves it over a network owes
their own users the source. What is released stays free.

### 3. It runs on what people have

We build for one person: a cheap Android phone on a slow connection that drops — the camera as
well as the screen. What Iris returns is plain HTML that works with JavaScript off, images
referenced not inlined so a reader chooses what to load. Speech is not the only output —
braille and large-print reflow are first-class, not exports. Every part of Iris runs on one
rentable GPU, from files anyone can download with no account, no licence click-through, no
waiting list.

## Privacy: what Iris sees stays the person's

Not kept, not trained on, not shown to anyone, unless that person plainly chooses it. Error
reports carry no content. Once something has helped fix a bug in the open it cannot be
withdrawn, so we only ask for what we could stand behind publishing, and say so first. This
covers what a person hands to Iris, not what an institution publishes. A camera catches more
than it was pointed at, and its holder is least able to check. Iris exists to remove the
stranger in the middle. It must never become one.

## Cost and access

**Today Iris runs only on hosted, proprietary model providers.** Changing that is Phase 1 work.
Every release publishes the free configuration's numbers beside the best we have measured.
Paying buys speed; it must never buy better answers or more rights. We never charge a person to
read; others may, and the licence is what lets them leave. Compute is paid by whoever runs an
instance; the public one runs on grants, and queues rather than closes if they run out.

## What Iris must do

- **Read it, then answer about it.** One description is never enough. A person can ask again,
  and closer, until they have what they came for.
- **Say where it could not read.** One marker per place, in reading order, with a reason, never
  a blanket disclaimer. Detection is by evidence, not the model's own confidence.
- **Never stand in for the original.** Output says it is machine-made, links the source, and
  carries a way to report an error. Iris submits nothing for a person without a step that
  person controls, and says so where a misreading cannot be undone: medical, legal, financial.
- **Act, not only describe.** Reading a form is half of it. Where Iris can speak to a thing,
  the person tells it what to do and stays in charge.
- **Carry any language.** Language and direction travel as markup, and every word Iris adds is
  in the person's language.

## How we measure success

Blind people judge whether Iris is usable, paid for that work. A checker score never stands in:
an empty page passes AA. There is no single success rate — [ROADMAP.md](ROADMAP.md) lists what
each phase publishes, on a public corpus fixed before we test. And someone outside this team
must be able to set Iris up from the public repos in a day, without our help.

Only Phase 1 is a commitment; these rules outlast it. Architecture, models, funding, and
hosting belong to each component's repo, decided under these rules.
