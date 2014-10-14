# Digital Ocean, Kubernetes CoreOS Deployment - Kelsey Hightower tutorial

This repo is an adaptation of [Kelsey Hightower's great tutoral](https://github.com/kelseyhightower/kubernetes-fleet-tutorial) to build an elastic Kubernetes cluster on top of CoreOS using [Fleet](https://github.com/coreos/fleet) and [flannel](https://github.com/coreos/flannel). This particular use case was built for Digital Ocean, sourced mostly by the /etc/environment and $private_ipv4 variables. The static network config and setup networking units have been removed.

The config and unit files simulate the architecture of the aforementioned tutorial, and I also used the [Digital Ocean guide](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-kubernetes-on-top-of-a-coreos-cluster) heavily for setting up a Kubernetes Cluster on the Digital Ocean platform with private networking configured accordingly. The 

All fleetctl and kubecfg commands were executed from the etcd server. 

The same steps for launching the units apply, along with manually configuring the etcd server IP, and assumes that the KUBERNETES_MASTER variable is created prior to starting the kube-register.service.
