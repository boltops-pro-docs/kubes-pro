<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/deploy.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

## Examples

Deploy all resources in .kubes/resources/web

    kubes deploy

Deploy specific resource, like .kubes/resources/web/deployment.rb, use kubes to build the YAML files and then use kubectl directly.

    kubes build
    kubectl apply -f .kubes/output/web/
