---
title: MCP Configuration Guide
description: Complete guide to configuring the Model Context Protocol for SEMCL.ONE
date: 2025-01-18
author: SEMCL.ONE Team
tags: [mcp, configuration, setup]
---

This guide provides comprehensive information on configuring the Model Context Protocol (MCP) for SEMCL.ONE.

## Overview

The Model Context Protocol (MCP) enables seamless communication between AI models and compliance tooling. Proper configuration ensures optimal performance and accurate results.

## Configuration File Structure

The MCP configuration file uses YAML format:

```yaml
mcp:
  version: "1.0"
  server:
    host: "localhost"
    port: 8080
  authentication:
    method: "api-key"
    key: "${MCP_API_KEY}"
  features:
    license-detection: true
    vulnerability-scan: true
    dependency-analysis: true
```

## Environment Variables

Set up the following environment variables:

- `MCP_API_KEY`: Your API key for authentication
- `MCP_SERVER_URL`: Custom server URL (optional)
- `MCP_LOG_LEVEL`: Logging verbosity (debug, info, warn, error)

## Server Configuration

### Local Server

To run a local MCP server:

```bash
mcp-semclone server --config ./mcp-config.yml
```

### Cloud Deployment

For cloud deployments, configure your server endpoint:

```yaml
server:
  endpoint: "https://mcp.semcl.one/api/v1"
  region: "us-west-2"
  timeout: 30000
```

## Authentication Methods

### API Key Authentication

The recommended method for most users:

```yaml
authentication:
  method: "api-key"
  key: "${MCP_API_KEY}"
```

### OAuth 2.0

For enterprise deployments:

```yaml
authentication:
  method: "oauth2"
  client_id: "${OAUTH_CLIENT_ID}"
  client_secret: "${OAUTH_CLIENT_SECRET}"
  token_url: "https://auth.semcl.one/token"
```

## Feature Flags

Enable or disable specific features:

```yaml
features:
  license-detection:
    enabled: true
    cache-results: true

  vulnerability-scan:
    enabled: true
    sources:
      - nvd
      - github-advisories

  dependency-analysis:
    enabled: true
    max-depth: 10
    include-dev-dependencies: false
```

## Best Practices

1. **Use environment variables** for sensitive data
2. **Enable caching** to improve performance
3. **Set appropriate timeouts** based on your project size
4. **Regularly update** your configuration as new features are released

## Troubleshooting

### Connection Issues

If you experience connection problems:

```bash
mcp-semclone diagnose --verbose
```

### Performance Issues

For slow scans, try:

- Reducing scan depth
- Enabling parallel processing
- Excluding unnecessary directories

## Additional Resources

- [API Documentation](https://docs.semcl.one/api)
- [GitHub Repository](https://github.com/SemClone)
- [Community Forum](https://community.semcl.one)
