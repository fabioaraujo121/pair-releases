# pair

Voice-driven pairing with a coding agent (Claude Code, Codex) in the terminal.
The agent explains what it is about to do out loud, points at code in Neovim,
asks questions and listens for the answer, while you watch edits land live
and can interrupt at any time. Everything runs locally.

This repository holds the releases. Install with Homebrew:

```sh
brew tap fabioaraujo121/tap
brew install --cask pair     # pulls tmux, neovim, sox, whisper.cpp
pair doctor --fix            # downloads the whisper model (1.6 GB)
pair doctor --mic            # records one second so macOS asks for microphone access
```

In a repository: `pair init` (or `pair init --agent codex`), then `pair`.
In the session: F5 to talk, F6 to interrupt, F7 to show the agent's pane.

Each release ships `pair_<version>_darwin_arm64.tar.gz`,
`pair_<version>_darwin_amd64.tar.gz` and `checksums.txt`.
