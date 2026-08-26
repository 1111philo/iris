# Iris — Product Requirements

**Version 0.1.** A draft to argue with, not a contract.

**Iris turns visual information into something a person can read, understand, and act on,
with nobody in the middle.**

## Why Iris exists

A blind person hits a wall several times a day. A PDF that reads as nothing. A form that
cannot be filled in without handing a stranger your private information. A ticket machine
with a flat glass screen and no voice. These walls stand not because the problems are hard,
but because removing them has never made anyone money. Documents are where we start —
everywhere, and easy to measure. They are the proving ground, not the destination.

## Who it is for

1. A blind or low-vision person, anywhere, using the device they already own.
2. The people and institutions who publish what that person needs to read.
3. The developers who extend Iris.

When a change helps group 2 or 3 at the cost of group 1, we do not ship it.

## The three rules

They hold in every phase, for every part. A proposal that breaks one gets changed, not
excused.

**1. Plain language.** Our documentation, interfaces, and error messages let a reader find
what they need, understand it, and use it. So does what Iris hands back — with one hard
limit. Iris makes a document's *structure* plain; it never rewrites the author's words. A tax
form paraphrased is a tax form falsified. Real headings, honest reading order, real tables,
described images.

**2. AGPL v3.** Every line of Iris is under the GNU Affero General Public License, version 3.
Plain GPL is not enough: Iris will mostly be used as a service over a network, and only the
AGPL makes whoever runs that service publish their changes back. Anyone may run Iris. Anyone
may sell it. Nobody may take it private.

**3. It runs on what people have.** Our reference reader is on a cheap Android phone over a
slow connection that drops, so Iris returns plain HTML: small, readable without JavaScript,
standard enough for whatever screen reader that person already has. And any group must be
able to run all of Iris on hardware they can rent, without asking us or anyone else.

## One promise

A person's document is theirs. Not kept, not trained on, not shown to anyone, unless they say
so plainly and can take it back later. Iris learns from what broke, never from what it read.
We exist to remove the stranger in the middle. We do not get to become one.

## The floor and the ceiling

There is always a configuration of Iris that depends on nothing proprietary. We test it, and
publish its numbers beside the best configuration we know of. Better tools may make Iris
faster, sharper, and cheaper, and whoever can afford them should use them. What better tools
may never buy is access: the same document, the same answer, the same rights, arriving more
slowly. We never charge a person to read.

Two sets of numbers, side by side, keep that honest. The distance between them is the work.

## What Iris must do

- **Read it.** Visual information in; something a screen reader can read out.
- **Admit what it could not read.** A confident wrong answer is worse than an honest gap, and
  the gap belongs in the output where the reader meets it, not in a log.
- **Carry any language.** Nothing in Iris assumes English, or that lines run left to right.
- **Let the person act, not only read.** Reading a form is half of it.
- **Fix itself.** When Iris gets something wrong it proposes the repair; a person approves it.

## How we will know

- Blind people judge whether a document is usable, and are paid for that work. Passing an
  automated checker is not the same as being readable, and never stands in for it.
- Success rate, speed, and cost per page are measured on a real corpus and published for
  anyone to check, failures included.
- Someone outside this team stands up their own Iris from the public repos, unaided.

What is not settled here — architecture, models, funding, hosting — belongs to each
component's repo, decided under these rules. Sequencing lives in [ROADMAP.md](ROADMAP.md).
