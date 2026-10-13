Beat the Flood — GitHub Pages feed mirror
==========================================

This folder mirrors the layout served from
https://voilibaar.github.io/beat-the-flood/ (the shell's failover feed
host; Google Drive stays the primary feed). Publish by copying this tree
to the repo root of https://github.com/Voilibaar/beat-the-flood so that:

  feed/stable.json          -> https://voilibaar.github.io/beat-the-flood/feed/stable.json
  feed/unstable.json        -> https://voilibaar.github.io/beat-the-flood/feed/unstable.json
  payload/game-<ver>.html   -> https://voilibaar.github.io/beat-the-flood/payload/game-<ver>.html

Manifest schema (append-only): { version, gameUrl, sha256?, minShell?,
channel? }. gameUrl may be relative — it resolves against the manifest
URL, which is why stable.json points at "../payload/game-0.14.1.html".

feed/stable.json + payload/game-0.14.1.html are included here (the live
0.14.1 payload, sha256-verified copy). feed/unstable.json and
payload/game-0.14.3.html are added by the staging step once the 0.14.3
candidate exists — the unstable feed file ID baked into the shell points
at the Drive copy; this GitHub copy is the failover for the same channel.
