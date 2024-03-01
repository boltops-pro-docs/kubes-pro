<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/release/diff.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

Runs a diff on the release. You can compare any 2 releases.

## Examples

    kubes release diff      # compares latest release to previous
    kubes release diff 3    # compares 2 to 3
    kubes release diff 1..3 # compares 1 to 3

Example with output

    $ kubes release diff
    Diff of 2 and 3
    --- .kubes/tmp/history/2.yaml   2023-03-30 19:24:34.966696545 +0000
    +++ .kubes/tmp/history/3.yaml   2023-03-30 19:24:35.750694446 +0000
    @@ -49,7 +49,7 @@
        spec:
        containers:
        - name: web
    -        image: repo/demo:kubes-2023-03-30T18-24-46-b1bfdd8
    +        image: repo/demo:kubes-2023-03-30T19-24-11-b1bfdd8
            envFrom:
            - configMapRef:
                name: demo-979bd35c9d

You can also get a diff of the latest by passing the special "preview" value. This builds the latest version and uses it to provide a diff preview.

    $ kubes release diff preview
    => colordiff -u .kubes/tmp/release/8.yaml .kubes/tmp/release/preview.yaml
    --- .kubes/tmp/release/8.yaml   2023-05-02 17:52:09.045715759 +0000
    +++ .kubes/tmp/release/preview.yaml     2023-05-02 17:52:09.045715759 +0000
    @@ -77,7 +77,7 @@
        serviceAccountName: demo
        containers:
        - name: web
    -        image: 1111111111111.dkr.ecr.us-west-2.amazonaws.com/demo:v146
    +        image: 1111111111111.dkr.ecr.us-west-2.amazonaws.com/demo:v148
