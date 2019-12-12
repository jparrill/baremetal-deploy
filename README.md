# OpenShift Baremetal Deploy

This repository is intended to store resources and deployment artifacts
for [bare metal](https://github.com/metal3-io/metal3-docs/blob/master/design/bare-metal-style-guide.md)
OpenShift KNI clusters (currently OpenShift 4.3)

It also contains optional features focused on low-latency workloads, NFV workloads, etc.

## Installation artifacts

* [Installation Steps](install-steps.md)
* [Using Baremetal-prep.sh](baremetal-prep.md)
* [E2E Feature Tests](features/e2e_tests/README.md)

## Optional features

* [CPU Manager](features/cpumanager/). CPU Manager manages groups of CPUs and constrains workloads
to specific CPUs.
* [PTP](features/ptp). This operator manages cluster wide Precision Time Protocol (PTP) configuration.
* [SCTP](features/sctp). These assets enables Stream Control Transmission Protocol (SCTP) in the RHCOS
worker nodes.
* [SRIOV](features/sriov). The SR-IOV Network Operator creates and manages the components of the SR-IOV stack.

## Performance tuning

The [Performance Tuning](features/performance) folder contains some assets intended to improve performance such as:

* Huge Pages
* Topology Manager
* Real time kernel (including a new `worker-rt` Kubernetes/OpenShift node role)

Those assets are applied mainly via the [Node Tuning operator](https://github.com/openshift/cluster-node-tuning-operator)
and/or the [Machine Config](https://github.com/openshift/machine-config-operator) operators.

## How to contribute

See [CONTRIBUTING](CONTRIBUTING.md) for some guidelines.

## To do

* [ ] Additional step for disconnected install
* [ ] Installation Troubleshooting
* [ ] Installation scripts
