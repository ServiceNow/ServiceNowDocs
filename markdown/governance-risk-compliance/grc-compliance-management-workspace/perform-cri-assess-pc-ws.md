---
title: Perform CRI profile assessment per CRI guidelines using control assessment engine
description: Perform CRI profile assessment based on the tiering questionnaire of an entity to determine the compliance status of the controls and know the compliance score that rolls up to the entity.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage control objectives and policies using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Perform CRI profile assessment per CRI guidelines using control assessment engine

Perform CRI profile assessment based on the tiering questionnaire of an entity to determine the compliance status of the controls and know the compliance score that rolls up to the entity.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst, sn\_compliance\_ws.corporate\_compliance\_manager, sn\_compliance\_ws.it\_compliance\_manager

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  Select the lists \(![List icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\) icon.

3.  Select **All entities** from the Scoping list on the left pane and click the entity record for which you completed the CRI tiering questionnaire.

4.  As an owner of the entity, select the ![More actions icon.](../../../reuse/icons/product-icons/ellipsis-horizontal-outline-24.svg) icon and click the **Initiate CRI profile assessment** option.

    The CRI profile assessment is created based on the tier value, and you can view the assessments in the **CRI profile assessment** related list, which takes a few seconds to be generated. The controls are also created simultaneously.

    **Note:** When the tier assessment is in progress, you will not be able to trigger either tier assessment or CRI profile assessment. When one CRI profile assessment is in the process of creation, then you will not be able to trigger another CRI tier assessment. If one CRI assessment is open, then the tier assessment option is also not visible.

5.  Select the CRI profile assessments related list and refresh the page to view the assessment.

6.  Select the assessment link.

    The assessment is divided into many sections based on the functions of the CSF v2.0 content. You can read the instructions and answer the questions. Each question is mapped to the control objective which in turn maps to the diagnostic statement of the CRI profile. Each of these questions have a multiple choice answers out of which you can choose an answer.

    1.  Select the **View guidance** link

        The text in the link gives more context and guides you in your response to the question that is being asked by providing a response guidance. It gives examples of effective evidence as to what kind of evidence you can attach.

    2.  Write your justification in the **Provide justification for this response** field.

    3.  Select the **Add attachments** button in the **Provide attachments for this response** field.

        Justification and adding attachments are optional, however these are recommended by CRI. The related information on the right pane of the questionnaire gives you more context about the scope, entity, people, requested and due dates of the assessment.

7.  Answer all the questions and select **Submit**.

    After you complete the assessment, based on your responses the corresponding controls reflect the compliance status. The compliance score rolls up to the entity level.

8.  Select the **Downstream controls** related list to view the status of each control if it is Compliant or Non Compliant.

    If non compliant then an issue is generated that you can view in the **Downstream issues** related list. Compliance score is calculated at the entity level, which you can view in the Overview page of the entity.


