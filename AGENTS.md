# Working in this repository

Everything here is generated. The feed under `feed/` is written by the weekly run in
`kayzn-io/eval-papers` and pushed from its delivery job, so nothing in it is authored by
hand.

Do not edit the feed files. A hand-patched entry is overwritten by the next weekly run and
leaves this repository disagreeing with the archive that produced it, which is worse than
the error being fixed. Corrections belong upstream, in `scripts/build_public_feed.py` and
the run archive it reads; publishing again replaces what is here.

Two properties matter and are worth checking after any change upstream: every path under
`feed/` stays valid JSON that the website, both syndication feeds and the per-issue
archive can read, and no entry carries anything internal. Relevance scores, selection
rationales, held-back entries and house-view material must never appear here.

Readers who think an entry misreads a paper should open an issue with the entry `id`, as
`README.md` describes.
