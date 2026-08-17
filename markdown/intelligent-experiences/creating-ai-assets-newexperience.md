---
title: Creating AI assets manually
description: You can create AI assets to track and manage the life cycles of your AI systems, AI models, prompts, and datasets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/creating-ai-assets-newexperience.html
release: zurich
topic_type: concept
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Creating AI assets manually

You can create AI assets to track and manage the life cycles of your AI systems, AI models, prompts, and datasets.

## Manually creating AI assets

Most AI assets enter your inventory through automated discovery, Service Graph Connectors, or observability traces. Manual creation is the option to use when an asset isn't reachable by those methods, or when you need to record an asset that isn't yet operational so governance work can begin before deployment.

The intake form is a three-step process for AI systems, a two-step process for AI models, and a single-step process for both prompts and datasets. The first step captures the asset's identifying information, including the name, asset type, and provider. The second step is where you link related assets — for example, associating an AI system with the AI models, prompts, datasets, and tools it depends on — so AI Control Tower can track relationships and assess governance impact across the portfolio. The third step captures the use and purpose of the asset, including the primary business outcome and the type of output produced.

Manually created assets enter the inventory in the unmanaged state. To bring an asset into governance workflows, set its management status to managed from the inventory list or initiate a steward review.

