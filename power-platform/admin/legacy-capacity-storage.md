---
title: "Legacy storage capacity  | MicrosoftDocs"
description: About the legacy storage model.
ms.date: 04/17/2020
ms.reviewer: ""
ms.service: "power-platform"
ms.topic: "quickstart"
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - PowerApps
  - Powerplatform
---
# Legacy storage capacity

In April 2019, we introduced Common Data Service capacity storage that is optimized for relational data, attachments, and audit logs. If you purchased storage prior to April 2019, you are using the legacy licensing model for storage discussed in this topic.

We're rolling out this feature now so check back if your user experience varies from the following content.

## Licenses for the legacy storage model

The following licenses provide capacity using the legacy storage model. If you have any of the following licenses and none of the new model licenses, you'll see the legacy model report: 

- Microsoft Dynamics CRM Online Additional Non-production Instance 
- Microsoft Dynamics CRM Online Additional Test Instance 
- Microsoft Dynamics CRM Online Instance 
- Microsoft Dynamics CRM Online Storage Add-On 

To see whether you have any of these licenses, sign in to the Microsoft 365 admin center, and then go to **Billing** > **Products & Services**.

> [!NOTE]
> If you have a mix of the abovementioned legacy model licenses and [new model licenses](capacity-storage.md#licenses-for-the-new-storage-model), you'll see the [new model report](capacity-storage.md).
> 
> If you have none of the abovementioned legacy model licenses nor the [new model licenses](capacity-storage.md#licenses-for-the-new-storage-model), you'll see the [new model report](capacity-storage.md).

## Verifying your legacy storage model

1. Sign in to the Power Platform admin center, and then select an environment. 

2. Select **Analytics** > **Capacity**.

3. View the data on the **Summary** page.

The legacy licensing storage model looks like the following image.

> [!div class="mx-imgBorder"] 
> ![Legacy licensing storage model](media/capacity-old-license-model.png "Legacy licensing storage model")

The report displays available storage capacity by source in addition to overall storage capacity usage. To help customers transition to the new licensing model, current usage is also shown by database, file, and log capacity.

## Capacity page details

> [!NOTE]
> The calculation of storage capacity usage in the legacy licensing model consists of all three storage types&mdash;database, file, and log&mdash;however, it's displayed as one overall storage number.

### Summary tab

This page provides a tenant-level view of where your organization is using storage capacity.

To view the **Summary** page, select **Analytics** > **Capacity** > **Summary**.

> [!div class="mx-imgBorder"] 
> ![Capacity storage details](media/capacity-old-license-model-explained.png "Capacity storage details")

|  | |
|---------|---------|
|(1)   |**Storage capacity usage**  <ul><li>**File and database**: The following entities store data in file and database storage: <ul><li>Attachment</li><li>AnnotationBase</li><li>Any custom or out-of-the-box entity that has fields of datatype file or image (full size)</li></ul></li><li>**Log**: The following entities are used: <ul><li>AuditBase</li><li>PlugInTraceLogBase</li></ul><li>**Database only**: All other entities are counted for your database</li></ul> |
|(2)    |**Storage capacity, by source** <ul><li>**Org (tenant) default**: The default capacity given at the time of sign-up </li><li>**User licenses**: Additional capacity added for every user license purchased</li><li>**Additional storage**: Any additional storage you bought </li><li>**Total**: Total storage available </li><li>**View self-service sources**: See [View self-service license amounts and storage capacity](view-self-service-capacity.md)</li></ul>      |
|(3)     |**Top storage usage, by environment**: The environments that consume the most capacity        |

### Storage capacity tab

This page provides similar information as the **Summary** tab, but with an environment-level view of where your organization is using capacity.

To view the **Storage capacity** page, select **Analytics** > **Capacity** > **Storage capacity**. See the next section for using the **Details** button (![Details button](media/storage-data-details-button.png "Details button")) to see environment capacity analytics.

> [!div class="mx-imgBorder"] 
> ![Storage capacity tab](media/capacity-old-license-model-storage-tab.png "Storage capacity tab")


> [!NOTE]
> - The following environments don't count against capacity and are shown as 0 GB:
>   - Trial 
>   - Preview
>   - Support
>   - Developer
> - You can select an environment that's showing 0 GB, and then go to its **Environment Analytics** page to see the actual consumption.

### Environment capacity analytics

This page provides an environment-level detailed view of where your organization is using capacity, in addition to the three types of capacity consumption. 

**To view environment-level capacity analytics**

1. Select **Analytics** > **Capacity** > **Storage capacity**.
2. Select an environment.
3. Select **Details** (![Details button](media/storage-data-details-button.png "Details button")).

> [!div class="mx-imgBorder"] 
> ![Environment capacity analytics](media/capacity-old-license-model-storage-details.png "Environment capacity analytics")

The following details are provided:

- Actual database usage
- Top database tables and their growth over time
- Actual file usage
- Top files tables and their growth over time
- Actual log usage
- Top tables and their growth over time

## Example storage capacity scenario

### Scenario: Storage is over capacity

|Type  |Entitled  |Consumed  |
|---------|---------|---------|
|**Database**     | 100 GB        | 110 GB        |

This tenant is 10 GB over in storage usage. Therefore, there is a deficit. This tenant should free up storage or purchase more capacity.

## Actions to take for a storage capacity deficit

You can always [free up storage](free-storage-space.md), [delete unwanted environments](delete-environment.md), or buy more capacity to be compliant with storage usage. To learn more about capacity add-ons, see the [Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/p/?LinkId=866544) or the ["Add-ons" section of the Power Apps and Power Automate Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130). You can work through your organization's standard procurement process to purchase capacity add-ons.

## FAQ

### I have available instances (production and sandbox), but my capacity usage is more than my capacity entitlement. Will I be able to provision new environments? 

Provisioning a new environment requires that you not be delinquent in storage capacity. If you have at least 1 GB of available storage capacity, you can provision environments to align with your available instances.

### I have storage licenses from the legacy licensing model, and I also purchased new model storage licenses. Which report will I see?

You'll see the report for the [new licensing model](capacity-storage.md). 

### Do I get notified through email when my org is over capacity?

When you sign in to the Power Platform admin center, you'll be notified if your capacity usage is more than the capacity you're entitled to. 

### See also

[Common Data Service storage capacity](capacity-storage.md) <br />
[What's new in storage](whats-new-storage.md) <br />
[Free up storage space](free-storage-space.md) <br />
[Capacity add-ons](capacity-add-on.md)

