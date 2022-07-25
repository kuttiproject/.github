The Kutti project aims to create a simple way of creating and managing small Kubernetes clusters for learning and development, using vanilla Kubernetes and open source components only.

The central component of this project is a library called [kuttilib](https://github.com/kuttiproject/kuttilib), which provides the management API.

Kuttilib can be used with one or more _drivers_, each of which allow the creation and management of clusters on an underlying platform. Driver functionality is defined using neutral interfaces in a library called [drivercore](https://github.com/kuttiproject/drivercore). As of now, two implementations exist:

* [VirtualBox Driver](https://github.com/kuttiproject/driver-vbox)
* [Hyper-V Driver](https://github.com/kuttiproject/driver-hyperv)

Finally, an application called [kutti](https://github.com/kuttiproject/kutti) combines kuttilib and drivers, and provides a CLI for managing clusters.
