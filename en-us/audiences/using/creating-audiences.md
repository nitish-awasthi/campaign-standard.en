---
title: Creating audiences
seo-title: Creating audiences
description: Creating audiences
seo-description: Learn how to create audiences in Adobe Campaign.
uuid: 867252b5-5d0d-44e8-aebb-048a1486a3ef
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/creating-audiences
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 13.574-0400
cq-lastreplicated: 2018-07-23T05 55 25.569-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
cq-template: /apps/help/templates/article-3
discoiquuid: fec45b4c-b446-4d5e-b16e-59cb9c4fd8ac
firstPublishExternalDate: 2018-07-23T05:55:25.491-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 46.243-0400
jcr-createdby: admin
jcr-description: Creating audiences
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:55:25.491-0400
lochandoffdate: 2018-07-25T09 29 13.573-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Creating audiences
publishexternaldate: 2018-07-23T05 55 25.491-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/audiences/using/creating-audiences.html
sha1: 6b6d083c1e9c4b926f38120250079d106a82e632
topicBrowsingSortDate: 2018-07-23T05:55:25.491-0400
index: y
internal: n
snippet: y
---

# Creating audiences

Creating audiences

## <p>Creating query audiences</p>

This section describes how to create a **Query** audience. You can also create audiences from importing a file or targeting in a [workflow](../../automating/using/discovering-workflows.md).

From the audience list, you can create audiences by performing queries or importing an Adobe Experience Cloud audience.

1. Go to the audience list via the **Audiences** tab or card.

   ![](assets/audiences_query_1.png)

1. Select **Create** to access the screen to create a new audience.

   ![](assets/audiences_query.png)

1. Name your audience. The audience label is used in the list of audiences and in the palette of the query tool.
1. Choose a **Query** audience type: the audiences defined by a query are recomputed at each further use.

   ![](assets/audience_type_selection.png)

1. Then select the **Targeting dimension** that you would like to use to filter your customers. Each audience is made up of a single targeting dimension. For example, you cannot create an audience made up of both profiles, test profiles and subscribers. For more on targeting dimensions, refer to [this page](../../automating/using/query.md#targeting-dimensions-and-resources). 
1. Create the query to define the audience population. Refer to the section on [editing queries](../../automating/using/editing-queries.md).
1. Click the **Create** button to save your audience.

>[!NOTE]
>
>You can add a description to this audience and define the access authorizations via the **Edit properties** icon.

## <p>Creating list audiences</p>

This section describes how to create a **List** audience after targeting in a workflow. You can also create audiences by importing a file into a [workflow](../../automating/using/discovering-workflows.md) or via a query from the **Audiences** menu.

To create a **List** audience, the steps are as follows:

1. In the **Marketing activities** tab, click **Create** then select **Workflow**.

   ![](assets/audiences_list_1.png)

1. Drag and drop, and then configure the targeting activities which will allow you to select a population that has a **known** dimension. The list of available activities and their configuration are detailed in the [Targeting activities](../../automating/using/about-targeting-activities.md) section.

   You can use a **Query** activity, or import data using a **Load file** activity before using a **Reconciliation** activity to identify the dimension of the data imported. Here, we want to target recipients who subscribed to the Sport Newsletter with a **Query** activity .

   ![](assets/audiences_list_2.png)

1. After your targeting, drag and drop a **Save audience** activity into your workflow. For example, you can chose to **Create or update an audience**, this allows you to create then automatically update your audience with new data. In this case, add a **Scheduler** activity at the beginning of your workflow.

   For more information on configuring this activity, refer to the [Save audience](../../automating/using/save-audience.md) section.

   ![](assets/audiences_list_3.png)

1. Save and start the workflow.

   As the **Save audience** is placed after a targeting with a known dimension, the audiences created via this activity are **List** audiences.

   The content of the saved audience is then available in the audience's detailed view that can be accessed via the list of audiences. The columns available from this view correspond to the columns of the inbound transition of the workflow's save activity. For example: the columns of the file imported, the additional data added from a query.

   ![](assets/audiences_list_4.png)

## <p>Creating file audiences</p>

This section details how to create a **File** audience by importing a file into a workflow. You can also create audiences from a targeting activity in a [workflow](../../automating/using/discovering-workflows.md) or via a query from the **Audiences** menu.

To create a **File** audience, the steps are as follows:

1. In the **Marketing activities** tab, click **Create** then select **Workflow**.
1. Drag and drop, and then configure a **Load file** activity which will allow you to import a population that has an **unknown** dimension when the workflow is executed. For more information on configuring this activity, refer to the [Load file](../../automating/using/load-file.md) section.

   ![](assets/audience_files_1.png)

1. Drag and drop a **Save audience** activity after the **Load file** activity. For more information on configuring this activity, refer to the [Save audience](../../automating/using/save-audience.md) section.
1. Save and start the workflow.

   ![](assets/audience_files_2.png)

   As the **Save audience** is placed after an import, the data dimension is unknown and the audiences created via this activity are **File** audiences.

   The content of the saved audience is then available in the audience's detailed view that can be accessed via the list of audiences. The columns available from this view correspond to the columns of the inbound transition of the workflow's save activity. For example: the columns of the imported file, the additional data added from a query.

   ![](assets/audience_files_3.png)

## <p>Creating Experience Cloud audiences</p>

Adobe Campaign allows you to share and exchange audiences with Adobe Experience Cloud. Creating and managing audiences is detailed in the [Importing/Exporting audiences with People core service](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md) section.

## <p>Editing audiences</p>

There are different ways to edit an audience depending on the audience type:

* To edit a **Query** audience, go to the list of audiences via the **Audiences** menu, or the **Audiences** card from the Adobe Campaign home page.

  Open the relevant audience. All of the elements of a previously created audience can be edited.

  >[!CAUTION]
  >
  >If you change the **Filtering dimension** in the query, the rules that have previously been defined will be lost.

* To edit a **List** or **File** audience, edit the workflow from which it was created and modify the **Save audience** activity. Start the workflow so that the audience is modified.
* To edit an **Experience Cloud** audience, refer to the [Importing/Exporting audiences with People core service](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md) section.
