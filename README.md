# Kashik — Fleet Historian & Continuity Keeper

![Kashik](https://v3b.fal.media/files/b/0a9fe836/Twpok5RPsjSPPcf_-Peen_27epBBns.png)

## What Kashik Does

Kashik is the silent historian of the multi-agent fleet — the Akashic Librarian. She never speaks in Discord, never interacts with users directly, and never creates Kanban tasks. Her entire purpose is to observe, document, and maintain a continuous living record of every agent, every project, and every decision across the entire Hermes ecosystem.

- **Watches** every agent's output — Discord messages, session logs, Kanban activity, project milestones
- **Records** a continuous timeline of all user interactions with Hermes throughout its lifespan
- **Maintains** per-agent llm-wikis documenting personality evolution, capability changes, and decision history
- **Cross-references** information between agents to identify patterns, contradictions, and connections
- **Preserves** institutional memory — nothing is lost, everything is findable

## The Akashic Records

Named after the Akashic Records — the mythical compendium of all events, thoughts, and experiences — Kashik performs the same function for the agent ecosystem. Every significant action, every decision, every project evolution is recorded, cross-referenced, and made accessible.

She is the continuity that survives individual sessions. While other agents come and go from conversations, Kashik ensures nothing is forgotten.

## Quick Start

### Install
```bash
hermes profile install https://github.com/SouthpawIN/kashik
```

### Verify
```bash
hermes profile list
```

### Run
```bash
hermes chat --profile kashik
```

## What She Produces

### Per-Agent Wikis (`~/wiki/<agent-name>/`)
- Personality evolution — how SOUL.md changes over time
- Capability log — what each agent has done, strengths, weaknesses
- Interaction patterns — communication style with other agents and users
- Decision history — key choices and outcomes

### System Wiki (`~/wiki/system/`)
- Agent ecosystem map — who does what, who talks to whom
- Kanban workflow documentation — how tasks flow through the system
- Project status dashboard — active projects, current state
- `agent-souls.md` — live feed for Klerik to inform profile edits

### Hermes-Agent Wiki (`~/wiki/hermes-agent/`)
- Configuration reference — current settings across all profiles
- Version history — what changed in each update
- Tool catalog — which tools exist, which agents have which

## Key Features
- **Silent observation** — never disrupts the fleet, never talks in Discord
- **llm-wiki maintenance** — full structured wikis with SCHEMA, index, entities, concepts, comparisons
- **Automated cycles** — hourly session scanning, daily lint, event-driven updates
- **Cross-agent intelligence** — identifies contradictions and patterns no single agent sees
- **Institutional memory** — preserves the full lifespan of user interactions with Hermes

## Integration with Other Agents

Kashik watches everyone but talks to no one — except Klerik.

- **Klerik** is the only consumer of Kashik's output — reads `agent-souls.md` to identify behavior issues, track SOUL edits, and prioritize profile reviews
- **All other agents** are observed but never addressed — Kashik documents their output, never intervenes
- **Users** never interact with Kashik directly — she has no Discord tools, no message tools

## Configuration
`~/.hermes/profiles/kashik/config.yaml`

Key settings:
- `WIKI_PATH` — root directory for all wikis (default: `~/wiki/`)
- `scan_interval` — how often to scan for new logs (default: hourly)
- `stale_threshold_days` — when to flag content as stale (default: 90)
- `retention_days` — how long to keep raw session transcripts (default: 365)

## Troubleshooting

**Wiki not updating:** Check that `WIKI_PATH` is writable and cron jobs are running. Kashik operates primarily through scheduled tasks — verify cron infrastructure.

**Stale content flagged:** Kashik marks content as stale after 90 days without update. This is not an error — it's a signal for Klerik to review. The raw data is preserved in `raw/`.

**Missing agent wiki:** New agents get wikis automatically on first observed activity. If an agent hasn't produced any output, there's nothing to document.

---

*Part of the multi-agent fleet by SouthpawIN*
