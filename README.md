## Hi, I'm Dup (Jacob Caza)

Technical support engineer in Windsor, Ontario, with eight years at 1Password and Applied Systems. Building with AI developer tools: Claude Code, agent SDKs, MCP servers.

Support is where I learned the habit I still work by. Go watch the thing break for an actual person, then fix that.

### What I'm building

<details>
<summary><b><a href="https://chordstamp.app">chordstamp.app</a></b> (private repo, live site): chord labels and diagrams stamped onto guitar tabs</summary>

Drop in a Guitar Pro or MusicXML file and get it back with [a chord stamped above every bar](https://chordstamp.app/app.html), a fingering diagram for each one, and a strummed backing track that follows the changes. The chord-detection engine reads every note in a bar and works out the chord in the song's key, so it labels the bars the tab's author left blank. Indexes [a whole tab library](https://chordstamp.app/library.html) in the browser. A [Learn section](https://chordstamp.app/learn.html?key=C) for new players has [interactive widgets](https://chordstamp.app/learn.html?key=C&view=widgets) (CAGED, Circle of Fifths, ear training) that stay in sync: set the key in one and every widget follows.\
JavaScript, Python / FastAPI, SQL, Oracle Cloud, Cloudflare.

</details>

<details>
<summary><b><a href="https://github.com/duplonicus/gmail-triage">Gmail triage service</a></b>: labels new mail within seconds, unattended</summary>

Runs 24/7 under systemd on a home server (Ubuntu). Gmail pushes new mail through Google Cloud Pub/Sub, Claude Haiku classifies it, the service applies the label before I ever open the inbox. Picked the smallest model that handles the job to keep token costs down.

</details>

<details>
<summary><b>D&amp;D campaign pipeline</b> (private): session recordings to written recaps, unattended</summary>

Our D&D group plays online, and the campaign notes write themselves. A multi-track Discord recording bot exports each player's audio as FLAC; Whisper transcribes each track locally into one time-ordered, speaker-labelled transcript; Claude writes an in-character session recap from it, with guardrails against invented facts and spoilers; and the site rebuilds from markdown and deploys to Cloudflare Pages. It runs unattended as a systemd service, and the audio never leaves my machine.\
Python, Whisper, Claude Code, Cloudflare Pages, systemd.

</details>

<details>
<summary><b>Trading research pipeline and operations dashboard</b> (private): a multi-bot dashboard and a strategy research pipeline</summary>

A ~20-page Django dashboard using the freqtrade REST API that monitors several bots at once, with health checks, auto-restarts and a read-only Claude Agent SDK assistant that talks through the data on any page. The research pipeline behind it runs hyperparameter optimization with walk-forward and out-of-sample gates, plus a causality auditor that rejects any signal peeking at future prices.

</details>

<details>
<summary><b><a href="https://github.com/duplonicus/agent-skills">agent-skills</a></b>: skills for AI agents, each tested with and without the skill</summary>

A set of agent skills in the open SKILL.md format, which both Claude Code and OpenAI's Codex support. Three of them teach by making the person do the work: learn-web walks them through a product or console in their own browser, learn-cli drills command-line tools they type themselves, and learn-repo gets them up to speed on an unfamiliar codebase. Each one sets one small task at a time, gives hints before answers, waits while they try it, and ends with a quiz from memory.

</details>

<details>
<summary><b><a href="https://github.com/duplonicus/claude-messenger">claude-messenger</a></b>: a local MCP server for WhatsApp and Discord</summary>

A local MCP server that lets the Claude app send messages for me: WhatsApp from my own number, Discord DMs from my bot. It asks before every send by default and never guesses between two contacts with the same name. Small on purpose, and instrumented like something bigger: structured logs, OpenTelemetry traces and metrics into Jaeger and Prometheus, and a doctor script that connects the way a client does.\
Python, MCP, OpenTelemetry. 142 automated tests.

</details>

<details>
<summary><b>Background</b></summary>

Eight years in technical support. At 1Password I handled escalations for enterprise customers and IT admins, reproducing bugs across Windows, macOS, iOS, Android and browser extensions, and digging through Datadog and Kibana at the API layer whenever a ticket gave me a reason to. Before that, nearly seven years at Applied Systems supporting insurance brokers on comparative quoting software, where I wrote a Python EDI service monitor that eliminated our biggest single call driver.

</details>

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/jacob-caza999) · [chordstamp.app](https://chordstamp.app)

Avatar: generated locally in 2023 with Stable Diffusion (GhostMix, a psychedelic LoRA and a negative embedding).
