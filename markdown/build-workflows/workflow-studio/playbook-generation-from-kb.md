---
title: Playbook generation from a knowledge base article
description: Generate a playbook directly from an existing knowledge base article to reduce manual effort when creating playbooks for documented processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/playbook-generation-from-kb.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 1
breadcrumb: [Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Playbook generation from a knowledge base article

Generate a playbook directly from an existing knowledge base article to reduce manual effort when creating playbooks for documented processes.

When you create a playbook from a knowledge base article, AI reads the article, identifies the stages and activities described in the content, and generates a structured playbook based on the information. Each generated activity includes a description derived from the article content.

This feature is useful when your organization has existing knowledge base articles that describe operational processes. Instead of recreating those processes manually as playbook stages and activities, you can use the article as the source and let AI generate the playbook structure.

## How the playbook generation works

AI extracts the content of the selected knowledge base article and combines it with any optional instructions you provide. This combined input is passed to the playbook generation skill, which identifies stages and activities, and generates the playbook structure. The generated playbook appears as a preview before you save it.

Knowledge base article content takes priority over user-provided instructions. AI generates stages and activities only from the content in the article and does not add content from other sources.

## Limitations

-   The knowledge base article must describe an actual process with discrete steps. Articles that contain only definitions, organizational charts, or reference information aren't suitable for playbook generation. If AI determines that an article does not represent a valid process, it does not generate a playbook.
-   The feature supports knowledge base articles up to 13,000 characters. For articles that exceed this limit, AI uses only the main process-relevant portions of the content.
-   Only knowledge base articles that are accessible to the logged-in user are available for selection.

-   **[Generate a playbook from a knowledge base article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/generate-playbook-from-kb.md)**  
Use an existing knowledge base article to generate a playbook using AI. The stages and activities are automatically populated based on the article content.

**Parent Topic:**[Creating and managing Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/creating-managing-playbooks.md)

**Related topics**  


[Generate a playbook from a knowledge base article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/generate-playbook-from-kb.md)

