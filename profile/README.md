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

- [`brewlet/brewlet`](https://github.com/brewlet/brewlet) — core runtime, operator, CLI, and documentation
- [`brewlet/kubernetes`](https://github.com/brewlet/kubernetes) — Kubernetes deployment assets
- [`brewlet/maven-plugin`](https://github.com/brewlet/maven-plugin) — Maven integration
- [`brewlet/specs`](https://github.com/brewlet/specs) — architecture and specifications
- [`brewlet/integration-tests`](https://github.com/brewlet/integration-tests) — end-to-end integration tests
- [`brewlet/site`](https://github.com/brewlet/site) — source for [brewlet.sh](https://brewlet.sh)
- [`brewlet/.github`](https://github.com/brewlet/.github) — organization profile and community health files
