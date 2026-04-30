---
title: Amazon Web Services S3 Bucket Out Of Box permissions
description: AWS S3 Bucket OOB catalog items permissions. S3 Bucket supports provision and deprovision only.
locale: en-US
release: yokohama
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Amazon Web Services S3 Bucket Out Of Box Catalog items, Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Amazon Web Services S3 Bucket Out Of Box permissions

AWS S3 Bucket OOB catalog items permissions. S3 Bucket supports provision and deprovision only.

<table id="table_bsw_xy2_hzb"><thead><tr><th>

Catalog item

</th><th>

Services

</th><th>

Permissions

</th></tr></thead><tbody><tr><td rowspan="2">

CSC AWS S3 Bucket

</td><td>

AWS S3 Bucket provision

</td><td>

1.  GetBucketPolicy
2.  PutBucketPublicAccessBlock
3.  GetBucketLifecycle
4.  GetBucketReplication
5.  GetBucketTagging
6.  CreateBucket
7.  GetBucketLogging
8.  GetBucketPublicAccessBlock
9.  GetBucketRequestPayment
10. GetBucketAcl
11. GetBucketWebsite
12. GetAccelerateConfiguration
13. GetBucketVersioning
14. GetBucketEncryption
15. GetBucketCors
16. GetBucketObjectLockConfiguration
17. PutBucketEncryption
18. GetCallerIdentity

</td></tr><tr><td>

AWS S3 Bucket deprovision

</td><td>

1.  DeleteBucketEncryption
2.  DeleteBucketPublicAccessBlock
3.  DeleteBucket
4.  GetBucketObjectLockConfiguration
5.  GetBucketLifecycle
6.  GetBucketEncryption
7.  GetBucketReplication DescribeTable

</td></tr></tbody>
</table>**Parent Topic:**[Amazon Web Services S3 Bucket Out Of Box Catalog items](aws-s3-bucket-out-of-box-catalogs.md)

