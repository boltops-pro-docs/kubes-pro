<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/exec.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

The exec command finds the latest pod from the deployment and runs `kubectl exec -ti POD bash` to get you into it. It spares you from having to manually find and type it.

## Examples

    kubes exec
    kubes exec sh
    kubes exec ls -l

## Multiple Deployments

If you have have multiple deployments in your `.kubes/resources` then the command will use the first deployment by default. You can specify the specfic deployment with the `--deployment` or `-d` option.  Examples:

    kubes exec --deployment web
    kubes exec -d web
    kubes exec -d clock
    kubes exec -d worker
    kubes exec -d web sh
    kubes exec -d web ls -l

## Multiple Pod Containers

If you have have multiple containers in your pod. You can specify the specfic container with the `--container` or `-c` option.  Examples:

    kubes exec --deployment web --container sidecar

If the `--container` option is not specified, the first container in the pod is selected.

## Specific Pod

You target a specific pod with the `--pod` or `-p` option.

    $ kubes exec -p worker-6d69cfcc54-lb5cv
    => kubectl exec -n demo-dev -ti worker-6d69cfcc54-lb5cv -- sh
    #

## Default Exec Command

The default exec command is `sh`.  Example:

    $ kubes exec
    => kubectl exec -d demo-dev -ti web-568645f665-62j8f -- sh
    /app #

You can override the default with `KUBES_EXEC_SHELL`.  Example:

    $ export KUBES_EXEC_SHELL=bash
    $ kubes exec
    => kubectl exec -d demo-dev -ti web-568645f665-62j8f -- bash
    /app #
