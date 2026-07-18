# Brewlet

**Java on Kubernetes, for real this time.**

[Brewlet](https://brewlet.sh) lets teams ship Java applications as OCI artifacts
without a Dockerfile, OS base image, or bundled JVM. A node-resident JVM runs the
application inside a Kubernetes-managed sandbox, so runtime patching and resource
management stay with the platform while developers ship only their applications.

At a high level, Brewlet uses a node provisioner to install the runtime, a
containerd shim to execute Java payloads, and a Kubernetes `RuntimeClass` to route
workloads. An operator and the `JavaApplication` API provide a higher-level
deployment experience.

## Repositories

| Repository | Owns |
|---|---|
| [`brewlet/brewlet`](https://github.com/brewlet/brewlet) | CLI, OCI artifact support, containerd shim, and node-provisioner source |
| [`brewlet/kubernetes`](https://github.com/brewlet/kubernetes) | Operator, admission webhooks, APIs, CRDs, manifests, and Helm chart |
| [`brewlet/maven-plugin`](https://github.com/brewlet/maven-plugin) | Maven build and publishing integration |
| [`brewlet/specs`](https://github.com/brewlet/specs) | Architecture contracts and enhancement proposals |
| [`brewlet/integration-tests`](https://github.com/brewlet/integration-tests) | Cross-repository end-to-end harness and fixture applications |
| [`brewlet/site`](https://github.com/brewlet/site) | [brewlet.sh](https://brewlet.sh), user documentation, workshop, and brand assets |
| [`brewlet/.github`](https://github.com/brewlet/.github) | Organization profile and shared community health files |

Each repository is independently versioned and built. The integration harness accepts
separate core and Kubernetes checkouts, so changes can be tested across repository
branches before they are merged.
