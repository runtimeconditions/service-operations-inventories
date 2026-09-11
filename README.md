# Service Operations Inventories

This repository contains language-neutral operations inventories for services that do not provide an adequate authoritative machine-readable operation model such as Smithy, OpenAPI, or protobuf service definitions.

An inventory describes service-owned facts: stable operations, service resource and action classifications, operation inputs, input requiredness, and service-domain value constraints. It MUST NOT reference a Runtime Conditions extension, Condition kind, interface type, adapter behavior, SDK package, programming language, or profile emission policy.

Runtime Conditions extensions consume an exact inventory through a Service Operations Semantic Bridge maintained in the `runtimeconditions/extensions` repository. That bridge owns the reviewed translation from service operations into adapter-actionable Condition semantics.

The [Service Operation Authoring Guide](https://github.com/runtimeconditions/spec/blob/main/docs/guides/service-operation-authoring.md) explains when an inventory is justified, how it differs from a semantic bridge, and how the extension and service mapping are generated from the selected operation authority.

Each maintained inventory uses the standard filename `service-operations-inventory.yaml` inside a service-named directory. Generated or authoritative models remain in their owning upstream repositories; this repository is the fallback when no adequate upstream model exists.
