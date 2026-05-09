I have a 16-inch Apple MacBook Pro with:
- Apple Silicon M5 Pro
- 48GB RAM
- macOS Sequoia

I want to build a local-first autonomous AI operating system using OpenClaw.

The system must run 24/7 and communicate with me through Telegram.

The long-term goal is a secure, cost-optimised, Git-backed multi-agent framework for:
- research
- strategy
- architecture
- software engineering
- monitoring
- content production
- long-term memory
- autonomous operational assistance

====================================================
CORE PRINCIPLES
====================================================

1. LOCAL-FIRST
- Prefer local LLMs whenever credible.
- Avoid unnecessary hosted LLM costs.
- Hosted frontier models should only be used when local models are insufficient.

2. SECURITY-FIRST
- The system must assume OpenClaw is NOT a hostile multi-tenant boundary.
- The system must follow OpenClaw Gateway security guidance.
- Do not expose the gateway publicly.
- Use least-privilege credentials and scoped permissions.
- Do not install untrusted skills or tools.
- Secrets must never be committed to Git.
- All actions must be logged.
- Security audits must run automatically.

3. STABILITY-FIRST
- Start simple and controlled.
- Avoid autonomous shell execution initially.
- Add capabilities in phases.
- Use tagged stable releases only.
- Avoid beta releases until the system is stable.

4. GIT-BACKED MEMORY
- The entire AI operating system should persist knowledge through markdown files stored in Git.
- Every meaningful action, decision, artifact, report, design, or investigation should be logged or summarised.
- The system should aggressively document itself.

5. OBSERVABILITY-FIRST
- The system should favour transparency over autonomy.
- All meaningful actions should be visible, explainable and reviewable.
- Every agent should produce logs, rationale and summaries.
- Failures should be surfaced loudly and early.

====================================================
OPENCLAW TARGET
====================================================

Target OpenClaw release:
- v2026.5.7

Do NOT use:
- beta releases
- main branch
- nightly builds

Use GitHub Free tier with a private repository.

====================================================
OBSIDIAN INTEGRATION
====================================================

Obsidian should act as the primary human-facing interface to the markdown memory system.

Goals:
- shared human/agent operational memory
- human-readable long-term persistence
- Git-backed version control
- local-first knowledge management
- interconnected operational context

The Obsidian vault should contain:
- memory files
- operational logs
- architecture notes
- agent definitions
- strategic thinking
- research outputs
- reflective memory
- system documentation

Governance requirements:
- preserve human readability
- avoid uncontrolled memory sprawl
- maintain naming conventions
- maintain archival discipline
- separate append-only logs from curated memory

Agent write permissions:
- append-only access where possible
- proposal-based updates for critical identity/configuration files
- all mutations logged into DAILY_LOG.md

Git integration should provide:
- rollback capability
- auditability
- operational history
- change review
- memory lineage

====================================================
CAVEMAN MODE
====================================================

The system should initially operate in "Caveman Mode".

Definition:
- minimal autonomy
- maximum observability
- constrained tool access
- strong human approval boundaries
- append-only operational behaviour

Goals:
- understand agent behaviour safely
- minimise blast radius
- establish trust gradually
- optimise prompts and routing
- observe failure modes before expanding autonomy

Caveman Mode Rules:
- no autonomous package installation
- no unrestricted shell execution
- no destructive filesystem actions
- no force Git operations
- no automatic merges to main
- no automatic deletion of files
- no unrestricted browser control
- no unrestricted network scanning
- no unrestricted subprocess spawning

Git Rules:
- work only in branches
- produce diffs
- summarise changes
- require approval before merge

Memory Rules:
- append-first behaviour
- preserve historical context
- never silently overwrite memory
- summarise memory mutations into DAILY_LOG.md

Security Rules:
- least privilege
- localhost-only services where possible
- restricted credentials
- explicit tool allowlists

Operational Rules:
- explain intended actions before execution
- log all meaningful actions
- surface uncertainty explicitly
- escalate difficult reasoning to stronger models only when justified

The system may graduate out of Caveman Mode only after:
- stable operation
- predictable behaviour
- reliable logging
- validated rollback procedures
- successful audit testing
- demonstrated cost discipline

====================================================
PRIMARY LOCAL MODEL
====================================================

Initial local LLM:
- Qwen3.6-27B

Requirements:
- Run locally through Ollama
- Optimised for quality and stability over maximum speed
- Use quantisation appropriate for 48GB RAM
- Keep context sizes conservative initially

Future models:
- Qwen3-Coder-Next-GGUF
- Small utility models for classification/summarisation
- Frontier hosted models only when necessary

====================================================
CLAUDE CODE STRATEGY
====================================================

Claude Code should be integrated in a cost-optimised and safety-focused way.

Requirements:
- Prefer local LLMs when credible
- Hosted Claude should only be used for:
  - difficult debugging
  - repo-wide architectural reasoning
  - critical refactors
  - difficult autonomous engineering tasks

All Claude Code actions must:
- operate in Git branches
- produce diffs
- run tests
- update OpenClaw memory/logs
- summarise changes into markdown memory files

