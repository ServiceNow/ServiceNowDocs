---
title: Example prompts for MCP for Enterprise Architecture
description: Example prompts that you can use with MCP for Enterprise Architecture, with the role that typically asks each one and the outcome it produces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-portfolio-management/ea-mcp-server-example-prompts.html
release: australia
topic_type: reference
last_updated: "2026-10-12"
reading_time_minutes: 3
keywords: [EA MCP server, example prompts]
breadcrumb: [Reference, MCP for Enterprise Architecture, Enterprise Architecture]
---

# Example prompts for MCP for Enterprise Architecture

Example prompts that you can use with MCP for Enterprise Architecture, with the role that typically asks each one and the outcome it produces.

To answer these prompts, your AI assistant can combine several MCP for EA tools in one response. The results depend on the EA data in your instance. For the tools that are available, see [Explore MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/exploring-ea-mcp-server.md).

|Prompt|Asked by|Outcome|
|------|--------|-------|
|`If I had to cut 15% of our application spend this year, which applications should we retire or consolidate, and what would break if we did?`|Application portfolio owner|Defensible cost-reduction plan that combines rationalization scores, redundancy by capability, and dependency impact in one answer.|
|`Which of our strategic business capabilities depend on applications with high technology risk or end-of-life components in the next 12 months?`|Business capability owner|Prioritized risk list that shows where the business strategy is exposed, so remediation funding goes to what matters most.|
|`Where do we have multiple applications supporting the same capability, and which one should be our strategic platform?`|Enterprise architect|Consolidation opportunities backed by scores for business fit, technical health, and cost, lowering complexity and license spend.|
|`Build a sequenced modernization roadmap for the Finance domain: what to retire, migrate, or invest in first, so that no critical dependency breaks along the way.`|Enterprise architect|Actionable, dependency-aware roadmap that turns portfolio analysis into an execution plan.|
|`Prepare an executive brief on *application* covering business value, cost, risk, capability coverage, dependencies, and a recommended disposition.`|Application or capability owner preparing for an architecture review board or budget review|Decision-ready summary in minutes instead of days of pulling data from multiple views.|
|`Compare the current and previous versions of this architecture diagram. What changed, and what is the impact on dependent applications, services, and capabilities?`|Enterprise architect|Instant change impact analysis, so reviewers see the consequences of a design change without manually tracing every connection.|
|`Review this solution architecture against our approved technology standards and reference architectures. Where does it deviate, and what risks do those deviations introduce?`|Architecture review board member|Faster, more consistent design reviews that catch nonstandard technology, unapproved vendors, or policy violations before approval.|
|`Does this target-state diagram include any applications flagged for retirement, high technology risk, or end-of-life components?`|Application portfolio owner|Prevention of new designs that build on components the organization is already trying to retire.|
|`Does this diagram match what actually exists in our CMDB? Show me missing components, undocumented integrations, and outdated relationships.`|Enterprise architect|Trustworthy diagrams, by closing the gap between documented architecture and the operational landscape.|
|`Identify single points of failure, security gaps, and integration bottlenecks in this architecture, and suggest how to fix them.`|Solution architect or capability owner|Stronger resilience and security designs, with concrete improvement recommendations before the design goes into build.|

**Parent Topic:**[MCP for Enterprise Architecture reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/reference-ea-mcp-server.md)

**Related topics**  


[Access Enterprise Architecture data using MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/access-ea-data-using-mcp-tools.md)

[MCP for Enterprise Architecture tool parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/ea-mcp-server-tool-parameters.md)

