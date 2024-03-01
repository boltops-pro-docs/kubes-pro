<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/kubes-pro/blob/main/lib/kubes/cli/help/completion.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

## Examples

    kubes completion

Prints words for TAB auto-completion.

    kubes completion
    kubes completion hello
    kubes completion hello name

To enable, TAB auto-completion add the following to your profile:

    eval $(kubes completion_script)

Auto-completion example usage:

    kubes [TAB]
    kubes hello [TAB]
    kubes hello name [TAB]
    kubes hello name --[TAB]
