# Overview

DRBD is a software-based, shared-nothing, replicated storage solution mirroring the content of block devices (hard disks, partitions, logical volumes etc.) between hosts.  
The DRBD software defined storage (DRBD SDS) solution provides mirrored block devices (logical volumes).

Its DRBD Manage layer creates configuration files for the lower level DRBD Linux kernel driver and manages logical volumes (LVM). Features of DRBD Manage include creating, resizing and removing of replicated volumes.
Additionally, DRBD Manage handles taking snapshots and creating volumes in consistency groups, and creating and deleting snapshots.

This can be used in High-Availability setups as well as high-performance cloud-storage; see the links below for more details.

This charm installs the kernel module and userspace components, and optionally registers the node in an existing DRBDmanage cluster as well.

	---
	
	Describe the intended usage of this charm and anything unique about how this charm relates to others here.
	
	This README will be displayed in the Charm Store, it should be either Markdown or RST. Ideal READMEs include instructions on how to use the charm, expected usage, and charm features that your audience might be interested in. For an example of a well written README check out Hadoop: http://jujucharms.com/charms/precise/hadoop
	
	Use this as a Markdown reference if you need help with the formatting of this README: http://askubuntu.com/editing-help
	
	This charm provides [service](http://example.com). Add a description here of what the service itself actually does.
	
	Also remember to check the [icon guidelines](https://jujucharms.com/docs/stable/authors-charm-icon) so that your charm looks good in the Juju GUI.

# Usage

Please install this charm via the usual

    juju deploy drbdmanage

command line.

## Scale out Usage

If you want to add more nodes to your storage cluster, you might want to read the [Rebalancing data with DRBDmanage](http://www.drbd.org/en/doc/users-guide-90/s-dm-rebalance) section in the Users' Guide.

Alternatively, if you're mostly concerned about performance for each single volume, please read up on our [Optimizing DRBD throughput](http://www.drbd.org/en/doc/users-guide-90/ch-throughput) section - basically, whatever your hardware can give you, DRBD will pass on.

## Known Limitations and Issues

Each DRBD9 resource is limited to 16 copies of the data; that also means that the DRBDmanage control volume can't be more redundant.

The recommendation is to have a few _Control Nodes_ (3 to 5 should be a good number), and to run the other nodes as _Satellites_. See [Types of DRBDmanage nodes](http://www.drbd.org/en/doc/users-guide-90/s-dm-add-node#_types_of_drbdmanage_nodes) in the Users' Guide for more information.

# Configuration

This charm will only install _Satellite_ nodes; when deploying a new cluster you'll need to manually promote a few to _Control Nodes_. In fact, to register newly installed nodes in an existing DRBDmanage cluster, the easiest (manual) way is to have SSH access when installing the charm, because then the installation can do the registration automatically.

# Contact Information

[LINBIT](http://www.linbit.com) provides support for DRBD, DRBDmanage, and the ecosystem around these products.

With a headquarter in Vienna, Austria, an office in Portland, Oregon, and partners all around the world, you can get 24/7 support in every timezone.

## Further Information

- The [LINBIT homepage](https://www.linbit.com/)
- The [DRBD SDS homepage](https://www.drbd.org/)
- The [DRBD9 Users' Guide](https://www.drbd.org/en/doc/users-guide-90/about) is one of the most extensive project documentations in the Open Source world, with (at the last count) more than 170 pages in the A4 PDF format!
- List of LINBIT's [projects on Launchpad](https://launchpad.net/~linbit): [DRBDmanage](https://launchpad.net/drbdmanage), [DRBD 9 kernel module](https://launchpad.net/drbd9), and [DRBD utils (userspace)](https://launchpad.net/drbd-utils)
- The DRBD User Mailing list at drbd-user@lists.linbit.com; [web frontend](http://lists.linbit.com/mailman/listinfo/drbd-user) via mailman
- Performance reports, tips and tricks on the [Blog](https://blogs.linbit.com/)

