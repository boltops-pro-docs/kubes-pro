<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/helm/rollback.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

## Example

    ❯ kubes helm history
    Showing history of releases:
    => helm history demo-dev --namespace demo-dev
    REVISION        UPDATED                         STATUS          CHART           APP VERSION     DESCRIPTION
    1               Sun May  7 04:03:13 2023        superseded      app-0.1.0       0.1.0           Install complete
    2               Sun May  7 04:03:19 2023        deployed        app-0.1.0       0.1.0           Upgrade complete

    ❯ kubes helm rollback 1
    => helm rollback demo-dev 1 --namespace demo-dev
    Rollback was a success! Happy Helming!

    ❯ kubes helm history
    Showing history of releases:
    => helm history demo-dev --namespace demo-dev
    REVISION        UPDATED                         STATUS          CHART           APP VERSION     DESCRIPTION
    1               Sun May  7 04:03:13 2023        superseded      app-0.1.0       0.1.0           Install complete
    2               Sun May  7 04:03:19 2023        superseded      app-0.1.0       0.1.0           Upgrade complete
    3               Sun May  7 04:03:34 2023        deployed        app-0.1.0       0.1.0           Rollback to 1

    ❯
