# SMB CSI Driver for Kubernetes
![linux build status](https://github.com/kubernetes-csi/csi-driver-smb/actions/workflows/linux.yaml/badge.svg)
![windows build status](https://github.com/kubernetes-csi/csi-driver-smb/actions/workflows/windows.yaml/badge.svg)
[![Coverage Status](https://coveralls.io/repos/github/kubernetes-csi/csi-driver-smb/badge.svg?branch=master)](https://coveralls.io/github/kubernetes-csi/csi-driver-smb?branch=master)

### About
This driver allows Kubernetes to access [SMB](https://wiki.wireshark.org/SMB) server on both Linux and Windows nodes, csi plugin name: `smb.csi.k8s.io`. The driver requires existing and already configured SMB server, it supports dynamic provisioning of Persistent Volumes via Persistent Volume Claims by creating a new sub directory under SMB server.

### Project status: GA

### Container Images & Kubernetes Compatibility:
|Driver Version | supported k8s version | supported [Windows csi-proxy](https://github.com/kubernetes-csi/csi-proxy) version |
|---------------|-----------------------|-------------------------------------|
|master branch  | 1.20+                 | v0.2.2+                             |
|v1.5.0         | 1.19+                 | v0.2.2+                             |
|v1.4.0         | 1.19+                 | v0.2.2+                             |
|v1.3.0         | 1.18+                 | v0.2.2+                             |

### Driver parameters
Please refer to [`smb.csi.k8s.io` driver parameters](./docs/driver-parameters.md)

### Install driver on a Kubernetes cluster
 - install by [kubectl](./docs/install-smb-csi-driver.md)
 - install by [helm charts](./charts)
 
### Examples
 - [Set up a Samba Server on a Kubernetes cluster](./deploy/example/smb-provisioner/)
 - [Basic usage](./deploy/example/e2e_usage.md)
 - [Windows](./deploy/example/windows)

### Troubleshooting
 - [CSI driver troubleshooting guide](./docs/csi-debug.md) 

## Kubernetes Development
Please refer to [development guide](./docs/csi-dev.md)

### View CI Results
Check testgrid [sig-storage-csi-smb](https://testgrid.k8s.io/sig-storage-csi-other) dashboard.

### Links
 - [SMB FlexVolume driver](https://github.com/Azure/kubernetes-volume-drivers/tree/master/flexvolume/smb)
 - [Kubernetes CSI Documentation](https://kubernetes-csi.github.io/docs/)
 - [CSI Drivers](https://github.com/kubernetes-csi/drivers)
 - [Container Storage Interface (CSI) Specification](https://github.com/container-storage-interface/spec)