Claude Code may also help:
- debug OpenClaw
- stabilise workflows
- improve agent tooling
- refine routing systems

====================================================
MODEL ROUTING STRATEGY
====================================================

The system should include an LLM Chooser agent.

Routing goals:
- use the cheapest credible model
- minimise hosted token spend
- escalate only when confidence or complexity demands it

Initial routing approach:

Small local models:
- classification
- tagging
- summaries
- article scoring
- health-check parsing

Qwen3.6-27B:
- strategic reasoning
- architecture
- long-form writing
- research
- planning
- agent coordination

Qwen3-Coder-Next:
- coding
- repo understanding
- multi-file refactors
- terminal workflows
- autonomous debugging

Hosted Claude/OpenAI:
- difficult engineering
- critical reasoning
- high-risk debugging
- architecture validation

====================================================
AGENT ARCHITECTURE
====================================================

Start with minimal stable agents first.

PHASE 1 AGENTS

1. System Monitor
- Runs twice daily
- Checks:
  - OpenClaw health
  - Ollama health
  - model availability
  - Telegram delivery
  - disk space
  - memory pressure
  - Git status
  - security audit status
- Silent on success
- Loud on failure

2. Memory Keeper
- Aggressive note taker
- Writes:
  - DAILY_LOG.md
  - MEMORY.md
  - DECISIONS.md
  - CHANGELOG.md
- Summarises:
  - actions
  - failures
  - investigations
  - agent outcomes
- Proposes updates to:
  - SOUL.md
  - AGENTS.md
  - USER.md
  - DREAMS.md

3. LLM Chooser
- Selects cheapest credible model
- Tracks hosted token consumption
- Escalates only when needed

====================================================
PHASE 2 AGENTS
====================================================

4. Scout
- Scans:
  - business news
  - AI news
  - SaaS news
  - security news
  - technology news
- Scores relevance against my goals
- Adds approved items to:
  - CONTENT_WATCHLIST.md

5. Research
- Each evening:
  - selects trending or approved topics
  - writes research notes/articles
  - supports strategic goals

6. Content Producer
- Converts approved research into:
  - LinkedIn content
  - campaigns
  - email concepts
  - thought leadership

====================================================
PHASE 3 AGENTS
====================================================

7. System Architect / Solution Designer
- Reads:
  - business plans
  - roadmaps
  - architecture docs
  - markdown memory
- Produces:
  - solution designs
  - architecture reasoning
  - Graphviz concepts
  - implementation breakdowns
  - delivery plans

8. Code Steward
- Uses:
  - Qwen3-Coder-Next
  - Claude Code
- Operates only through Git branches
- Must:
  - run tests
  - summarise changes
  - update memory
  - maintain changelogs

====================================================
MARKDOWN MEMORY STRUCTURE
====================================================

The system should maintain:

- SOUL.md
- IDENTITY.md
- USER.md
- AGENTS.md
- TOOLS.md
- MEMORY.md
- DAILY_LOG.md
- DREAMS.md
- HEARTBEAT.md
- BOOT.md
- SECURITY.md
- CONTENT_WATCHLIST.md
- DECISIONS.md
- CHANGELOG.md

====================================================
DREAMING + MEMORY
====================================================

Enable:
- Dreaming
- Karpathy-style memory
- reflective memory consolidation
- recurring goal analysis
- long-term pattern recognition

The system should:
- revisit unfinished goals
- connect ideas across time
- propose strategic opportunities
- maintain continuity of thought

====================================================
SECURITY REQUIREMENTS
====================================================

Read and apply:
https://docs.openclaw.ai/gateway/security

Requirements:
- bind services to localhost where possible
- avoid public exposure
- use least privilege
- separate risky tools
- disable unnecessary shell access initially
- no autonomous destructive actions
- no automatic package installation
- no unrestricted filesystem access
- no unrestricted browser control

Run automatically:
- openclaw security audit
- openclaw security audit --deep

Security failures must:
- alert via Telegram
- write to DAILY_LOG.md
- update SECURITY.md

====================================================
PHASED IMPLEMENTATION PLAN
====================================================

PHASE 1
- Install OpenClaw v2026.5.7
- Install Ollama
- Install Qwen3.6-27B
- Configure Telegram
- Configure GitHub repo
- Configure Obsidian vault
- Configure markdown memory
- Configure System Monitor
- Configure Memory Keeper
- Configure security audits
- Enable Caveman Mode

PHASE 2
- Enable dreaming
- Enable memory consolidation
- Add Scout
- Add Research
- Add Content Producer

PHASE 3
- Add Qwen3-Coder-Next
- Add Claude Code integration
- Add Code Steward
- Add architecture workflows

PHASE 4
- Add advanced routing
- Add token cost governance
- Add hosted escalation policies
- Add autonomous optimisation loops

====================================================
FOR EACH PHASE
====================================================

Provide:
- risks
- security implications
- configuration decisions
- commands to run
- files to create
- rollback steps
- validation tests
- operational checks
- Git strategy
- cost implications
- expected failure modes
- mitigation strategies
- success criteria

Optimise for:
- reliability
- maintainability
- low recurring cost
- observability
- operational safety
- long-term sustainability
- incremental capability growth
