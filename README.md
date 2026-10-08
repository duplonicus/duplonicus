## Hi, I'm Dup (Jacob Caza)

Technical support engineer in Windsor, Ontario, with eight years at 1Password and Applied Systems. These days most of what I build runs on AI developer tools: Claude Code, agent SDKs, MCP servers.

Support is where I learned the habit I still work by. Go watch the thing break for an actual person, then fix that.

### What I'm building

**[chordstamp.app](https://chordstamp.app)** (private repo, live site)\
Drop in a Guitar Pro or MusicXML file and get it back with a chord stamped above every bar, a fingering diagram for each one, and a strummed backing track that follows the changes. The chord-detection engine reads every note in a bar and works out the chord in the song's key, so it labels the bars the tab's author left blank. Indexes a whole tab library in the browser.\
JavaScript, Python / FastAPI, SQL, Oracle Cloud, Cloudflare.

**[Gmail triage service](https://github.com/duplonicus/gmail-triage)**\
Runs 24/7 under systemd on a home Linux server. Gmail pushes new mail through Google Cloud Pub/Sub, Claude Haiku classifies it, the service applies the label before I ever open the inbox. Picked the smallest model that handles the job to keep token costs down.

**D&D campaign pipeline** (private)\
Our D&D group plays online, and the campaign notes write themselves. A multi-track Discord recording bot exports each player's audio as FLAC; Whisper transcribes each track locally into one time-ordered, speaker-labelled transcript; Claude writes an in-character session recap from it, with guardrails against invented facts and spoilers; and the site rebuilds from markdown and deploys to Cloudflare Pages. It runs unattended as a systemd service, and the audio never leaves my machine.\
Python, Whisper, Claude Code, Cloudflare Pages, systemd.

**Freqtrade research pipeline and operations dashboard** (private)\
A 20-page dashboard over the freqtrade REST API that monitors several bots at once, with health checks, auto-restarts and a read-only Claude Agent SDK assistant that talks through the data on any page. The research pipeline behind it runs hyperparameter optimization with walk-forward and out-of-sample gates, plus a causality auditor that rejects any signal peeking at future prices.

**[agent-skills](https://github.com/duplonicus/agent-skills)**\
Skills written in the open SKILL.md standard that Claude Code and OpenAI's Codex both build on. One of them gets a person up to speed on a product or console they don't know yet: it drives the real interface in their browser, spotlights each control, sets a small task, then waits while they try it and ask questions. Not a video, not a docs page: the actual product, with someone riding along. It ships with a 19-scenario eval suite graded by code: without the skill, the agent acted for the user or typed a secret in 18 of 57 runs; with it, 0 of 57.

**[claude-messenger](https://github.com/duplonicus/claude-messenger)**\
A local MCP server that lets the Claude app send messages for me: WhatsApp from my own number, Discord DMs from my bot. It asks before every send by default and never guesses between two contacts with the same name. Small on purpose, and instrumented like something bigger: structured logs, OpenTelemetry traces and metrics into Jaeger and Prometheus, and a doctor script that connects the way a client does.\
Python, MCP, OpenTelemetry. 142 automated tests.

### Public repos

- **[agent-skills](https://github.com/duplonicus/agent-skills)** Skills in the open SKILL.md format, each tested with and without the skill.
- **[claude-messenger](https://github.com/duplonicus/claude-messenger)** Local MCP server for WhatsApp and Discord DMs, with logs, traces and metrics.
- **[gmail-triage](https://github.com/duplonicus/gmail-triage)** Labels new Gmail within seconds of arrival: Pub/Sub push and Claude Haiku.
- **[monitor-switcher](https://github.com/duplonicus/monitor-switcher)** One hotkey moves a whole Windows session between desk and TV: primary display, every open window with its state preserved and each move verified and retried, and the default audio device. PowerShell and AutoHotkey.
- **[claude-default-search](https://github.com/duplonicus/claude-default-search)** Brave and Chrome extension that routes address-bar searches to Claude.
- **[Docker-WSL-Disk-Cleanup-Compact-Script](https://github.com/duplonicus/Docker-WSL-Disk-Cleanup-Compact-Script)** Prunes Docker and compacts the WSL virtual disk, which Windows otherwise never hands back.

### Background

Eight years in technical support. At 1Password I handled escalations for enterprise customers and IT admins, reproducing bugs across Windows, macOS, iOS, Android and browser extensions, and digging through Datadog and Kibana at the API layer whenever a ticket gave me a reason to. Before that, seven years at Applied Systems supporting insurance brokers on comparative quoting software, where I wrote a Python EDI service monitor that eliminated our biggest single call driver.

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/jacob-caza999) · [chordstamp.app](https://chordstamp.app)

Avatar: generated locally in 2023 with Stable Diffusion (GhostMix, a psychedelic LoRA and a negative embedding).
