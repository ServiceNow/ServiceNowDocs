---
title: Service Model Foundation personas
description: Understand the key personas involved in managing and using Service Model Foundation and their responsibilities in supporting business locations and service operations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Service Model Foundation personas

Understand the key personas involved in managing and using Service Model Foundation and their responsibilities in supporting business locations and service operations.

## Understanding Service Model Foundation personas

Service Model Foundation supports collaboration between multiple personas, each playing a distinct role in managing, delivering, and consuming services. Understanding these roles helps administrators assign the right access, responsibilities, and tools within the framework.

Service Model Foundation \(SMF\) supports access based on predefined personas that reflect the type of work users perform within a service organization. Because SMF is industry-agnostic, these personas aren’t tied to specific job titles and can be tailored to match your organization’s needs.

A single user can represent different personas across multiple business locations. For example, a user might act as a Location Manager at one branch and a Contributor at another. SMF models this flexibility through:

-   Roles – Defined at the user level.
-   Responsibilities – Defined according to business location.

The combination of user roles and responsibilities determines what a user can do within each service organization.

## Service Model Foundation user personas and their interactions with different industry verticals

Each following persona represents a different way users interact with business locations and service organizations.

|Persona|Related role|Description|Industry vertical example|
|-------|------------|-----------|-------------------------|
|Bank branch teller|Service organization contributor|A service organization contributor is assigned to a specific service organization and can make requests on behalf of their business location. They can also view any cases submitted by others for their location.|**Banking**: At the local Solana Bank branch, tellers primarily handle customer requests in person that don’t require case filing. Occasionally, they report operational issues or request support for their branch. These team members are service organization contributors.|
|Radiology operations associate|Location agent|A location agent works within a service organization to report issues and manage cases for both B2B and B2C customers at their business location.|**Healthcare**: The operations associate in the radiology department submits requests for patients and the department overall. They also fulfill requests assigned to radiology.|
|In-store customer care associate|Location consumer agent|A location consumer agent focuses specifically on B2C customers, reporting issues and managing cases assigned to their business location. Their role is similar to a location agent, but they're more centered on consumer interactions.|**Retail**: Solana Grocery has an in-store customer care department to assist shoppers. These customer care agents primarily interact with customers rather than working on the shop floor and are modeled as location consumer agents.|
|Hotel manager at a franchise location|Location manager contributor|A location manager contributor manages their business location teams while also submitting requests for issues that arise.|**Hospitality**: The front desk manager oversees daily operations and submits requests for support on behalf of the front desk and guests when needed.|
|College supervisor|Location manager|A location manager can contribute to their business locations, manage the team, and fulfill cases assigned to the location. This role combines the responsibilities of a location manager contributor with active case resolution.|**Higher Education**: The registrar manages a team that assists students with registration. They occasionally request help from other departments and temporarily add student workers to their team. The registrar also fulfills requests from students, professors, and other departments such as financial aid.|
|Inter-departmental support agent|Location support agent|A location support agent is assigned to a specific service organization and focuses on helping other business locations with their requests. They can view details about the organizations requesting support.|**Public Sector**: The Solana City government’s shared services department fulfills requests from other departments, such as IT or purchasing. Staff serving other departments are modeled as location support agents.|
|Regional dealership liaison|Location relationship manager|A location relationship manager is responsible for managing relationships with external business locations. This role is dedicated to supporting third-party locations through a primary internal contact.|**Manufacturing**: Dealerships may be managed by external teams while representing the manufacturer. Solana Cars manufactures vehicles and sells them through a network of dealerships, some company-owned and others managed via dealer groups.|
|Platform configuration admin|Administrator|An administrator doesn't use the application directly, but supports configuration of the service organization, hierarchy management, and assignment of member roles and responsibilities, including related-party configurations.| |

