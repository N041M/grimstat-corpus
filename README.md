# grimstat-corpus

Tournament army lists for Warhammer 40,000, gathered weekly for the [Grimstat](https://github.com/N041M/Grimstat) app.

## What is here

Monthly files `lists-YYYY-MM.json` in Grimstat's published-lists format, and `index.json`, which names
them and the tournaments they hold. Each list carries its faction, its detachments, its placing, the
list text as the player submitted it, and a link to the tournament page it was read from.

The `listhammer/` folder holds files of the same kind for the lists Listhammer collects. Those lists
carry a win-loss record in place of a placing. The top-level `index.json` names the folder as a part,
so Grimstat reads both.

## Where it comes from

[MiniHeadQuarters](https://miniheadquarters.com), a tournament platform whose pages a machine may read.
The relay in the Grimstat repository (`.github/workflows/corpus.yml`) reads its ended Warhammer 40,000
tournaments every Monday, one request a second under a named user agent, and commits the result here.

The same relay reads [Listhammer](https://listhammer.info)'s feed of undefeated and one-loss lists from
Grand Tournaments into `listhammer/`. Listhammer collects them from events on Best Coast Pairings and
Tabletop Herald.

## Names

Player names are removed before publishing, including the header lines organisers ask players to fill
in. Lists are credited to the tournament they were played in.

## Licence

The compilation of the files at the top of this repository is published under CC BY 4.0 (see
`LICENSE`). That licence does not cover the `listhammer/` folder. The lists themselves were written by
the players who submitted them and remain theirs. This dataset reproduces them as published, for study of
the competitive field, with a link back to each source.

## Corrections and removals

Open an issue in this repository. A list is removed on request from its author or the organiser who
published it.

## Using it

In Grimstat, the Data page's **Fetch the published corpus** button reads this repository. The default
address is `https://raw.githubusercontent.com/N041M/grimstat-corpus/main/`.
