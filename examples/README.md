# Configuration examples

The following examples can be used to get started quickly. Please review the files thoroughly and adapt things like configuration and cluster names.

A successful install will require you to generate a trust anchor and issuer certificate. The following steps loosely follow [the official instructions](https://linkerd.io/2.12/tasks/generate-certificates/).

Obtain the `step` cli (we're using `step_linux_0.19.0_amd64.tar.gz` from [here](https://github.com/smallstep/cli/releases/tag/v0.19.0)) and execute the following commands. Take note of the `--not-after` flag. (8760h = 1 year)

```bash
step certificate create root.linkerd.cluster.local ca.crt ca.key --profile root-ca --no-password --insecure --not-after=8760h
step certificate create identity.linkerd.cluster.local issuer.crt issuer.key --profile intermediate-ca --not-after=8760h --no-password --insecure --ca ca.crt --ca-key ca.key
```

## Examples

These examples should be applied to your management cluster.

- [Basic setup on Organization namespaces](https://github.com/giantswarm/linkerd-bundle/blob/main/examples/basic-org-ns.yaml)
