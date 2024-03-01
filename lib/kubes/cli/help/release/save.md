<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/release/save.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

This command allows you to create release history records manually. Kubes will use what is in `.kubes/output` to create the release.

This helps with GitOps.

* You would use `kubes build` to build the YAML resource manifests
* Commit it into your git repo.
* Then create a kubes release history record with this command.

## Example

    kubes build
    cp -r .kubes/output /path/to/your/repo
    cd /path/to/your/repo ; git add . ; git commit -m "Update"; git push ; cd -
    kubes release save
