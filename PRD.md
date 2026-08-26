# Iris — Product Requirements

**Version 0.1.** A draft to argue with, not a contract.

**Iris makes documents and screens readable by a blind person working alone, without handing
them to a stranger.**

## Why Iris exists

A blind person hits a wall several times a day. A PDF that reads as nothing. A form that
cannot be filled in without giving a stranger your private information. A ticket machine with
a flat glass screen and no voice. These barriers stay up because removing them has never made
money: the cost falls on whoever publishes, the harm on whoever reads.

Documents are where we start. They are the proving ground, not the destination.

## Who it is for

1. A blind or low-vision person, anywhere, using the device they already own.
2. The people and institutions who publish what that person needs to read.
3. The developers who extend Iris.

When a change helps publishers or developers at the cost of blind readers, we do not ship it.
Blind reviewers decide whether that has happened, and the reason is written down.

## The three rules

They hold in every phase, for every part. A proposal that breaks one gets changed, not
excused.

### 1. Plain language

Our documentation, interfaces, and error messages let a reader find what they need, understand
it, and use it. So must what Iris returns.

Iris does three things and labels which is which. It **transcribes** the author's words, never
reworded — OCR is transcription with an error rate we publish. It **infers** structure,
marking where it is unsure. It **describes** what has no words, in its own voice, so a reader
can tell by ear which words are the author's. Numbers are transcribed or marked unreadable,
never inferred.

### 2. AGPL-3.0-or-later

Every file we write is licensed AGPL-3.0-or-later, recorded in each repo, not only here.
Dependencies keep their own compatible licences; model weights and the documents Iris converts
are not covered. Plain GPL is not enough: its duties trigger on distribution, and a hosted
service never distributes. Anyone may run Iris. Anyone may charge for it. Anyone who
modifies it and serves it over a network owes their own users the source. What is released
stays free.

### 3. It runs on what people have

We build for one reader: a cheap Android phone on a connection that is slow and drops. So Iris
returns plain HTML that works with JavaScript off, images referenced rather than inlined so a
reader on a slow link chooses what to load. Speech is not the only output — braille and
large-print reflow are first-class, not exports. Every part of Iris runs on one rentable GPU,
from files anyone can download with no account, no licence click-through, no waiting list.

## Privacy: a person's document stays theirs

Not kept, not trained on, not shown to anyone, unless that person plainly chooses it. Error
reports carry no document content. Once a document has helped fix something in the open it
cannot be withdrawn, so we only ask for what we could stand behind publishing, and we say so
before we ask. This covers what a person hands to Iris, not what an institution publishes.
Iris exists to remove the stranger in the middle. It must never become one.

## Cost and access

**Today Iris runs only on hosted, proprietary model providers.** Changing that is Phase 1
work: a configuration built from freely licensed weights and self-hostable software, excluding
licences that restrict who may use them or for what. Every release publishes its numbers
beside the best configuration we have measured. Paying can buy speed. It must never buy a
better document, better answers, or more rights. We never charge a person to read; others may,
and the licence is what lets a person leave them. Compute is paid by whoever runs an instance; the
public one runs on grants, and queues rather than closes if they run out.

## What Iris must do

- **Read it.** Where a document already carries structure that can be trusted, use it rather
  than guess at it again.
- **Say where it could not read.** One marker per place, in reading order, with a reason —
  never a blanket disclaimer, never only a log. Detection is by evidence, not by the model's
  own confidence.
- **Never stand in for the original.** Every output says it is machine-made, links the source,
  and carries a way to report an error. Iris submits nothing for a person without a step that
  person controls, and says so where a misreading cannot be undone: medical, legal, financial.
- **Carry any language.** Language and direction travel as markup, including changes
  mid-sentence, and every word Iris adds is in the reader's language.
- **Fix itself.** Iris proposes repairs for its own errors; a maintainer approves them, and a
  blind reviewer approves any that touch what a reader receives.

## How we measure success

Blind people judge whether a document is usable, paid at a professional rate, budgeted before
a phase starts. A checker score never stands in for that: an empty page passes AA. There is no
single success rate — [ROADMAP.md](ROADMAP.md) lists what each phase publishes, on a public
corpus fixed before we test. And someone outside this team must be able to set Iris up from
the public repos in under a day, without our help.

Only Phase 1 is a commitment; these rules are written to outlast it. Architecture, models,
funding, and hosting belong to each component's repo, decided under these rules.
