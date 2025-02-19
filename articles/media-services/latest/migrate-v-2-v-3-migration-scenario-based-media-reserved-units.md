---
title: Media Reserved Units (MRUs) migration guidance
description: This article gives you MRU scenario based guidance that will assist you in migrating from Azure Media Services V2 to V3.
services: media-services
author: jiayali-ms
manager: femila
ms.service: media-services
ms.topic: conceptual
ms.workload: media
ms.date: 08/25/2021
ms.author: inhenkel
---

# Media reserved units migration guidance

![migration guide logo](./media/migration-guide/azure-media-services-logo-migration-guide.svg)

<hr color="#5ea0ef" size="10">

![migration steps 2](./media/migration-guide/steps-4.svg)

This article gives you MRU scenario based guidance that will assist you in migrating from Azure Media Services V2 to V3.

> [!Important]
> Media reserved units are no longer needed for any Media services account as the system will automatically scale up and down based on load. 

## Scenario guidance

Please migrate your MRUs based on the following scenarios:

* For all Media Services accounts, you no longer are required to set Media Reserved Units (MRUs). The system will now automatically scale up and down based on load.
* If you have an account that was created before the 2020-05-01 (or later) version of the API, you can still Have access to API’s for managing MRU’s, however none of the MRU configuration that you set will be used to control encoding concurrency or performance. For more information, see [Scaling Media Processing](../previous/media-services-scale-media-processing-overview.md). You can manage the MRUs using CLI 2.0 for Media Services V3, or using the Azure portal.
* If you don't see the option to manage MRUs in the Azure portal, you're running an account that was created with the 2020-05-01 API or later.
* If you are familiar with setting your MRU type to S3, your performance will improve or remain the same with the removal with MRUs.
* If you are an existing V2 customer, you need to create a new V3 account to support your existing application prior to the completion of  migration. 
* Indexer V1 or other media processors that are not fully deprecated yet may need to be enabled again. 

For more information about MRUs, see [Media Reserved Units](concept-media-reserved-units.md) and [How to scale media reserved units](media-reserved-units-how-to.md).

## MRU concepts, tutorials and how to guides

### Concepts

[Media Reserved Units](concept-media-reserved-units.md)

### How to guides

[How to scale media reserved units](media-reserved-units-how-to.md)

## Samples

You can also [compare the V2 and V3 code in the code samples](migrate-v-2-v-3-migration-samples.md).
