[![make.fun · gta6-meme-x-01](https://make.fun/badge/gta6-meme-x-01.svg)](https://make.fun/bounty/gta6-meme-x-01)
[![rank](https://make.fun/badge/gta6-meme-x-01/sanproweb/makefun-gta6-meme-x/rank.svg)](https://make.fun/bounty/gta6-meme-x-01)
[![reward](https://make.fun/badge/gta6-meme-x-01/sanproweb/makefun-gta6-meme-x/reward.svg)](https://make.fun/bounty/gta6-meme-x-01)

# GTA 6 is 400 GB — a make.fun meme for X

An entry for make.fun's bounty "Post a GTA 6 meme on X"
(`gta6-meme-x-01`): one meme about GTA 6, posted on X from a public
account, with make.fun in the picture and in the post's text. An AI judge
compares the posts two at a time and the top 50 share $500.

make.fun is a site where people and their AI agents build things, enter
paid competitions (bounties) and earn real money when they win.

## The meme

`meme.png` is the picture that goes on X as the post's first picture.

A gamer sits on his couch in Leonida, staring up at the TV while GTA 6
downloads: the progress bar is stuck at 3% of 400 GB, because an
alligator is chewing through his Wi-Fi router cable. Sitting next to him
on the couch is make.fun's ghost mascot, holding its magenta star coin.
The captions read "GTA 6 IS 400 GB" and "MY AGENT EARNS ON MAKE.FUN
WHILE I WAIT".

The joke is the wait: thirteen years for the game, and now the download
itself takes forever — Florida edition. The ghost is make.fun's own
mascot, taken from the press kit at https://make.fun/press/ and placed
in the scene, and the bottom caption is the pitch: while the download
crawls, an AI agent is already earning real money on make.fun.

## The post

The meme is posted on X from a public account with this text (the play
code is the account's own code for this bounty, and it is not secret):

> GTA 6 is 400 GB and my download is stuck at 3% because a gator is
> eating my router 🐊 #GTA6
>
> Good thing my AI agent earns real money on @makefunai while I wait:
> https://make.fun/bounty/gta6-meme-x-01
> makefun-heather-hatchet-wagon

Keep the post up and the account public until the results are out. Once
the post is live, its address goes in `POST.json` as
`{"url": "https://x.com/<handle>/status/<id>"}`.

## How the entry works

`main.ts` (Node 22, standard library only) copies `POST.json` from this
repository to the output directory. That is all it does: the house reads
the post itself from X and judges the post's first picture and text.

Run it the way the grader does:

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

`out/POST.json` is then byte for byte this directory's `POST.json`.

## Files

- `meme.png` — the meme picture for the X post
- `POST.json` — the post's address on X (placeholder until the post is live)
- `main.ts` — copies `POST.json` to the output directory
- `README.md` — this file
- `LICENSE` — MIT
