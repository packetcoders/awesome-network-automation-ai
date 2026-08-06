# Awesome Network Automation AI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome resources for applying Artificial Intelligence (AI), Large Language Models (LLMs), and Machine Learning (ML) to network automation.

The intersection of AI and network automation is moving fast — from LLM-powered assistants that generate device configs, to agentic workflows that troubleshoot networks, to ML models that predict outages. This list collects the best tools, frameworks, articles, talks, and learning resources in one place.

Maintained by [Packet Coders](https://www.packetcoders.io).

## Contents

- [Tools & Frameworks](#tools--frameworks)
- [LLM & Agent Tooling](#llm--agent-tooling)
- [Libraries & SDKs](#libraries--sdks)
- [Platforms & Products](#platforms--products)
- [Model Context Protocol (MCP)](#model-context-protocol-mcp)
- [Articles & Blog Posts](#articles--blog-posts)
- [Tutorials & Guides](#tutorials--guides)
- [Videos & Talks](#videos--talks)
- [Podcasts](#podcasts)
- [Courses & Training](#courses--training)
- [Books](#books)
- [Research Papers](#research-papers)
- [Datasets & Benchmarks](#datasets--benchmarks)
- [Newsletters](#newsletters)
- [Communities](#communities)

## Tools & Frameworks

*Open-source tools and frameworks that combine AI/ML with network automation.*

<!-- Resources go here. -->

## LLM & Agent Tooling

*LLM-based assistants, copilots, and agentic systems for networking and engineering tasks.*

- [Agent Skills](https://github.com/addyosmani/agent-skills) - Pack of production engineering skills for coding agents covering spec-driven development, incremental implementation, code simplification, and review gates, portable across Claude Code, Cursor, Codex, and others.
- [caveman](https://github.com/JuliusBrussee/caveman) - Agent skill that cuts output tokens by rewriting agent prose into a terse fragment style, with configurable compression levels and commands for commits and memory-file rewrites.
- [herdr](https://herdr.dev/) - Terminal-native multiplexer for AI coding agents that gives each agent its own pane, with automatic state detection, detachable persistent sessions, and a socket API for orchestration.
- [NetCopilot](https://github.com/AnasProgrammer2/netcopilot) - SSH/Telnet/serial client with ARIA, an agent that runs diagnostic commands and explains root causes across Cisco, Juniper, Arista, Nokia SR-OS, Huawei VRP, MikroTik, Fortinet, Palo Alto, and F5 (source-available, BSL 1.1).
- [Open WebUI](https://github.com/open-webui/open-webui) - Self-hosted, extensible AI platform and chat interface that runs fully offline, supporting multiple LLM runners (Ollama, OpenAI-compatible APIs), RAG, and tool calling.
- [Ponytail](https://github.com/DietrichGebert/ponytail) - Plugin for AI coding agents (Claude Code, Codex, Copilot) that enforces a "reuse before you build" decision ladder to minimise new code.
- [Skills for Real Engineers](https://github.com/mattpocock/skills) - Collection of composable agent skills targeting common coding-agent failure modes, including TDD, code review, bug diagnosis, and codebase architecture improvement.

## Libraries & SDKs

*Programming libraries for building AI-driven network automation.*

- [GCF (Graph Compact Format)](https://github.com/blackwell-systems/gcf) - AI-native, lossless wire format for passing structured data to LLMs and agents, with a grammar reverse-engineered from tokenization and attention-level analysis and zero-dependency SDKs in six languages.

## Platforms & Products

*Commercial and hosted platforms with AI network automation capabilities.*

- [NetPilot](https://netpilot.io) - Agent that builds lab topologies from plain-English descriptions, generating vendor-specific configs for Cisco, Juniper, Arista, Nokia, Palo Alto, and Fortinet and deploying them to cloud-hosted devices.
- [TopoAI](https://www.topoai.cc/) - Generates editable network topology diagram drafts from natural-language descriptions, sketches, and screenshots.

## Model Context Protocol (MCP)

*MCP servers and integrations exposing tooling to AI agents.*

- [ACI MCP](https://github.com/k3l0-dev/aci-mcp) - Schema-driven MCP server for Cisco ACI that lets an agent search the APIC object model, inspect a class schema, and run filtered queries without hardcoded class knowledge. Read-only, source-available under a non-commercial licence.
- [gridctl](https://github.com/gridctl/gridctl) - Gateway that aggregates multiple MCP servers and Agent Skills behind a single declarative YAML endpoint, with token-saving output conversion and per-call cost tracking.
- [MCP Gateway](https://github.com/jongaudu/mcp-gateway) - Proxy server that consolidates multiple MCP backend servers behind a single endpoint, with lazy schema loading and a web dashboard.
- [mcpo](https://github.com/open-webui/mcpo) - Proxy server that exposes any MCP tool as an OpenAPI-compatible HTTP endpoint, making MCP tooling usable from standard web APIs and agents.
- [Netmiko MCP](https://github.com/ktbyers/netmiko_mcp) - MCP server that gives AI agents controlled SSH access to network devices via Netmiko, with command whitelisting for safety.
- [tailscale-mcp](https://github.com/YawLabs/tailscale-mcp) - MCP server for managing Tailscale tailnets from AI assistants, covering devices, ACLs, DNS, auth keys, users, webhooks, and audit logs.

## Articles & Blog Posts

*Notable articles, write-ups, and blog posts.*

- [AI Agent Trends Engineers Should Care About](https://danielbeck.dev/blog/ai-agent-trends-engineers-should-care-about/) - Overview of emerging AI agent trends relevant to engineers.
- [The PENE Framework for AI Network Operations](https://sifbaksh.com/blog/pene-framework-ai-network-operations/) - Introduces the PENE framework for applying AI to network operations.
- [The Schema-Driven LLM Query Pattern](https://www.packetcoders.io/the-schema-driven-llm-query-pattern/) - Describes a pattern that uses a defined schema to structure and validate LLM outputs for reliable, structured querying of network data.

## Tutorials & Guides

*Hands-on tutorials and how-to guides.*

- [NetAgents](https://netagents.ai/) - Field guide to agentic AI in networking, cataloguing what vendors and open-source projects are shipping, alongside explainers on MCP and the IETF drafts bringing it to network devices, agent security risks, and TM Forum autonomy levels.

## Videos & Talks

*Conference talks, webinars, and video walkthroughs.*

<!-- Resources go here. -->

## Podcasts

*Podcasts and episodes covering AI in networking.*

- [The Cloud Gambit: AutoCon 4 Recap, AI Tools, MCP's First Birthday](https://packetpushers.net/podcasts/the-cloud-gambit/tcg065-autocon-4-recap-ai-tools-mcps-first-birthday-and-more/) - Episode covering AutoCon 4 takeaways, AI tooling for network engineers, and a year of MCP.

## Courses & Training

*Structured courses and training programs.*

- [AI Engineering from Scratch](https://github.com/rohitg00/ai-engineering-from-scratch) - Open-source curriculum teaching AI engineering from mathematical foundations through production deployment, with 503 lessons across 20 phases.

## Books

*Books covering AI, ML, and network automation.*

- [AI Networking Cookbook](https://www.packtpub.com/en-us/product/ai-networking-cookbook-9781805807988) - Recipe-based guide by Eric Chou to AI-assisted network automation, covering OpenAI API scripting, prompt engineering, local LLM fine-tuning, LangChain, and Streamlit frontends across multi-vendor APIs (Packt, 2026).
- [Building AI Agents for Network Operations](https://www.packtpub.com/en-us/product/building-ai-agents-for-network-operations-9781808346828) - Guide by Sif Baksh to LLM-powered NetOps workflows with Python and Ollama, covering the RACE prompt structure, parsing interface and BGP output into structured data, and connecting models to approved tools via MCP and tool calling (Packt, 2026).

## Research Papers

*Academic papers and research.*

<!-- Resources go here. -->

## Datasets & Benchmarks

*Datasets and benchmarks for training and evaluating models on networking tasks.*

<!-- Resources go here. -->

## Newsletters

*Newsletters worth subscribing to.*

- [Packet Coders Newsletter](https://www.packetcoders.io/newsletter/) - Monthly network automation newsletter that regularly covers AI and LLM tooling for network engineers.

## Communities

*Forums, Slack/Discord communities, and groups.*

<!-- Resources go here. -->

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainers have waived all copyright and related or neighboring rights to this work. See [LICENSE](LICENSE).
