# Prometheus Exporter Snap for charm-juju-backup-all

The prometheus-juju-backup-all-exporter is a snap for collecting backup results
from charm-juju-backup-all, and export those results as prometheus metrics. The
metrics are expected to be used with prometheus.

## Getting Started

## Snap Configuration

## Local Build and Testing

You need `snapcraft` to build the snap:

```bash
$ sudo snap install snapcraft --classic
```

Snapcraft also requires backend to create isolated build environment, you can
choose the following two backends:

- [LXD](https://linuxcontainers.org/lxd/introduction/), which creates container
  image build instances. It can be used inside virtual machines.
- [Multipass](https://multipass.run/), which creates virtual machine build
  instances. It cannot be reliably used on platforms that do not support nested
  virtualization. For instance, Multipass will most likely not run inside a
  virtual machine itself.

To build the snap:

```bash
$ make build
```

To try the snap that was built, you can install it locally:

```bash
$ sudo snap install --devmode ./$(grep -E "^name:" snap/snapcraft.yaml | awk '{print $2}').snap
```
