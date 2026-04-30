---
title: AbstractReconciler - Global
description: The AbstractReconciler script include provides methods to use as a base class to create your own Discovery reconciler.Determines if the newly discovered data is different than the data already in the database for the current item.Gets the string value of the field to be used as a key to look up a record in the newly discovered data.Returns true if the newly discovered data is different than the data already in the database for this item.Marks CIs as absent by setting the install status to "Absent"; other tables are marked by setting the \(presumed present\) field "absent" to true.Marks CIs as present by setting the install status to "Installed"; other tables are marked by setting the \(presumed present\) field "absent" to false.Reconciles the newly discovered data with the data already present in the database and resolves references to previously reconciled data.Reads the current memory table record of newly discovered data and checks its validity.Reads the current memory table record of newly discovered data and checks its validity.Reads the fields in the current database record into instance member fields.Sets the database fields for the current record to the values in the newly discovered information.Optional override for concrete subclasses that require special setup.Optional method to override in concrete subclasses that need to resolve reference fields.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# AbstractReconciler- Global

The AbstractReconciler script include provides methods to use as a base class to create your own Discovery reconciler.

This is an abstract base class for reconciling newly discovered data in an XMLMemoryTable to a related list in the database. The AbstractReconciler script include implements the common logic and helper methods for reconciling related lists for a particular CMDB item against discovered information present in a MemoryTable instance.

Most of this logic is very straightforward, but one bit may not be: the resolution of references to previously reconciled records. This feature works by collecting information while reconciling one related list, then passing that information on to the reconciler for another related list. For example, while switch partitions are being reconciled, information is gathered \(in a map instance\) that maps an interface number for a partition to the sys\_id of the partition's record in the partition table. Then later when the switchports are being reconciled, a reference to the switch partition that contains the switchport can be resolved by using this map.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## AbstractReconciler - getReconciliationField\(\)

Determines if the newly discovered data is different than the data already in the database for the current item.

This method is only invoked for items that have been rediscovered.

Mandatory method, must be overridden in all concrete subclasses.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the data has changed.|

## AbstractReconciler - getReconciliationKey\(\)

Gets the string value of the field to be used as a key to look up a record in the newly discovered data.

This value will be used to attempt to find a record in the discovered data, using the column returned by the getReconciliationKey\(\) method.

Mandatory method, must be overridden in all concrete subclasses.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value to use as a key into the discovered data.|

## AbstractReconciler - hasChanged\(\)

Returns true if the newly discovered data is different than the data already in the database for this item.

This method is only invoked for items that have been rediscovered.

Mandatory method, must be overridden in all concrete subclasses.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the discovered data is different than the data already in the database.|

## AbstractReconciler - markAbsent\(\)

Marks CIs as absent by setting the install status to "Absent"; other tables are marked by setting the \(presumed present\) field "absent" to true.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## AbstractReconciler - markPresent\(\)

Marks CIs as present by setting the install status to "Installed"; other tables are marked by setting the \(presumed present\) field "absent" to false.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## AbstractReconciler - process\(\)

Reconciles the newly discovered data with the data already present in the database and resolves references to previously reconciled data.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## AbstractReconciler - readDatabaseFields\(\)

Reads the current memory table record of newly discovered data and checks its validity.

Mandatory method, must be overridden in all concrete subclasses.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the data is valid.|

## AbstractReconciler - readDiscovered\(\)

Reads the current memory table record of newly discovered data and checks its validity.

Mandatory method, must be overridden in all concrete subclasses.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the data is valid.|

## AbstractReconciler - resolveReferenceFields\(\)

Reads the fields in the current database record into instance member fields.

Mandatory method, must be overridden in all concrete subclasses.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## AbstractReconciler - setDatabaseFields\(\)

Sets the database fields for the current record to the values in the newly discovered information.

This method is invoked both for new database records and for existing database records when the discovered data has changed.

Mandatory method, must be overridden in all concrete subclasses.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## AbstractReconciler - setup\(\)

Optional override for concrete subclasses that require special setup.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## AbstractReconciler - track\(String sys\_id\)

Optional method to override in concrete subclasses that need to resolve reference fields.

This method is invoked after valid discovered data is read. Generally implementations will use some of this discovered data as a key into a map \(passed into the concrete reconciler class when it was instantiated\) that will return the sys\_id of the database record holding the referenced information. However, implementations are not required to use this approach.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|The sys\_id of the current database record.|

|Type|Description|
|----|-----------|
|void| |

