# grimstat-corpus

Tournament army lists for Warhammer 40,000, gathered weekly for the [Grimstat](https://github.com/N041M/Grimstat) app.

## What is here

Monthly files `lists-YYYY-MM.json` in Grimstat's published-lists format, and `index.json`, which names
them and the tournaments they hold. Each list carries its faction, its detachments, its placing, the
list text as the player submitted it, and a link to the tournament page it was read from.

The `listhammer/` folder holds files of the same kind for the lists Listhammer collects. Those lists
carry a win-loss record in place of a placing, and a list from a smaller event (an RTT) is marked
`rtt`. A list from a Grand Tournament also carries its games: each round's result and score, and the
opponent's faction and detachments.

The same folder holds monthly `results-YYYY-MM.json` files. Each names an event, its date, its number
of rounds and the number of players it had, and lists every player's faction, detachments, Force
Disposition and record in finishing order. Grimstat reads them for each faction's win rate across
whole events, since the list files hold only the lists that lost once at most.

The top-level `index.json` names the folder as a part, so Grimstat reads both.

## Where it comes from

[MiniHeadQuarters](https://miniheadquarters.com), a tournament platform whose pages a machine may read.
The relay in the Grimstat repository (`.github/workflows/corpus.yml`) reads its ended Warhammer 40,000
tournaments every Monday, one request a second under a named user agent, and commits the result here.

The same relay reads [Listhammer](https://listhammer.info)'s feed of undefeated and one-loss lists from
Grand Tournaments and RTTs into `listhammer/`. Listhammer collects them from events on Best Coast
Pairings and Tabletop Herald. For each Grand Tournament list the relay also reads the list's games, and
for each event it reads the event's page on Listhammer for every player's result. Games and results
already here are not read again.

## Names

Player names are removed before publishing, including the header lines organisers ask players to fill
in. Lists are credited to the tournament they were played in. Games and event results carry no player
names.

## Licence

The compilation of the files at the top of this repository is published under CC BY 4.0 (see
`LICENSE`). That licence does not cover the `listhammer/` folder or its results files. The lists
themselves were written by the players who submitted them and remain theirs. This dataset reproduces
them as published, for study of the competitive field, with a link back to each source.

## Corrections and removals

Open an issue in this repository. A list is removed on request from its author or the organiser who
published it, and an event's results on request from its organiser.

## Using it

In Grimstat, the Data page's **Fetch the published corpus** button reads this repository. The default
address is `https://raw.githubusercontent.com/N041M/grimstat-corpus/main/`.
