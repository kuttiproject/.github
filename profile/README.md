# About the Kutti Project

The Kutti project aims to create a simple way of creating and managing small Kubernetes clusters for learning and development, using vanilla Kubernetes and open source components only.

The central component of this project is a library called [kuttilib](https://github.com/kuttiproject/kuttilib), which provides the management API.

Kuttilib can be used with one or more _drivers_, each of which allow the creation and management of clusters on an underlying platform. Driver functionality is defined using neutral interfaces in a library called [drivercore](https://github.com/kuttiproject/drivercore). As of now, two implementations exist: a [VirtualBox driver](https://github.com/kuttiproject/driver-vbox) and a [Hyper-V driver](https://github.com/kuttiproject/driver-hyperv).

Finally, an application called [kutti](https://github.com/kuttiproject/kutti) combines kuttilib and drivers, and provides a CLI for managing clusters.

Apart from these main components, the project also includes some add-ons and tools, including:

* [provisioner-localvolume](https://github.com/kuttiproject/provisioner-localvolume), a simple external provisioner that uses the Kubernetes in-tree `local` driver for dynamic volume provisioning.
* [kutti weave](https://github.com/kuttiproject/weave), a fork of the popular Weave Net CNI add-on, which provides container networking and network policies.
