# Iris — Product Requirements

**Version 0.1.** A draft to argue with, not a contract.

**Iris makes documents and screens readable by a blind person working alone, without handing
them to a stranger.**

## Why Iris exists

A blind person hits a wall several times a day. A PDF that reads as nothing. A form that needs
a stranger's help to fill in. A ticket machine with no voice. These barriers stay up because
removing them has never made money: the cost falls on whoever publishes, the harm on whoever
reads. Documents are where we start — the proving ground, not the destination.

## Who it is for

1. A blind or low-vision person, anywhere, on the device they already own.
2. The people and institutions who publish what that person needs to read.
3. The developers who extend Iris.

When a change helps publishers or developers at the cost of blind readers, we do not ship it.
Blind reviewers decide whether it has, and the reason is written down.

## The three rules

They hold in every phase, for every part. A proposal that breaks one gets changed, not excused.

### 1. Plain language

Our documents, interfaces, and errors let a reader find what they need, understand it, and use
it. So must what Iris returns. Iris does three things and labels which is which. It
**transcribes** the author's words, never reworded — OCR is transcription with an error rate we
publish. It **infers** structure, marking where it is unsure. It **describes** what has no
words, in its own voice, so a reader can tell by ear whose words are whose. Numbers are
transcribed or marked unreadable, never inferred.

### 2. AGPL-3.0-or-later

Every file we write, recorded in each repo and not only here. Dependencies keep their own
compatible licences; model weights and converted documents are not covered. Plain GPL is not
enough: its duties trigger on distribution, and a hosted service never distributes. Anyone may
run Iris. Anyone may charge for it. Anyone who modifies it and serves it over a network owes
their own users the source. What is released stays free.

### 3. It runs on what people have

We build for one reader: a cheap Android phone on a slow connection that drops. Iris returns
plain HTML that works with JavaScript off, images referenced not inlined so a reader chooses
what to load. Speech is not the only output — braille and large-print reflow are first-class,
not exports. Every part of Iris runs on one rentable GPU, from files anyone can download with
no account, no licence click-through, no waiting list.

## Privacy: a person's document stays theirs

Not kept, not trained on, not shown to anyone, unless that person plainly chooses it. Error
reports carry no document content. Once a document has helped fix something in the open it
cannot be withdrawn, so we only ask for what we could stand behind publishing, and say so
first. This covers what a person hands to Iris, not what an institution publishes. Iris exists
to remove the stranger in the middle. It must never become one.

## Cost and access

**Today Iris runs only on hosted, proprietary model providers.** Changing that is Phase 1 work.
Every release publishes the free configuration's numbers beside the best we have measured.
Paying buys speed; it must never buy a better document, better answers, or more rights. We
never charge a person to read; others may, and the licence is what lets them leave. Compute is
paid by whoever runs an instance; the public one runs on grants, and queues rather than closes
if they run out.

## What Iris must do

- **Read it.** Where a document already carries structure that can be trusted, use it rather
  than guess again.
- **Say where it could not read.** One marker per place, in reading order, with a reason, never
  a blanket disclaimer. Detection is by evidence, not the model's own confidence.
- **Never stand in for the original.** Output says it is machine-made, links the source, and
  carries a way to report an error. Iris submits nothing for a person without a step that
  person controls, and says so where a misreading cannot be undone: medical, legal, financial.
- **Carry any language.** Language and direction travel as markup, and every word Iris adds is
  in the reader's language.

## How we measure success

Blind people judge whether a document is usable, paid for that work. A checker score never
stands in: an empty page passes AA. There is no single success rate — [ROADMAP.md](ROADMAP.md)
lists what each phase publishes, on a public corpus fixed before we test. And someone outside
this team must be able to set Iris up from the public repos in a day, without our help.

Only Phase 1 is a commitment; these rules outlast it. Architecture, models, funding, and
hosting belong to each component's repo, decided under these rules.
