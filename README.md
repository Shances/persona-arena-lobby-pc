# Bar do Igor – Lobby client

Community lobby client for **Persona 4 Arena Ultimax** (PC). It adds a chat/lobby ("Bar do Igor") with matchmaking on top of the game's own online play.

**Current test build: 0.2.31** (Windows and Linux/Proton). This is a test release for the Persona Arena Brasil community. Expect rough edges.

## Download

Get the files from the [Releases](../../releases/latest) page:

- `BarDoIgor-windows.zip`
- `BarDoIgor-linux.tar.gz`

SHA-256:

```
e225a448acb4bbb2588b5c1c7709646d9931e9f5f1e364a77fca7f7c3f9c74b6  BarDoIgor-windows.zip
7c8089fb90fd30d923ad83f74bf0a63bb0150640e00038099762ff88a2c3f5ca  BarDoIgor-linux.tar.gz
```

## Install

1. Extract the archive and copy everything inside `pasta_do_jogo/` next to `P4U2.exe` (Steam > right click > Manage > Browse local files).
2. **Windows:** launch the game from Steam as usual.
   **Linux:** `chmod +x p4au-lobby juntar_logs.sh`, then set the Steam launch option `WINEDLLOVERRIDES="version=n,b" %command%`.
3. In game press **F10 > Servers**, enter the server address and port the organizer gives you, then **Connect**. When it turns green, the **LOBBY** button shows up under Network.

To play without it, delete `p4au-lobby(.exe)`, `version.dll` and `lobby_config.dll` from the game folder. Your antivirus may flag it because the client reads the game's memory; allow the game folder.

## Known issue: "Failed Connect"

After many rematches in a row, starting a new fight can fail with **Failed Connect**. We have not proven the cause yet, so treat what follows as a workaround, not a fix.

- **Do not mash the confirm/READY button.** Mashing right after a match makes it worse. Press it once and wait.
- If it fails, wait a few seconds and try again **once**.
- If it fails again, **swap who hosts**: the other player becomes P1 and starts the match.
- Still failing? Close and reopen the game and the client, then send us the logs.

## Sending logs

After closing the game and the client, run `Juntar_logs.bat` (Windows) or `bash ./juntar_logs.sh` (Linux) in the game folder and send the generated `logs_bar_do_igor_<date>.zip` to the organizer. `config.toml` and `avatar_escolhido.json` are left out of the package.

## Status

No source code is published here yet; this repository only distributes test builds. Not affiliated with Atlus or Arc System Works.
