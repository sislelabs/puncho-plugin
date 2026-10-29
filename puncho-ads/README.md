# Puncho

Run your Meta ads loop on your [Puncho](https://puncho.app) board from a
conversation with Claude: collect references, write ad concepts in your brand's
own voice, build the designs you asked for, and read what is working. You
decide; Claude does the work, on your own Claude plan.

It works in chats on claude.ai, the Claude desktop app and the mobile apps, in
Cowork, and in Claude Code.

## Install

1. In claude.ai or the desktop app, open **Customize**, then **Plugins**.
   Choose **Add**, then **Add marketplace**, and enter `sislelabs/puncho-plugin`.
2. Add **Puncho** (`puncho-ads`).
3. Open the plugin's **Connectors** tab and connect Puncho. Sign in with your
   Puncho account, pick the workspace if it asks, and press **Connect**.

You need a Puncho account. On Team and Enterprise plans, an Owner adds the
connector for the organization first, then each member connects.

In Claude Code, a plugin added on your claude.ai account arrives by itself at
the next session. To install it there directly:

```
/plugin install puncho-ads --marketplace sislelabs/puncho-plugin
```

Claude Code then asks you to sign in to Puncho the first time a tool is used.
For launches and budgets from a terminal, install the `puncho` plugin with a
token instead, as https://app.puncho.app/settings/tokens shows.

## Use it

Start a chat and say "Let's work on my ads in Puncho". Claude reads how Puncho's
own operator works from your Puncho, looks at your brand, tells you what it has
and lacks, and suggests what to do first. Ask it to write concepts, design what
is waiting, or tell you what is working.

## What it can and cannot do

- It can read your projects, references, concepts, designs and results; add
  references, voice samples, briefs and concepts; and edit concepts and designs.
- It can generate the parts of a design you pressed **Design this** for, paid
  from the budget that press gave the design and from your plan's image credits.
  Puncho refuses anything past either.
- It cannot approve an ad, switch one on, launch a campaign, change a budget,
  render a whole ad, or set your brand's colours, fonts and logo. You do those
  on the board. Everything Puncho launches starts paused.

## Data

The plugin holds no code and no credentials. It adds one skill, which tells
Claude how to work in Puncho, and one connector to `https://app.puncho.app/api/mcp`.
You sign in to the connector with OAuth; Claude never sees your password.
Through it, Claude reads and writes your Puncho workspace only, as you, and
sends what you work on with it (brand material, ad copy, images) to Puncho.
Puncho's privacy policy is at https://puncho.app/privacy. Disconnect it any time
from the plugin's Connectors tab or from **Connected apps** on
`https://app.puncho.app/settings/tokens`.

## Support

Write to support@puncho.app.
