# Contributing to Brewlet

Thanks for helping improve Brewlet.

Before starting substantial work, open an issue in the repository that owns the
change so the approach and scope can be discussed. Brewlet is a multi-repository
project; do not combine component changes in a single pull request.

| Change | Repository |
|---|---|
| CLI, OCI artifacts, runtime launch, shim, or provisioner implementation | [`brewlet/brewlet`](https://github.com/brewlet/brewlet) |
| Operator, admission, APIs, CRDs, manifests, or Helm chart | [`brewlet/kubernetes`](https://github.com/brewlet/kubernetes) |
| Maven plugin | [`brewlet/maven-plugin`](https://github.com/brewlet/maven-plugin) |
| Architecture contract or proposal | [`brewlet/specs`](https://github.com/brewlet/specs) |
| Cross-component tests or fixture applications | [`brewlet/integration-tests`](https://github.com/brewlet/integration-tests) |
| Website, user documentation, or workshop | [`brewlet/site`](https://github.com/brewlet/site) |

Keep pull requests focused, describe the motivation and behavior change, and
include tests and documentation in their owning repositories. For a change that
spans repositories, open linked pull requests and use the integration harness with
`BREWLET_CORE_DIR` and `BREWLET_KUBERNETES_DIR` pointed at the corresponding
checkouts.
