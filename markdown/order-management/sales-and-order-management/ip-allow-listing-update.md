---
title: IP allow-listing update
description: To better support our growing needs and increase capacity, we have expanded the pool of outbound addresses used for requests from CPQ.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# IP allow-listing update

To better support our growing needs and increase capacity, we have expanded the pool of outbound addresses used for requests from CPQ.

**Important:** This change is relevant only if you use allow-listing to control which external systems can communicate with your integration servers. If you rely on allow-listing, it is important to update your configuration to include the new addresses listed below. This will help ensure that your integration calls from CPQ continue to function smoothly and without interruption.

-   **Inbound production \(prod01.logik.io\)**
    -   35.224.151.71
    -   34.83.141.224
-   **Outbound production \(prod01.logik.io\)**
    -   34.72.98.104
    -   104.198.22.182
    -   35.238.218.128
    -   35.233.220.207
    -   35.222.102.215\(new\)
-   **Inbound non-production \(test.logik.io\)**

    Inbound:34.135.130.9

-   **Oubound non-production \(test.logik.io\)**
    -   34.68.236.64
    -   34.30.162.13
    -   35.226.98.108
    -   34.121.127.94\(new\)
    -   34.29.158.138\(new\)

## Aug 1, 2025 Test Sector Update

While performing testing for a large data migration, we had a large increase in outbound IPs. These are dynamically assigned currently, but on Friday, Aug 22, 2025, we changed to a much smaller static list in Test.

The following are the new additions:

-   34.10.0.135
-   34.10.242.143
-   34.122.88.68
-   34.123.63.250
-   34.134.181.254
-   34.135.82.144
-   34.136.119.129
-   34.171.226.19
-   34.173.198.250
-   34.28.193.204
-   34.28.74.81
-   34.29.158.138
-   34.44.124.55
-   34.44.76.215
-   34.46.254.151
-   34.55.149.73
-   34.55.173.230
-   34.55.91.85
-   34.56.58.123
-   34.58.152.142
-   34.58.72.106
-   34.60.204.253
-   34.63.178.255
-   34.63.29.27
-   34.66.102.79
-   34.66.181.238
-   34.66.55.102
-   34.67.116.134
-   34.72.83.158
-   34.9.93.234
-   35.188.84.55
-   35.223.33.177
-   35.226.103.168
-   35.232.208.89
-   35.238.247.112
-   35.239.113.70

The following are the IPs recently introduced:

-   35.226.81.113
-   35.238.9.191
-   34.27.254.59
-   35.222.207.50
-   34.29.115.14

