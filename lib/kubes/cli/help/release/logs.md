<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/release/logs.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

The `kubes release logs` command shows the logs when kubes was ran. It can be particularly useful to look at for failed deploys.

## Example

    ❯ kubes release logs
    Logs for version 3
    => docker build -t repo/demo:kubes-2023-03-30T19-24-11-b1bfdd8 -f Dockerfile .
    ...
    Created .kubes/output/shared/config_map.yaml
    Created .kubes/output/shared/namespace.yaml
    Created .kubes/output/shared/secret.yaml
    Created .kubes/output/web/deployment.yaml
    Created .kubes/output/web/service.yaml
    Created .kubes/output/worker/deployment.yaml
    Deploying resources
    => kubectl apply -f .kubes/output/shared/namespace.yaml
    namespace/demo-dev unchanged
    => kubectl apply -f .kubes/output/shared/config_map.yaml
    configmap/demo-979bd35c9d unchanged
    => kubectl apply -f .kubes/output/shared/secret.yaml
    secret/demo-6f6e6fb270 unchanged
    => kubectl apply -f .kubes/output/web/service.yaml
    service/web unchanged
    => kubectl apply -f .kubes/output/web/deployment.yaml
    deployment.apps/web configured
    => kubectl apply -f .kubes/output/worker/deployment.yaml
    deployment.apps/worker configured
