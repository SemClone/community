---
title: "Welcome to SEMCL.ONE"
date: 2025-12-04
author: SEMCL.ONE Team
---

Welcome to the SEMCL.ONE Community!

We're building the future of Open Source Software compliance—one where automation replaces manual work, communities share resources instead of duplicating efforts, and AI-powered tools make compliance accessible to everyone.

## What is SEMCL.ONE?

SEMCL.ONE is a comprehensive, community-driven Software Composition Analysis (SCA) platform designed to solve one of software development's biggest challenges: **managing open source compliance at scale** fully leveraging AI.

Every organization using open source software faces the same problems:
- Manually tracking hundreds or thousands of dependencies
- Identifying license obligations and incompatibilities
- Generating legal notices and SBOMs for distribution
- Detecting GPL contamination and patent-encumbered code
- Validating compliance policies across projects
- Doing all of that at scale

Traditional SCA tools are expensive, closed-source, and often miss AI-generated code transformations. **SEMCL.ONE takes a different approach**: open source tools, open data, shared infrastructure, and GenAI automation.

## Our Mission: Automation First

**We believe compliance should be automated, not manual.**

SEMCL.ONE provides a complete toolchain that automates the entire compliance workflow:

1. **Identify** - Detect packages and dependencies automatically
2. **Analyze** - Extract licenses, copyrights, and metadata
3. **Validate** - Check against compliance policies
4. **Report** - Generate SBOMs, notices, and documentation
5. **Monitor** - Continuous compliance in CI/CD pipelines

But we go further. With **MCP-SEMCLONE**, we bring compliance directly into your IDE—integrated with AI coding assistants like Kiro, Cursor, Cline, and others. Ask your AI: *"Is this project safe for commercial distribution?"* Get instant, automated compliance analysis.

## The SEMCL.ONE Toolchain

Our platform is built on 11+ specialized small tools, each solving a specific compliance challenge:

### Package Intelligence

**PURL2SRC** - Convert Package URLs to downloadable source code across 13+ ecosystems (npm, PyPI, Maven, Cargo, etc.)

**SRC2PURL** - Identify package coordinates from source code, reverse-engineering dependency information

**UPMEX** - Universal Package Metadata Extractor supporting 15+ package formats with standardized JSON output, dependency mapping, and API enrichment

### License & Copyright Detection

**OSSLILI** - High-performance license detector supporting 700+ SPDX identifiers with three-tier detection (Dice-Sørensen similarity, TLSH fuzzy hashing, regex patterns), copyright extraction, and comprehensive SBOM generation

**PURL2NOTICES** - Generate legal attribution notices and copyright documentation from Package URLs for distribution compliance

### Binary & Code Analysis

**BinarySniffer** - Detect hidden OSS components in compiled binaries, finding what traditional scanners miss. Now supports AI artifacts looking for problematic patterns in serialized components to detect weaponized models.

**Semantic CopyCat (CopycatM)** - Advanced IP contamination detection using transformation-resistant signatures to catch AI-generated code that copies GPL or patented algorithms—even across language translations and heavy refactoring

### Policy & Risk Management

**OSPAC** - Open Source Policy as Code engine with complete SPDX coverage (712 licenses), compatibility checking, and obligation tracking. Define compliance rules in version-controlled policy files.

**VulnQ** - Multi-source vulnerability query tool consolidating security data from various databases

### Automation & Integration

**MCP-SEMCLONE** - Model Context Protocol server that brings all SEMCL.ONE tools into AI-powered IDEs (Cursor, Cline, VS Code, Kiro). Enables conversational compliance: ask your AI assistant for license analysis, SBOM generation, or policy validation—all automated.

## Why Open Source and Community-Driven?

We're committed to **transparency and community collaboration**:

- **Open Source Code** - All tools are openly developed, auditable, and improvable by the community
- **Community-Developed Data** - Shared reference databases built collaboratively—license patterns, algorithm signatures, and vulnerability mappings that the community contributes to and benefits from
- **Open Standards** - Built on SPDX, PURL, CycloneDX, and other industry standards

