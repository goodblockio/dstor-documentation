---
description: This page explains node requirements.
---

# Node Operator Requirements

#### Processor

Intel i5 dual core @ 3.2Ghz or better.\
Operators may be able to use a lesser system, but it is not recommended.

#### Operating System

Ubuntu Linux version 18.04 LTS or later LTS version.

#### Memory

8GB RAM. More is better.

#### Network

NAT-ed IPv4 is acceptable for basic needs. A public IPv4 address assigned to a local interface is needed if you want to resolve IPv4 requests for dStor too.

#### Storage

Minimum 4TB of hard drive space. More is better. Partitions must be empty and mounted somewhere that is reboot proof. XFS is recommended, however ZFS, EXT4 and other file systems should be ok.

#### Cache Partition

The cache partition must be 20% in size of the data partition (or more) and its mount point final subpath must end in cache. Example:&#x20;

`_mnt_dstor/outpost-cache OR /cache`
