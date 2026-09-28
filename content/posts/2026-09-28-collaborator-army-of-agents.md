# Collaborator: Army of Agents - LinkedIn + Facebook - 2026-09-28

## LinkedIn version

```
3,000 developers stopped juggling tabs.

They run Claude Code agents side by side instead.

I found Collaborator this week. It is free and open source.

Here is what actually works:

One window. One infinite canvas.

Double click anywhere and you get a terminal.

Spin up 3 or 4 agents at once.

One researches. One codes. One debugs. One documents.

You watch the work happen side by side.

No context switching. No lost terminals.

Drag any file onto the canvas and it sits next to your agents.

Notes, code, images. All live. All local.

No account needed. Your files stay on your machine.

It is early stage. The team ships for macOS, Windows and Linux.

Do this next if you use Claude Code daily:

Start with 2 agents, not 5. Give each one job. One builds, one checks.

If you could hand one task to a second agent tomorrow, which task would it be?
```

Why this hook and structure: number-led opener (3,000) per your voice hook patterns. Short sentences and list for scanning. Closes with one specific question, not generic engagement bait.

---

## Facebook version

```
Found something useful for anyone using Claude Code.

It is called Collaborator. Free and open source. 3,000 stars on GitHub.

Think of it as one big whiteboard for agents.

You open one window. You double click to add terminals.

Each terminal runs its own agent. Side by side.

So one can research while another writes code and another fixes bugs.

No tabs everywhere. No losing track.

Everything stays on your computer. No account to create.

It is still early, so expect rough edges. But the idea is simple and practical.

Windows users: grab the 0.6.2 setup file to start fast. Mac users can use the latest 0.8.4.

Link in comments if you want it.

Quick question: what is the first boring task you would give to an extra agent?
```

## Source and install notes

- Repo: https://github.com/collabs-inc/collab-public
- Stars: 3.0k, 280 forks, 11 contributors (checked 28 Sep 2026)
- Stack: Electron 40, React 19, Tailwind 4, xterm.js, Monaco, local JSON storage in ~/.collaborator/
- Windows fast path: Collaborator-Setup-0.6.2.exe from v0.6.2 release
  https://github.com/collabs-inc/collab-public/releases/tag/v0.6.2
- Latest 0.8.4 is Mac only. For latest on Windows, clone and build:
  git clone https://github.com/collabs-inc/collab-public.git
  cd collab-public/collab-electron
  bun install
  bun run dev (requires Node.js 22+ and Bun, PowerShell 7 recommended, WSL2 optional)
```

