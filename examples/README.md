# Configuration examples

The following examples can be used to get started quickly. Please review the files thoroughly and adapt things like configuration and cluster names.

A successful install will require you to generate a trust anchor and issuer certificate. The following steps loosely follow [the official instructions](https://linkerd.io/2.13/tasks/generate-certificates/).

Obtain the `step` cli (we're using `step_linux_0.19.0_amd64.tar.gz` from [here](https://github.com/smallstep/cli/releases/tag/v0.19.0)) and execute the following commands. Take note of the `--not-after` flag. (8760h = 1 year)

```bash
step certificate create root.linkerd.cluster.local ca.crt ca.key --profile root-ca --no-password --insecure --not-after=8760h
step certificate create identity.linkerd.cluster.local issuer.crt issuer.key --profile intermediate-ca --not-after=8760h --no-password --insecure --ca ca.crt --ca-key ca.key
```

Please note, that for security reasons Giant Swarm by default forbids the usage of
`emptyDir` volumes as storage for pods.
The proxy containers injected by LinkerD are storing certificates in a memory backed `emptyDir` volume.
Enabling `emptyDir` volumes poses a risk that a pod will create
such big `emptyDir` that the underlying cluster node will run out of disk space.
If you're OK with this potential issue, the easiest way to allow for `emptyDir`
for all the deployments is to edit the default PSP of your cluster by running the
command:

```bash
kubectl patch psp restricted --type='json' -p='[{"op": "add", "path": "/spec/volumes/-", "value": "emptyDir"}]'
```

## Examples

These examples should be applied to your management cluster. Adapt the files according to your setup. When installing on Cluster API based workload clusters, deploy into your organization namespace (`org-`). Otherwise create the resources inside of the cluster namespace (Named after the cluster id).

- [Basic setup on Organization namespaces](https://github.com/giantswarm/service-mesh-bundle/blob/main/examples/basic-org-ns.yaml)
