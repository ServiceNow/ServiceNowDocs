---
title: IP address field type
description: The IP Address \(Validated IPV4, IPV6\) \[ip\_addr\] field type stores valid IPv4 and IPv6 addresses.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# IP address field type

The **IP Address \(Validated IPV4, IPV6\)** \[ip\_addr\] field type stores valid IPv4 and IPv6 addresses.

## Support for IPv4 and IPv6

Standard dot-decimal notation is supported for IPv4 and standard hex notation is supported for IPv6. For IPv6, you can use canonical notation to compress zeros. Familiarize yourself with [IETF RFC5952](https://tools.ietf.org/html/rfc5952) for examples and guidelines on text representation for IPv6 addresses.

The following are examples of valid IP addresses:

-   **A standard IPv4 address in dot-decimal notation**:

    `10.34.51.20`

-   **An expanded IPv4 address would be zero padded**:

    `10.1.10.210` would be represented as `010.001.010.210`

-   **An IPv6 address in fully expanded notation**:

    `1507:f0d0:1002:0051:0000:0000:0000:0004`

-   **The same IPv6 address above using the canonical notation**:

    `1507:f0d0:1002:51::4`


## How IP addresses are stored in the database

The IP address `ip_addr` field is a Variable Character \(VARCHAR\) field with a length of 40 characters. The values are normally stored in standard \(dot-decimal or canonical\) notation for both IPv4 and IPv6 addresses regardless of the notation you use when you input values in the field.

For example, if you enter an IPv6 address in a non-canonical format \(expanded or any other valid formats per [IETF RFC5952](https://tools.ietf.org/html/rfc5952)\), by default, the system will store it in canonical format unless an IP Data Control attribute value is defined on that column with a different address format. See the \[ip\_data\_control\] glide attribute section in [Altering tables and fields using dictionary attributes](../concept/c_DictionaryAttributes.md) for more details.

## Support for data migration

Provide support in migrating IP addresses stored as string fields to the new **IP Address\(Validated IPV4,IPV6\)** type. The new IP address type accepts only a valid IP address. The existing data is formatted according to the ip\_data\_control attribute. The ip\_data\_control attriute can be set to exactly one of the following four values:

-   **canonical**: Incoming IP addresses are validated and canonicalized before they are entered in the database. Invalid IP addresses are rejected.
-   **canonicalize\_when\_possible**: Valid IP addresses are canonicalized before before being entered in to the database. Invalid IP addresses are also entered in to the database without being changed.

    **Note:** **canonicalize\_when\_possible** is the default value for the ip\_data\_control attribute, unless it's otherwise specified.

-   **expanded**: The IP addresses are validated and stored in an expanded form to support efficient database range queries. Invalid IP addresses are rejected.
-   **none**: No validation or normalization is performed in this value type. It is used only as an emergency mechanism as it essentially reverts this type to a plain string field.

