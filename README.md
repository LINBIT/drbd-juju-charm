# Overview

DRBD is a software-based, shared-nothing, replicated storage solution mirroring the content of block devices (hard disks, partitions, logical volumes etc.) between hosts.  

DRBDmanage is an abstraction layer which takes over management of logical volumes (LVM) and management of configuration files for DRBD. Features of DRBDmanage include creating, resizing, and removing of replicated volumes. Additionally, DRBDmanage handles taking snapshots and creating volumes in consistency groups.


---

Describe the intended usage of this charm and anything unique about how this charm relates to others here.

This README will be displayed in the Charm Store, it should be either Markdown or RST. Ideal READMEs include instructions on how to use the charm, expected usage, and charm features that your audience might be interested in. For an example of a well written README check out Hadoop: http://jujucharms.com/charms/precise/hadoop

Use this as a Markdown reference if you need help with the formatting of this README: http://askubuntu.com/editing-help

This charm provides [service](http://example.com). Add a description here of what the service itself actually does.

Also remember to check the [icon guidelines](https://jujucharms.com/docs/stable/authors-charm-icon) so that your charm looks good in the Juju GUI.

# Usage

Step by step instructions on using the charm:

    juju deploy servicename

and so on. If you're providing a web service or something that the end user needs to go to, tell them here, especially if you're deploying a service that might listen to a non-default port.

You can then browse to http://ip-address to configure the service.

## Scale out Usage

If the charm has any recommendations for running at scale, outline them in examples here. For example if you have a memcached relation that improves performance, mention it here.

## Known Limitations and Issues

This not only helps users but gives people a place to start if they want to help you add features to your charm.

# Configuration

The configuration options will be listed on the charm store, however If you're making assumptions or opinionated decisions in the charm (like setting a default administrator password), you should detail that here so the user knows how to change it immediately, etc.

# Contact Information

LINBIT (http://www.linbit.com) provides support for DRBD, DRBDmanage, and the ecosystem around these products.

With the headquarter in Vienna, Austria, an office in Portland, Oregon, and partners all around the world you can get 24/7 support in every timezone.

## Further Information for DRBD and DRBDmanage

- LINBIT homepage: http://www.linbit.com/
- DRBD (9) Users' Guide: http://www.drbd.org/en/doc/users-guide-90/about
- https://launchpad.net/drbdmanage (and https://launchpad.net/drbd9, and https://launchpad.net/drbd-utils)
- DRBD User Mailing list at drbd-user@lists.linbit.com; web frontend at http://lists.linbit.com/mailman/listinfo/drbd-user
