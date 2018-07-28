---
title: HDFS(Hadoop Distributed File System)
layout: page
comments: true
social-share: true
show-avatar: true
---

Hadoop’s architecture O.X and 1.X

**NameNode**

• **Master** of HDFS, directs the slave DataNode daemons to perform low-level I/O tasks

• Keeps track of file splitting into blocks, replication, block location, etc.

* **Secondary NameNode**: takes snapshots of the NameNode.

* **DataNode**: each slave machine hosts a DataNode daemon.

**NameNodes and DataNodes**

![namenodes_datanodes](/datanodes_namenodes.png){:class="img-responsive"}

**Hadoop Cluster Topology**

![hadoop_cluster](/hadoop_cluster.png){:class="img-responsive"}