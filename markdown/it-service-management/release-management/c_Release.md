---
title: Using Release Management v2
description: The Release Management v2 plugin \(com.snc.release\_management\_v2\) provides release tables which store information about the planned release and tasks that are required to execute the release.
locale: en-US
release: australia
product: Release Management
classification: release-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Release Management, IT Service Management]
---

# Using Release Management v2

The Release Management v2 plugin \(com.snc.release\_management\_v2\) provides release tables which store information about the planned release and tasks that are required to execute the release.

## Product

Use a Product record in Release Management to store information about a product for reference purposes and groups all the releases and work artifacts for the product.

You can use the **Configuration Items** reference field to link the product with a corresponding CI in the CMDB. Each CI keeps information about how it relates to other CIs, and can track any incidents, problems, or changes related to it. Specifying a CI for the Product connects information from the release process to other processes in the instance.

Defining a product is not mandatory to manage the release process. A release can be an enterprise release in which it is associated with all products or services, or it can be associated to more than one product as well. In either of these cases, defining a product is not mandatory.

Once releases are defined for a product, the Product Hierarchy related link displays the hierarchy of releases, release phases, and release tasks associated with the product.

## Release

Once a product is defined, you can plan and execute a release. Start by defining a release for the product and add child releases or release phases for the release. Then, scope the release by defining work artifacts for the release.

## Release Phase

Define multiple release phases for a release for release governance and smooth execution.

For example, if the release is managed more like a waterfall process, the release phases could be requirement gathering, design, development, testing, build, acceptance, and deployment. For each phase, there can be release tasks associated to it. The phase gets completed as and when all tasks are completed for a phase. Release managers must keep the release phases updated.

If the release is divided into multiple merges, the phases could be merge 1, merge 2, merge 3, and so on. The type and number of phases would depend upon the release management process of your organization.

## Scoping a release

Before starting the release execution, you must define scope of the release. Scope of a release includes the work artifacts such as projects, epics, stories, enhancements, and defects that are a part of the release.

For example, a minor release might only have a few problems and enhancements whereas a major release might have multiple projects or epics associated to it.

**Important:** Starting with the New York release, scoping a release using SDLC or Scrum \(Agile Development 1.0 \(com.snc.sdlc.scrum.pp\)\) is not available.

While scoping the release, you can use the Release Hierarchy related list on the Release Form to view the release as a hierarchy.

-   **[Product hierarchy in Release Management](c_ProductHierarchy.md)**  
A release can be an enterprise release, in which it is associated to all products or services or to more than one product. In either case, defining a product is not required.
-   **[Define a product in Release Management](../task/define-a-product.md)**  
Define a product in the Release Management application to facilitate managing a release process.
-   **[Define a release in Release Management](../task/t_DefineARelease.md)**  
During the release planning process, release managers define the type of the release \(major, minor, and so on.\), schedule of the release \(planned start and end dates\), required phase, phase tasks, and the scope.
-   **[Define a release phase in Release Management](../task/t_DefineAReleasePhase.md)**  
Define a release phase to represent the different stages of work required to complete your release.
-   **[Define scope of a release in Release Management](../task/t_ScopeARelease.md)**  
Add projects, epics, stories, enhancements, and defects to define the scope of a release.

**Parent Topic:**[Release Management](c_ITILReleaseManagement.md)

