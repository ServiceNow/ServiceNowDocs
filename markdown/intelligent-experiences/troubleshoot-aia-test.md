---
title: Troubleshooting agentic AI manual testing failures
description: When testing an agentic AI asset in AI Agent Studio, there are a few common errors that can be addressed before you test again.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/troubleshoot-aia-test.html
release: australia
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 1
breadcrumb: [Reference, AI Agent Studio, Enable AI experiences]
---

# Troubleshooting agentic AI manual testing failures

When testing an agentic AI asset in AI Agent Studio, there are a few common errors that can be addressed before you test again.

Most failures in a first manual test of an agentic AI asset can be traced to issues with configuration. The run may complete, a tool reports an error in the trace, and nothing in the testing panel names the cause. Check for the following errors before attempting to adjust prompts.

-   **Misspelled inputs, fields, or variable names**

    Names are matched exactly and are not validated when you save an agentic AI asset, so the failure appears only at run time as a tool error. Check the name against the field label on the table.

-   **Records or other identifiers in the objective that don't exist**

    Record identifiers that don't exist on the instance fail the lookup and end the objective early. Confirm the record exists before looking for a fault in the agentic AI asset.

-   **Inconsistent access to subcomponents**

    Check whether all of the components of the agentic AI asset have the same ACL requirements. A tool whose ACL the running identity cannot pass may fail for some users and not others. Compare the invoking user roles against what the tool requires. Run tests as different users to verify the security constraints you've added.

-   **Incorrect tool calling**

    Multipurpose or loosely described tools can lead the Orchestrator to select the wrong tool. Give each tool a single purpose. Tool descriptions should also include when it does not apply.


