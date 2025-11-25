---
title: Getting Started with MCP-SEMCLONE
description: A quick start guide to help you begin using MCP-SEMCLONE for OSS compliance tooling
date: 2025-01-15
author: SEMCL.ONE Team
tags: [getting-started, mcp, setup]
---

Welcome to MCP-SEMCLONE! This guide will help you get up and running quickly.

## What is MCP-SEMCLONE?

MCP-SEMCLONE is an AI-driven OSS compliance tooling solution that helps you manage and track open source software compliance in your projects.

## Prerequisites

Before you begin, make sure you have:

- Node.js 18 or higher installed
- A Claude API key
- Basic familiarity with command-line tools

## Installation

Install MCP-SEMCLONE using npm:

```bash
npm install -g mcp-semclone
```

Or using yarn:

```bash
yarn global add mcp-semclone
```

## Configuration

1. Create a configuration file in your home directory:

```bash
mcp-semclone init
```

2. Add your API credentials to the configuration file

3. Test your configuration:

```bash
mcp-semclone test
```

## Basic Usage

Run a compliance scan on your project:

```bash
mcp-semclone scan ./path/to/project
```

Generate a compliance report:

```bash
mcp-semclone report --format pdf
```

## Next Steps

- Explore the [User Guides](/docs/user_guides/) for detailed documentation
- Check out more [Examples](/docs/examples/) for advanced use cases
- Join our [GitHub Discussions](https://github.com/SemClone/) for community support

## Need Help?

If you encounter any issues, please:

- Check our [troubleshooting guide](#)
- Visit our [GitHub Issues](https://github.com/SemClone/issues)
- Contact support at support@semcl.one
