# Puncho for Claude Code

The Puncho operator as a Claude Code plugin: an agent that writes ad concepts,
builds designs, launches approved ads paused and reads results on your
[Puncho](https://puncho.app) board. You decide; it does the work, on your own
Claude plan.

## Install

1. Make a token at `https://app.puncho.app/settings/tokens`.
2. In a terminal:

   ```bash
   claude plugin install puncho --marketplace sislelabs/puncho-plugin --config token=<your token>
   ```

3. Start it and say hello:

   ```bash
   claude --agent puncho
   ```

To change the token later, run `/plugin configure puncho@puncho` inside Claude
Code.

## What it installs

- **The agent** (`puncho`). It reads how the work is done from your Puncho
  itself, so it is up to date without reinstalling. It cannot edit files or run
  commands on your machine.
- **The connection** to your board, with your token kept in your system's
  credential store.
- **A prompt before anything paid.** Whatever mode Claude Code is in, you are
  asked before a paid image, a launch, a budget change or a change to the
  brand's colours, fonts and logo.

Approving an ad and switching one on are never the agent's. You do both on the
board.
