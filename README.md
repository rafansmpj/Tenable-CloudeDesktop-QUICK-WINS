# Tenable Quick Wins - Claude Desktop Skills

An agent that works with the Hexa AI MCP to build/generates an interactive Executive Dashboard for Quick Wins to reduce the Tenable One Exposure Score across cumulative phases of 10%-20%-30%-40%-50%. 

## What it does

Generates an interactive Executive Dashboard for Quick Wins to reduce the Tenable One Exposure Score across cumulative phases of 10%-20%-30%-40%-50%. ALWAYS use this skill when the user asks for quick wins, fast gains, a phased risk reduction plan, a remediation roadmap, how to reduce their score, which vulnerabilities to close first, a 50% reduction plan, an executive prioritization dashboard, or when they mention percentage-based exposure reduction goals. The skill connects to the Tenable HEXA AI MCP, calculates which vulnerabilities and actions generate the greatest score reduction with the least effort (high VPR × assets affected × fix ease), and presents an interactive visual dashboard with cumulative remediation phases, industry benchmark, and score projection. Also use when the user mentions "where to start", "highest impact with least effort", "10 to 50 percent reduction", "C-Level remediation prioritization", "executive security roadmap", or "vulnerability quick wins".

## Quick Start (5 minutes)

### 1. Prerequisites

- Claude Code (or another Claude environment with skills support) installed locally.
- A Tenable One MCP server connected and authenticated — this is what provides live Exposure Score, vulnerability findings, Crown Jewels, and attack path chokepoint data. Without it, the skill falls back to a "DEMO — illustrative data" mock dashboard.
- The MCP connection needs read access to: Exposure View (score, domain notes, industry benchmark), Findings/Vulnerabilities (VPR, severity, affected assets), Crown Jewels list, and Attack Path graph (for chokepoint identification).
- An environment capable of rendering the resulting React/HTML artifact (Claude.ai or Claude Code's artifact viewer).

### 2. Installation

Copy the skill folder into the local Claude Code skills directory:

~/.claude/skills/tenable-quick-wins-dashboard/

The folder should contain SKILL.md (and optionally README.md, LICENSE, listing.yaml as packaged). No build step or dependencies to install — it's a prompt-driven skill, not code that needs compiling.

### 3. Configure

- Make sure the Tenable One HEXA AI MCP connector is set up and active in the same Claude environment (this is the one external dependency; everything else, like the color palette, phase logic, and scoring weights, is hardcoded in SKILL.md).
- Optionally, set organizational context the skill will use when invoked: industry/sector (for benchmark comparison), language preference (English/Portuguese), and any default filters (e.g., always focus on Crown Jewels, or always include regulatory mapping like LGPD/ISO 27001/NIST CSF/PCI-DSS).
- No API keys or .env files are needed inside the skill itself — credentials live entirely in the MCP connector configuration, not in the skill folder.

