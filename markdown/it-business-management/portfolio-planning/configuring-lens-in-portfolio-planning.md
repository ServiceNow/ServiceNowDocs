---
title: Configuring lens in Portfolio Planning
description: Learn about lens structure and pre-defined lenses in Portfolio Planning so that you can configure a lens that represents your company's planning process.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Configuring lens in Portfolio Planning

Learn about lens structure and pre-defined lenses in Portfolio Planning so that you can configure a lens that represents your company's planning process.

## Lens structure

Each lens in Portfolio Planning consists of a structure that is made up of lens entities. These entities represent different levels of planning. Planning managers can build portfolio plans at one of these levels, and create plans for the type of work items that are associated to this lens.

![Lens structure](../images/lens-structure-pp.png "Sample lens structure")

## Pre-defined lenses in Portfolio Planning

Two pre-defined lenses, Organization and Project Portfolio are available.

For example, the Organization lens has Company, Business Unit, and Department as its entities. A department head can create a portfolio plan at the department level, and start to prioritize and roadmap the department's work. This work can be in the form of projects, demands, or any other custom type that is configured.

![Lens structure of the pre-defined Organization, Project Portfolio lenses](../images/lens-structure-predefined-custom-pp.png "Lens structure of pre-defined lens")

In the Portfolio Planning Workspace, planning managers can get started with creating portfolio plans with one of the pre-defined lenses.

## Planning items for a lens

For every portfolio plan that is built using a lens, only those item types that are included with that lens are available for planning. For example, a lens XYZ has just demands added to it. Then, in any portfolio plan that is built using the XYZ lens, work can be planned in the form of demands only.

## Configuring lens and lens structure

You can either use a pre-defined lens as it is or update its existing configuration.

-   To use the lens as it is, complete your lens setup by configuring integration with a ServiceNow Project Portfolio Management.

    See [Configuring Portfolio Planning with PPM](configuring-portfolio-planning-with-ppm.md).

-   To update the lens configuration:
    -   Change the planning items included within the lens. See [Lens Form](../reference/lens-form-portfolio-planning.md).
    -   Add more entities to the lens structure. See [Modify lens structure in Portfolio Planning](../task/modify-lens-portfolio-planning.md).

