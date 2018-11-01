---
title: Resource statuses
seo-title: Resource statuses
description: Resource statuses
seo-description: Discover the different resource statuses.
uuid: 41e36a2d-b9ce-457b-a51c-15e28d3ddc46
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/resource-statuses
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 19.100-0400
cq-lastreplicated: 2018-07-23T05 59 03.665-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
cq-template: /apps/help/templates/article-3
discoiquuid: 08542fed-9dae-4c35-845e-66a2b2304689
firstPublishExternalDate: 2018-07-23T05:59:03.541-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 16.807-0400
jcr-createdby: admin
jcr-description: Resource statuses
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:03.541-0400
lochandoffdate: 2018-07-26T02 53 19.099-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Resource statuses
publishexternaldate: 2018-07-23T05 59 03.541-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/resource-statuses.html
sha1: 51e052fb0d5bf4559cd45269a0559c37e54a80d3
topicBrowsingSortDate: 2018-07-23T05:59:03.541-0400
index: y
internal: n
snippet: y
---

# Resource statuses

Resource statuses

Resources can have different statuses according to their publication or activation status.

There are two columns dedicated to displaying these statuses in the **Custom resources** screen.

![](assets/schema_colonne_1.png)

**Publication statuses**

* **Draft**: the resource has just been created or re-drafted. To create the database tables as well as the corresponding APIs the resource must be republished. If a resource is being re-drafted, it is automatically rendered inactive following the publication step.
* **Pending re-draft**: the resource was re-drafted. The re-draft process will occur during the next publication. Re-drafting is irreversible. Several warning messages warn the user of this fact both when re-drafting, then when preparing to publish.

  >[!NOTE]
  >
  >The **Cancel re-draft** option is available when the resource that you want to re-draft still contains links through other resources with the "Published" status. This option allows you to revert the "re-draft" process. The custom resources will then go back to their original statuses.

* **Published**: the resource has been published. If the resource is modified after the last modified date, then a message appears asking the user to republish in order to take into account the latest modifications.

The **Do not publish latest modifications** field prevents modifications from being taken into account during future publications.

This field can be configured in the custom resource definition.