This approach enables:
- **Community Collaboration** - Contribute discoveries and benefit from collective knowledge
- **Decentralized Operations** - Run tools locally, in your cloud, or use community instances
- **Collective Intelligence** - Improved detection through community-contributed patterns and shared research

## Automation Through AI Integration

The real breakthrough is **MCP-SEMCLONE**, our Model Context Protocol server that integrates the entire SEMCL.ONE toolchain with AI coding assistants.

**What this means for developers:**

Instead of running separate CLI commands or switching to web dashboards, you simply ask your AI:

- *"Scan this project for license compliance issues"*
- *"What are my obligations for the Apache-2.0 license?"*
- *"Is this package safe for mobile app distribution?"*
- *"Generate SBOM for this release"*
- *"Check if GPL-2.0 and Apache-2.0 are compatible"*
- *"Create NOTICE file for distribution"*

Your AI assistant handles it automatically, using SEMCL.ONE tools behind the scenes. No manual commands. No context switching. Just conversational compliance.

**Supported IDEs:**
- Kiro IDE
- Cursor IDE
- Cline (VS Code extension)
- VS Code (with MCP extensions)
- JetBrains IDEs (with AI plugin)

## Real-World Use Cases

### For Individual Developers
- Check license compatibility before adding dependencies
- Generate attribution notices for your projects
- Validate compliance before publishing to npm, PyPI, etc.

### For Teams
- Automate compliance checks in pull requests
- Share compliance policies across projects
- Generate SBOMs for security audits

### For Organizations
- Enforce consistent compliance policies company-wide
- Track license obligations across thousands of packages
- Detect IP contamination in AI-generated code
- Generate legal documentation for product releases

## Current Status

SEMCL.ONE is **79% complete** with 12 core components operational:

**Production-Ready Tools:**
- OSSLILI (v1.5+) - License detection
- OSPAC (v1.2+) - Policy engine
- UPMEX - Package metadata extraction
- PURL2SRC - Source download URLs
- PURL2NOTICES - Legal notice generation
- MCP-SEMCLONE - IDE integration

**In Development:**
- Semantic CopyCat - IP contamination detection
- OSSVAL
- Open Source Compliance Advisory
- Web management interface
- Compliance dashboard

## Get Involved

SEMCL.ONE is community-driven. Here's how you can participate:

### Use the Tools

Install from PyPI:
```bash
pip install osslili ospac upmex purl2src purl2notices
pipx install mcp-semclone
```

Or from source:
```bash
git clone https://github.com/SemClone/{tool-name}
cd {tool-name}
pip install -e .
```

### Contribute

- **Report bugs** - Help us improve quality
- **Suggest features** - Shape the roadmap
- **Write code** - Fix bugs, add features
- **Improve docs** - Make tools more accessible
- **Share patterns** - Contribute to reference databases (license patterns, algorithm signatures)

### Commercial Services

Enterprise support and commercial data services are available from ecosystem partners, including:
- Enterprise support and consulting
- Business continuity risk advisories
- Commercial data intelligence
- Custom policy development
- Integration services
- Training and workshops


## Join the Community

- **Website**: [https://semcl.one](https://semcl.one)
- **GitHub**: [https://github.com/SemClone](https://github.com/SemClone)
- **MCP Server**: [https://github.com/SemClone/mcp-semclone](https://github.com/SemClone/mcp-semclone)

## The Vision

**We're building a future where:**
- Compliance is automated, not a burden
- Open source is used safely and legally
- AI coding assistants understand licensing
- Compliance tools are simple and accessible to everyone

**Welcome to SEMCL.ONE. Let's build the future of compliance together.**

---

*Got questions? Want to contribute? Check our [GitHub organization](https://github.com/SemClone) or explore the tools at [semcl.one](https://semcl.one).*
