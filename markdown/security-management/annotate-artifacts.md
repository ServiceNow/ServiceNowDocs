---
title: Annotate security artifacts
description: As you are analyzing a case, you can add annotations to any artifact.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security artifact analysis, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Annotate security artifacts

As you are analyzing a case, you can add annotations to any artifact.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required:

-   sn\_ti.case\_user\_write for adding annotations
-   sn\_ti.case\_user\_read to view annotations

## Procedure

1.  Open a case that contains artifacts that you want to annotate.

2.  Click the **Case Artifacts** related list.

3.  Click the tab associated with the artifacts you want to annotate.

    For example, click **Indicators of Compromise** to add annotations to IoCs.

4.  To add an annotation to one or more artifacts, perform the following steps:

    1.  Select the artifacts to which you want to add an annotation.

    2.  Click **Annotate**.

        ![Add an annotation](../image/annotations.png)

    3.  Type the annotation and click **Annotate**.

        The annotation is added to the selected artifacts.

5.  To view annotations for an artifact, click the View annotations \(![View Annotations](../image/annotation-icon.png)\) icon.

    The existing annotations appear in the Annotations dialog box.

    ![Annotations dialog box](../image/annotations-dialog.png)

6.  You can also enter a new annotation for the artifact in the **Security Annotation** box, and click **Annotate**.


**Parent Topic:**[Security artifact analysis](../concept/sec-artifact-analysis.md)

**Related topics**  


[Related details for case artifacts](../concept/related-details-for-case-artifacts.md)

[Security artifact exclusion and inclusion](../concept/artifact-inclusion-exclusion.md)

[Search for security artifacts](search-for-artifacts.md)

