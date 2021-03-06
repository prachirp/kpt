---
title: "Validator Catalog"
linkTitle: "Validators"
type: docs
description: >
    Catalog of Validator Functions.
---
<!---
DO NOT EDIT. Generated by: "cd ../catalog; npm run gen-docs"
-->

A validator verifies that a resource satisfies certain conditions without creating
or modifying any resources. Validator functions are managed by function authors who
desire to verify the state (optionally) recorded in the `--results-dir` path
provided by `kpt`.

For example, a replica may be specified to be within a certain range and verified
using a validator function.

## Validator Functions

| Image                                                | Args | Description                                                                                                                             | Example                                                                                                         | Source                                                                                                                          | Toolchain                                         |
| ---------------------------------------------------- | ---- | --------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| gcr.io/kpt-functions/istioctl-analyze                |      | Istioctl analyze is a diagnostic tool that can detect potential issues with Istio configuration and output errors to the results field. | [Example](https://github.com/GoogleContainerTools/kpt-functions-catalog/tree/master/examples/istioctl-analyze/) | [Source](https://github.com/GoogleContainerTools/kpt-functions-catalog/blob/master/functions/ts/src/istioctl_analyze.ts)        | [Typescript SDK](../../../producer/functions/ts/) |
| gcr.io/kpt-functions/gatekeeper-validate             |      | Enforces OPA constraints on input objects. The constraints are also passed as part of the input to the function.                        |                                                                                                                 | [Source](https://github.com/GoogleContainerTools/kpt-functions-sdk/blob/master/go/pkg/functions/gatekeeper/validate.go)         |                                                   |
| gcr.io/kpt-functions/validate-rolebinding            |      | [Demo] Enforces a blacklist of subjects in RoleBinding objects.                                                                         |                                                                                                                 | [Source](https://github.com/GoogleContainerTools/kpt-functions-sdk/blob/master/ts/demo-functions/src/validate_rolebinding.ts)   | [Typescript SDK](../../../producer/functions/ts/) |
| gcr.io/kpt-functions/kubeval                         |      | Validates configuration using kubeval.                                                                                                  |                                                                                                                 | [Source](https://github.com/GoogleContainerTools/kpt-functions-catalog/blob/master/functions/ts/src/kubeval.ts)                 | [Typescript SDK](../../../producer/functions/ts/) |
| gcr.io/kustomize-functions/example-validator-kubeval |      | [Demo] Validates that all containers have cpu and memory reservations set.                                                              |                                                                                                                 | [Source](https://github.com/kubernetes-sigs/kustomize/blob/master/functions/examples/validator-kubeval/image/main.go)           | [Go Library](../../../producer/functions/golang/) |
| gcr.io/kustomize-functions/example-validator         |      | Validates Kubernetes configuration files using schemas from the Kubernetes OpenAPI spec.                                                |                                                                                                                 | [Source](https://github.com/kubernetes-sigs/kustomize/blob/master/functions/examples/validator-resource-requests/image/main.go) | [Go Library](../../../producer/functions/golang/) |
| gcr.io/kpt-functions/suggest-psp                     |      | [Demo] Lints PodSecurityPolicy by suggesting 'spec.allowPrivilegeEscalation' field be set to 'false'.                                   |                                                                                                                 | [Source](https://github.com/GoogleContainerTools/kpt-functions-sdk/blob/master/ts/demo-functions/src/suggest_psp.ts)            | [Typescript SDK](../../../producer/functions/ts/) |

## Next Steps

- Learn more ways of using the kpt fn command from the [reference] doc.

[reference]: ../../../../reference/fn/run/
