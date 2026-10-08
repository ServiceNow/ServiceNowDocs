---
title: Zurich Patch 12 W33 Hotfix 1
description: The Zurich Patch 12 W33 Hotfix 1 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-12-W33-hf-1-PO.html
release: zurich
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 3
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 12 W33 Hotfix 1

The Zurich Patch 12 W33 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 09-22-2026\_1817

    Build tag: glide-zurich-07-01-2025\_\_patch12w33-hotfix1-09-14-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Virtual Agent

 PRB2078678

</td><td>

The dynamic loading 'Processing new information' progress message is not translated in localized Now Assist Virtual Agent \(NAVA\) conversations

</td><td>

Even though the values are translated in Spanish when the user opens **Testing \(En pruebas\)** in AI Agent Studio \(Estudio de agentes de IA\), the message 'Processing new information' remains in English and is not translated to Spanish.

</td><td>

1.  Set up Dynamic Translation.
2.  Change the language to Spanish.
3.  Navigate to **AI Agent Studio \(Estudio de agentes de IA\)** &gt; **Testing \(En pruebas\)**.

Observe the following values that are translated:

    -   Choose a test type AI agent or workflow \(Elegir un tipo de prueba\): Agente de IA o Flujo de trabajo
    -   Name of the AI Agent or agentic workflow \(Nombre del agente de IA o flujo de trabajo agéntico\): Agente de IA de categorizar incidentes de ITSM
    -   Version: 1 - V1 \(activo\)
    -   Task: INC000XXXX
4.  Select **Continuar para probar la respuesta del chat**.
5.  Watch the dynamic loading messages.

 Expected behavior: The user sees 'Processing new information' translated in Spanish, 'Procesando nueva información'.

 Actual behavior: The English text 'Processing new information' displays and is not translated to Spanish.

</td></tr><tr><td>

List Filters

 PRB2031646

</td><td>

Mixed language text is displayed in the filter

</td><td>

When the session is in a language other than English, the pop up invoked from the list filter controls displays text in English.

</td><td>

1.  Open a Zurich instance.
2.  Install the I18N: Brazilian Portuguese Translations plugin.
3.  Open the System Preferences.
4.  Switch the language to Portuguese.
5.  Open Service Operations Workspace.
6.  Select the **List** icon.
7.  Open any interaction.
8.  Select the filter control **x filtros**.

 Observe that there is English text content, such as 'Generate filters', when it should be in Portuguese, such as 'gerar filtros'.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 12 W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147948)
-   [Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)
-   [Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)
-   [Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)
-   [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)
-   [Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)

