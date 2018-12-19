---
copyright:
  years: 2017,2018
lastupdated: "2018-10-11"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}

# Activity Tracker Integration

{{site.data.keyword.databases-for-etcd_full}} is integrated with  [Activity Tracker](https://{DomainName}/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov), so you can view service-level events.

In order to see the events, you need to [provision the Activity Tracker service](https://{DomainName}/docs/services/cloud-activity-tracker/how-to/provision.html#provision) from the [{{site.data.keyword.cloud_notm}}  catalog](https://{DomainName}/catalog/services/activity-tracker). Activity Tracker has a _Lite_ plan available at no additional cost.

Once you have the Activity Tracker service, the {{site.data.keyword.databases-for-etcd}} events appear under _Account Logs_ from the _View Logs_ dropdown menu. 

In addition to the Activity Tracker UI, the Kibana dashboard is also available at https://logging.ng.bluemix.net.
{: .tip}

## Event Fields
A description of the common fields for an Activity Tracker event is on the [Activity Tracker event fields](https://{DomainName}/docs/services/cloud-activity-tracker/at_event.html#at_event) page.

## List of Events

The table lists the events that get sent to Activity Tracker from {{site.data.keyword.databases-for-etcd}}.

Action|Description
-------|-------
`databases-for-etcd.backup.create`|A backup of your deployment was created. If the backup failed, a "-failure" flag is included in the message.
`databases-for-etcd.user-password.update`|A user's password was updated. A "-failure" flag is included in the message if the attempt to update a user's password failed.
`databases-for-etcd.user.create`|A user was created. A "-failure" flag is included in the message if the attempt to create a user failed.
`databases-for-etcd.user.delete`|A user was deleted. A "-failure" flag is included in the message if the attempt to delete a user failed.
`databases-for-etcd.backup.restore`|A restore from backup was created. If the attempted restore failed, a "-failure" flag is included in the message.
`databases-for-etcd.resources.scale`|A scaling operation was performed. If the scaling operation failed, a "-failure" flag is included in the message.
`databases-for-etcd.whitelisted-ips-list.update`|The whitelist was modified. A "-failure" flag is included in the message if the attempt to modify the whitelist failed.
{: caption="Table 1. List of Events and Event Descriptions" caption-side="top"}
