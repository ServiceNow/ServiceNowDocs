---
title: Monitoring an MCP server
description: Identify tools on an MCP server that fail often or respond slowly by reviewing request counts, success rates, and latency percentiles for each tool that AI agents call through AI Gateway.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/mon-ai-mcp-server-monitor.html
release: australia
topic_type: concept
last_updated: "2026-10-14"
reading_time_minutes: 3
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Working with MCP server records, Discover and manage AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Monitoring an MCP server

Identify tools on an MCP server that fail often or respond slowly by reviewing request counts, success rates, and latency percentiles for each tool that AI agents call through AI Gateway.

The **Monitor** tab on an MCP server record summarizes how each tool on that server performs when AI agents call it through AI Gateway.

AI Gateway records the calls that agents make to the tools on the server, and the tab summarizes those calls for each tool. Unlike the **Monitor** tab for an AI system, which reports quality and safety scores, the **Monitor** tab for an MCP server reports operational performance. For metrics across all MCP servers, see .

## Key benefits

-   Find tools that return errors by comparing success rates across every tool on a server.
-   Judge how widely a problem affects agents by comparing each tool's success rate with its request count.
-   Detect slow responses by comparing median and worst-case latency for each tool.
-   Review tool performance on the MCP server record without switching to the AI Gateway view of all servers.

## When tool metrics appear

Tool metrics appear for managed MCP servers. For an unmanaged server, the tab displays a message that the asset must be managed before the dashboard can appear.

## MCP tools observability metrics

The MCP tools observability metrics list shows one row for each tool that agents called during the last 30 days. The list contains the following columns.

-   **Tool name**

    Name of the tool as defined by the MCP server.

-   **Requests**

    Number of times agents called the tool during the period. Use this value to judge how much weight to give the other columns for the same tool, because a low success rate across many requests indicates a broader problem than the same rate across a few requests.

-   **Success rate**

    Percentage of the tool's requests that returned an HTTP status code from 200 through 299. A low value indicates that agents are receiving errors from the tool.

-   **Latency P50**

    Request duration, in milliseconds, at or below which 50 percent of the tool's successful requests completed. This is the median, so it represents typical performance.

-   **Latency P90**

    Request duration, in milliseconds, at or below which 90 percent of the tool's successful requests completed. The slowest 10 percent of successful requests took longer.

-   **Latency P95**

    Request duration, in milliseconds, at or below which 95 percent of the tool's successful requests completed. The slowest 5 percent of successful requests took longer.


## Reading latency percentiles

Percentiles describe the spread of response times rather than a single average. Comparing the three latency values for the same tool shows whether slow responses are typical or occasional.

When P50 is low but P90 and P95 are much higher, most calls respond quickly while a minority run slowly. For example, a tool with a P50 of 553 ms and a P95 of 1,845 ms responds in about half a second for a typical call, and roughly one successful call in 20 takes about 1.8 seconds or longer. P95 is the most useful of the three for judging worst-case behavior in workflows where one slow response delays the whole task.

Latency percentiles are calculated from successful requests only. Requests that return an error count toward **Requests** and **Success rate** but not toward the latency columns, so a tool that fails often can still show low latency. A tool with no successful requests shows a latency of 0. Latency values are approximate, with a relative error of up to 1 percent.

For a tool with few successful requests, the three values are often identical because each is calculated from the same small set of requests. Percentiles carry more meaning as the request count grows.

## Prioritizing tools to investigate

Tools that combine a low success rate with a high request count affect the most agent calls, so they are the strongest candidates for investigation. Tools with an acceptable success rate but a wide gap between P50 and P95 are candidates for a latency review.

