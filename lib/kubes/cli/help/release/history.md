<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/release/history.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

## Example

    $ kubes release history
    +---------+---------+-------------------------+----------------+
    | Version | Status  |       Released At       |    Message     |
    +---------+---------+-------------------------+----------------+
    | 39      | success | 2023-03-28 17:53:08 UTC | Rollback to 30 |
    | 38      | success | 2023-03-28 17:52:50 UTC | Deployed       |
    | 37      | success | 2023-03-28 17:52:31 UTC | Rollback to 30 |
    | 36      | success | 2023-03-28 17:52:07 UTC | Deployed       |
    | 35      | success | 2023-03-28 17:51:33 UTC | Deployed       |
    | 34      | success | 2023-03-28 17:51:16 UTC | Deployed       |
    | 33      | success | 2023-03-28 17:51:00 UTC | Deployed       |
    | 32      | success | 2023-03-28 17:47:43 UTC | Deployed       |
    | 31      | success | 2023-03-28 17:47:16 UTC | Rollback to 22 |
    | 30      | success | 2023-03-28 17:45:39 UTC | Deployed       |
    +---------+---------+-------------------------+----------------+

Also see: kubes release -h

The `kubes release logs [VERSION]` command can be useful to show why a deploy failed.
