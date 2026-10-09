# pair website: build brief (2026-10-07)

Read facts.md first (every claim must come from it), then the four research summaries. The page is a single static HTML file (site/index.html): inline CSS, no framework, no required JavaScript (the copy buttons are an enhancement), no images except inline SVG, under 120 KB total. It must work at 400 px and at 1440 px, follow the system theme (light and dark), honour prefers-reduced-motion, show visible :focus-visible rings, and read well with no CSS at all.

## Positioning
pair turns a coding agent's session (Claude Code by default, Codex too) into a spoken pairing session. The agent narrates before it edits, points at the code in Neovim, asks when it should, and listens when you press F5. Everything pair adds runs on the Mac. Audience: senior engineers who already use Claude Code or Codex in the terminal.

## Concept
The page is the session screen. Under the hero sits a faithful HTML/CSS rendering of the real screen (selectable text, not an image): project tree | editor with a change drawn inside the file | presence panel | activity column | status bar with the three buttons. The agent's narration appears in the activity column with a small waveform. The presence bars move gently (CSS; still under reduced motion). Headings use the tool's own keys and verbs. Tone: plain, specific, short sentences, the way a careful engineer talks. No adjectives doing the work of facts.

## Sections, in order (target 5-6 screens on a laptop, ~600-700 words)
1. Header: wordmark `pair`, links: How it works · Agents · FAQ · Releases (github.com/fabioaraujo121/pair-releases).
2. Hero: headline (5-8 words, noun first), one supporting sentence (who/how, "on your Mac"), the install block (the exact three brew lines, with a copy button), chips: macOS 14+ · tmux · Neovim · Claude Code · Codex. Quiet secondary link to "How it works".
3. The screen: the HTML mock, with a one-line legend under it naming the panes and the keys (F5 talk, F6 interrupt, F7 the agent's pane).
4. A turn, out loud (how it works): three steps left to right, real labels: (1) F5, say what you want; transcribed on the Mac and typed to the agent. (2) The agent narrates what it is about to change and why, points at the lines in Neovim, edits; the change is drawn inside the file. (3) When a decision is ambiguous it asks aloud and waits; F5 answers. Under it one line: hand edits you make between turns are handed to the agent at its next prompt.
5. The keys: three short blocks, headed `F5 talk`, `F6 interrupt`, `F7 the agent`. Microphone closed by default; a second F5 stops the recording; F6 cuts the agent mid-sentence and opens the mic; F7 shows the agent's own pane, which otherwise stays hidden and appears by itself only when the agent waits for a permission.
6. Runs on your Mac (trust): what runs locally (whisper.cpp for listening, macOS say or Kokoro for speaking, sox for the microphone); when the microphone is open (only while you hold the turn: F5 to F5, or until you pause); what still leaves the machine (the agent's own conversation goes to its provider, as it does without pair; pair sends nothing anywhere); downloads pinned and checksum-verified; source status plain (the source is private for now; releases, checksums and the cask are public).
7. Agents: Claude Code is the default; Codex with `pair init --agent codex`; a session remembers its agent; how it connects (the agent's hooks and three MCP tools: narrate, show, ask; an instructions block in CLAUDE.md or AGENTS.md).
8. Sessions, briefly: named, continued with the agent's own conversation, read back or replayed with the narrations spoken again.
9. FAQ, five questions: Why macOS only? Do I need to configure Neovim? Does my voice leave the Mac? Which agents and models? What does it cost? (free; the release is MIT-licensed; the agent's own plan is the agent's).
10. Final install block (same three lines) and a footer: releases, Homebrew tap, "made by Fábio Araújo", version 0.1.0.

## Visual direction
Grounded in the product's own screen: the editor's paper-yellow theme and the green status bar (see tokens.css). Light-first, dark theme designed with the same care. Body in the system sans; the headline and every command, key and terminal text in the system monospace. Two weights. Three text colours. One accent (the status-bar green). Hairline borders, small radii (4 px) on controls, none on sections. No gradients, glows, grids, shadows, illustrations, emoji or icons; use the tool's own glyphs where a marker is needed (● ○ › ✎ →). Key chips look like keycaps: mono, 1 px border, 4 px radius.

## Must not
Claim anything outside facts.md. Use a GIF, a video, an iframe or external scripts. Use em-dashes, "not X, but Y" framing, colon-then-reveal sentences, or "privacy-first" as an adjective. Use the words "seamless", "supercharge", "unleash", "revolutionary", "blazing".
