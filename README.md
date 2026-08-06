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

- [Packet Buddy](https://github.com/automateyournetwork/packet_buddy) - Dockerised Streamlit app that embeds a packet capture and answers questions about it conversationally, running fully locally against Ollama models.
- [Packet RAPTOR](https://github.com/automateyournetwork/packet_raptor) - Packet capture assistant that builds a RAPTOR recursive-summary tree over the capture before querying it, aimed at larger files than a flat retrieval approach handles well.

## LLM & Agent Tooling

*LLM-based assistants, copilots, and agentic systems for networking and engineering tasks.*

- [Agent Skills](https://github.com/addyosmani/agent-skills) - Pack of production engineering skills for coding agents covering spec-driven development, incremental implementation, code simplification, and review gates, portable across Claude Code, Cursor, Codex, and others.
- [caveman](https://github.com/JuliusBrussee/caveman) - Agent skill that cuts output tokens by rewriting agent prose into a terse fragment style, with configurable compression levels and commands for commits and memory-file rewrites.
- [GAIT](https://github.com/automateyournetwork/gait) - Version control system for AI conversations that commits, branches, and merges agent turns, and pins selected turns into a persistent memory layer injected into every later prompt.
- [herdr](https://herdr.dev/) - Terminal-native multiplexer for AI coding agents that gives each agent its own pane, with automatic state detection, detachable persistent sessions, and a socket API for orchestration.
- [MCPyATS](https://github.com/automateyournetwork/MCPyATS) - Containerised reference stack pairing Cisco pyATS with a LangGraph agent, a Streamlit frontend, and a set of MCP tool servers, plus an A2A adapter for agent-to-agent delegation.
- [NetBox ReAct Agent](https://github.com/automateyournetwork/netbox_react_agent) - ReAct agent that performs CRUD operations against the NetBox API from plain-English prompts, with separate branches for OpenAI models and local models via Ollama.
- [NetClaw](https://github.com/automateyournetwork/netclaw) - Agentic network engineering assistant built on OpenClaw, bundling hundreds of skills and MCP integrations across multi-vendor devices, controllers, labs, observability, and ITSM, with change gating, source-of-truth reconciliation, and an immutable audit trail.
- [NetCopilot](https://github.com/AnasProgrammer2/netcopilot) - SSH/Telnet/serial client with ARIA, an agent that runs diagnostic commands and explains root causes across Cisco, Juniper, Arista, Nokia SR-OS, Huawei VRP, MikroTik, Fortinet, Palo Alto, and F5 (source-available, BSL 1.1).
- [Open WebUI](https://github.com/open-webui/open-webui) - Self-hosted, extensible AI platform and chat interface that runs fully offline, supporting multiple LLM runners (Ollama, OpenAI-compatible APIs), RAG, and tool calling.
- [Ponytail](https://github.com/DietrichGebert/ponytail) - Plugin for AI coding agents (Claude Code, Codex, Copilot) that enforces a "reuse before you build" decision ladder to minimise new code.
- [Skills for Real Engineers](https://github.com/mattpocock/skills) - Collection of composable agent skills targeting common coding-agent failure modes, including TDD, code review, bug diagnosis, and codebase architecture improvement.
- [Won't You Be My Neighbor](https://github.com/automateyournetwork/WontYouBeMyNeighbour) - Multi-agent platform in which agents self-configure and peer with one another over real OSPF and BGP implementations, using the routing control plane itself as the agent interconnect.

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
- [ACI MCP Server](https://github.com/automateyournetwork/ACI_MCP) - MCP server for the Cisco ACI APIC that builds read and write tools from a configurable endpoint map, handling token-based authentication and APIC payload wrapping.
- [Catalyst Center MCP](https://github.com/richbibby/catalyst-center-mcp) - MCP server for Cisco Catalyst Center (formerly DNA Center) exposing device inventory, client, and site data for management and monitoring.
- [Cisco SD-WAN MCP](https://github.com/siddhartha2303/cisco-sdwan-mcp) - Read-only MCP server that queries Cisco vManage for SD-WAN fabric devices, policies, and operational state.
- [Cisco Secure Firewall FMC MCP](https://github.com/CiscoDevNet/CiscoFMC-MCP-server-community) - MCP server for Firepower Management Center that searches access policies by IP, FQDN, or identity indicator such as SGT and realm user, and resolves FTD devices to their assigned policies.
- [clab-mcp-server](https://github.com/seanerama/clab-mcp-server) - MCP server for ContainerLab that deploys and manages containerised network labs through the ContainerLab API.
- [cml-mcp](https://github.com/xorrkaz/cml-mcp) - MCP server for Cisco Modeling Labs covering lab lifecycle, topology, and node management.
- [F5 BIG-IP MCP](https://github.com/czirakim/F5.MCP.server) - MCP server for F5 BIG-IP that exposes iControl REST operations across virtual servers, pools, and profiles.
- [gridctl](https://github.com/gridctl/gridctl) - Gateway that aggregates multiple MCP servers and Agent Skills behind a single declarative YAML endpoint, with token-saving output conversion and per-call cost tracking.
- [Infrahub MCP](https://github.com/opsmill/infrahub-mcp) - MCP server from OpsMill for Infrahub, giving agents access to its schema-driven, version-controlled source of truth.
- [ISE MCP](https://github.com/automateyournetwork/ISE_MCP) - MCP server that exposes Cisco ISE REST endpoints as FastMCP tools generated from a JSON endpoint map, with per-tool result filtering and streamable HTTP transport.
- [Itential MCP Server](https://github.com/itential/itential-mcp) - MCP server for the Itential Platform covering workflow orchestration, configuration management, compliance, and platform health.
- [Junos MCP Server](https://github.com/Juniper/junos-mcp-server) - Official Juniper MCP server bridging MCP clients and Junos devices over PyEZ and NETCONF, with configuration management tools.
- [MCP Gateway](https://github.com/jongaudu/mcp-gateway) - Proxy server that consolidates multiple MCP backend servers behind a single endpoint, with lazy schema loading and a web dashboard.
- [mcpo](https://github.com/open-webui/mcpo) - Proxy server that exposes any MCP tool as an OpenAPI-compatible HTTP endpoint, making MCP tooling usable from standard web APIs and agents.
- [Meraki Magic MCP](https://github.com/CiscoDevNet/meraki-magic-mcp-community) - Community MCP server from CiscoDevNet covering the Meraki Dashboard API across wireless, switching, security, and diagnostics.
- [Nautobot MCP](https://github.com/kvncampos/nautobot_mcp) - MCP server for Nautobot with STDIO and HTTP deployments, including embedding search and RAG over network source-of-truth data.
- [NetBox MCP](https://github.com/automateyournetwork/NetBox_MCP) - Full-CRUD MCP server for NetBox covering 119 object types across all ten API apps through eight generic tools, including next-available IP, prefix, VLAN, and ASN allocation.
- [netbox-mcp-server](https://github.com/netboxlabs/netbox-mcp-server) - Official NetBox Labs MCP server providing read-only access to NetBox DCIM and IPAM data.
- [Netmiko MCP](https://github.com/ktbyers/netmiko_mcp) - MCP server that gives AI agents controlled SSH access to network devices via Netmiko, with command whitelisting for safety.
- [pyATS MCP](https://github.com/automateyournetwork/pyATS_MCP) - MCP server wrapping Cisco pyATS and Genie so agents can run show commands, parse output into structured data, and apply configuration over STDIO JSON-RPC.
- [tailscale-mcp](https://github.com/YawLabs/tailscale-mcp) - MCP server for managing Tailscale tailnets from AI assistants, covering devices, ACLs, DNS, auth keys, users, webhooks, and audit logs.
- [ThousandEyes MCP Server](https://github.com/CiscoDevNet/ThousandEyes-MCP-Server-official) - Official MCP server for ThousandEyes, letting an assistant query tests, alerts, outages, and BGP routing data.

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
