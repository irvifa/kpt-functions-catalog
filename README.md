
<!---
DO NOT EDIT. Generated by: "cd docs; npm run gen-docs"
-->

# KPT Functions Catalog

This repository documents a catalog of functions implementing [Configuration Functions Specification][spec].

These functions can be implemented using any toolchain such as the [KPT Functions SDK][sdk].

## Sources

See [definition of source functions][source].

| Image                          | Args          | Description                                                | Source                                                                                                           |
| ------------------------------ | ------------- | ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| gcr.io/kpt-dev/kpt             | kpt fn source | Reads a directory of Kubernetes configuration recursively. | [Link](https://github.com/kubernetes-sigs/kustomize/blob/master/cmd/config/internal/commands/source.go)          |
| gcr.io/kpt-functions/read-yaml |               | Reads a directory of Kubernetes configuration recursively. | [Link](https://github.com/GoogleContainerTools/kpt-functions-sdk/tree/master/ts/demo-functions/src/read_yaml.ts) |

## Sinks

See [definition of sink functions][sink].

| Image                           | Args        | Description                                                                                                                | Source                                                                                                            |
| ------------------------------- | ----------- | -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| gcr.io/kpt-dev/kpt              | kpt fn sink | Writes a directory of Kubernetes configuration. It maintains the original directory structure as read by source functions. | [Link](https://github.com/kubernetes-sigs/kustomize/blob/master/cmd/config/internal/commands/sink.go)             |
| gcr.io/kpt-functions/write-yaml |             | Writes a directory of Kubernetes configuration. It maintains the original directory structure as read by source functions. | [Link](https://github.com/GoogleContainerTools/kpt-functions-sdk/tree/master/ts/demo-functions/src/write_yaml.ts) |

## Validators

| Image                                     | Args | Description                                                                                                      | Source                                                                                                                      |
| ----------------------------------------- | ---- | ---------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| gcr.io/kpt-functions/gatekeeper-validate  |      | Enforces OPA constraints on input objects. The constraints are also passed as part of the input to the function. | [Link](https://github.com/GoogleContainerTools/kpt-functions-sdk/tree/master/go/pkg/functions/gatekeeper/validate.go)       |
| gcr.io/kpt-functions/validate-rolebinding |      | [Demo] Enforces a blacklist of subjects in RoleBinding objects.                                                  | [Link](https://github.com/GoogleContainerTools/kpt-functions-sdk/tree/master/ts/demo-functions/src/validate_rolebinding.ts) |

## Generators

| Image                               | Args | Description                                                                                          | Source                                                                                                                |
| ----------------------------------- | ---- | ---------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| gcr.io/kpt-functions/expand-team-cr |      | [Demo] Reads custom resources of type Team and generates multiple Namespace and RoleBinding objects. | [Link](https://github.com/GoogleContainerTools/kpt-functions-sdk/tree/master/ts/demo-functions/src/expand_team_cr.ts) |

## Transformers

| Image                                | Args | Description                                                                                 | Source                                                                                                              |
| ------------------------------------ | ---- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| gcr.io/kpt-functions/mutate-psp      |      | [Demo] Mutates PodSecurityPolicy objects by setting spec.allowPrivilegeEscalation to false. | [Link](https://github.com/GoogleContainerTools/kpt-functions-sdk/tree/master/ts/demo-functions/src/mutate_psp.ts)   |
| gcr.io/kpt-functions/label-namespace |      | [Demo] Adds a label to all Namespaces.                                                      | [Link](https://github.com/GoogleContainerTools/kpt-functions-sdk/tree/master/ts/hello-world/src/label_namespace.ts) |

## Miscellaneous

| Image                      | Args | Description                                | Source                                                                                                       |
| -------------------------- | ---- | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| gcr.io/kpt-functions/no-op |      | [Demo] No Op function for testing purposes | [Link](https://github.com/GoogleContainerTools/kpt-functions-sdk/tree/master/ts/demo-functions/src/no_op.ts) |

[spec]: https://github.com/kubernetes-sigs/kustomize/blob/master/cmd/config/docs/api-conventions/functions-spec.md
[source]: https://github.com/GoogleContainerTools/kpt-functions-sdk/blob/master/docs/concepts.md#source-function
[sink]: https://github.com/GoogleContainerTools/kpt-functions-sdk/blob/master/docs/concepts.md#sink-function
[sdk]: https://github.com/GoogleContainerTools/kpt-functions-sdk

