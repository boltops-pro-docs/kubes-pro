<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/release/rollback.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

## Example

    ❯ kubes release history
    +---------+---------+-------------------------+----------+
    | Version | Status  |       Released At       | Message  |
    +---------+---------+-------------------------+----------+
    | 2       | success | 2023-05-07 04:10:12 UTC | Deployed |
    | 1       | success | 2023-05-07 04:09:58 UTC | Deployed |
    +---------+---------+-------------------------+----------+

    ❯ kubes release rollback 1
    Rolling back to version 1
    => kubectl apply -f .kubes/tmp/release/rollback.yaml
    namespace/demo-dev unchanged
    service/web unchanged
    deployment.apps/web configured
    Release Version: 3

    ❯ kubes release history
    +---------+---------+-------------------------+---------------+
    | Version | Status  |       Released At       |    Message    |
    +---------+---------+-------------------------+---------------+
    | 3       | success | 2023-05-07 04:10:33 UTC | Rollback to 1 |
    | 2       | success | 2023-05-07 04:10:12 UTC | Deployed      |
    | 1       | success | 2023-05-07 04:09:58 UTC | Deployed      |
    +---------+---------+-------------------------+---------------+

    ❯

Also see: kubes release history -h
