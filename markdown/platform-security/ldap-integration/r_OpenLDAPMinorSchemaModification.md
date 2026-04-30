---
title: OpenLDAP minor schema modification
description: In OpenLDAP 2.3 systems that use the back-bdb \(Berkley backend\), administrators make a minor modification to their schema to facilitate the integration.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# OpenLDAP minor schema modification

In OpenLDAP 2.3 systems that use the back-bdb \(Berkley backend\), administrators make a minor modification to their schema to facilitate the integration.

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

In OpenLDAP 2.3, back-bdb has limited support for inequality indexing \(ordering\). It is implemented only for generalizedTime and ChangeSequenceNumber syntax. It cannot be supported on syntax that support substrings. Search filters containing inequalities are processed using the presence index.

We recommend creating a custom attribute for this purpose, instead of changing what is already indexed or present in the schema \(for example, **servnowid**\).

