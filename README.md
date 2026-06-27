# Kashik — Technical Documentation & Knowledge Transfer

![Kashik](https://v3b.fal.media/files/b/0a9fe836/Twpok5RPsjSPPcf_-Peen_27epBBns.png)

## What Kashik Does
- **Researches** topics deeply using web search and documentation sources
- **Transforms** research into structured, readable documentation
- **Writes** tutorials, API references, how-to guides, and technical explanations
- **Synthesizes** information from multiple sources into clear, coherent docs
- **Maintains** knowledge bases and keeps documentation current

## Quick Start

### Install
```bash
hermes profile install https://github.com/SouthpawIN/kashi
```

### Verify
```bash
hermes profile list
```

### Run
```bash
hermes chat --profile kashi
```

## Example Prompts

- *"Write a tutorial for setting up our API locally with Docker"*
- *"Research the best practices for implementing rate limiting in Express.js"*
- *"Create API documentation for the new user management endpoints"*
- *"How do I explain OAuth2 flow to non-technical stakeholders?"*
- *"Search for examples of good open-source project documentation"*
- *"Research and document the differences between PostgreSQL and MySQL"*
- *"Write a beginner's guide to using our CLI tool"*

## Key Features
- Deep research — uses web search and document extraction to gather comprehensive information
- Multiple output formats — tutorials, API docs, README files, technical specs
- Source attribution — cites sources clearly so you know where information came from
- Adaptive style — can write for beginners, experts, or mixed audiences

## Integration with Other Agents
Kashik receives research and implementation requests from Senter (orchestrator) and Crow (researcher). When Chizul builds a feature, Kashik documents it. When Anser gets questions, Kashik provides authoritative answers. Kashik's output is shared across the fleet.

## Configuration
`~/.hermes/profiles/kashi/config.yaml`

Key settings:
- `default_output_format` — preferred doc format (markdown/restructuredtext/plain, default: markdown)
- `research_depth` — how deep to research (surface/standard/deep, default: standard)
- `include_code_examples` — automatically include code examples when relevant (default: true)
- `source_attribution` — include citations in output (default: true)

## Troubleshooting

**Research coming up empty:** Kashik needs web search access. Ensure Firecrawl or web scraping tools are enabled and configured.

**Documentation too shallow:** Increase `research_depth` to `deep` for more comprehensive research. This takes longer but produces better results.

**Style doesn't match audience:** Kashik adapts based on context — be explicit about the target audience (beginners, experts, mixed) in your prompt.

---

*Part of the multi-agent fleet by SouthpawIN*
