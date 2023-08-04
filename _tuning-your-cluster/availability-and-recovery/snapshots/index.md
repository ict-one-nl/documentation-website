---
layout: default
title: Snapshots
nav_order: 5
has_children: true
parent: Availability and recovery
redirect_from: 
  - /opensearch/snapshots/
  - /opensearch/snapshots/index/
has_toc: false
---

# Snapshots

Snapshots are backups of a cluster's indexes and state. State includes cluster settings, node information, index metadata (mappings, settings, or templates), and shard allocation.

Snapshots have three main uses:

- **Recovering from failure**

  For example, if cluster health goes red, you might restore the red indexes from a snapshot.

- **Migrating from one cluster to another**

  For example, if you're moving from a proof-of-concept to a production cluster, you might take a snapshot of the former and restore it on the latter.

- **Make use of searchable snapshots to save on storage/compute costs**

  For example, if you have a high volume of data that is too expensive to retain on fast storage. You can store the data in a snapshots repository based on cheap storage while still being able to search through it.


You can take and restore snapshots using the [snapshot API]({{site.url}}{{site.baseurl}}/opensearch/snapshots/snapshot-restore/). 

If you need to automate snapshot creation, you can use the [snapshot management]({{site.url}}{{site.baseurl}}/opensearch/snapshots/snapshot-management/) feature.
