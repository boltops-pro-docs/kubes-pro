<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/release/show.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

Shows the Kubernetes resource manifests used for the release.

## Example

    $ kubes release show 2 | yq
    Showing version 2
    ---
    metadata:
    labels:
        app: demo
    name: demo-dev
    apiVersion: v1
    kind: Namespace
    ...
