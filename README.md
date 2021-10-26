# Repro repo for bug in patch-package

The bug seems to occur when trying to patch a file that doesn't end in a newline, where the patch then involves adding a line to the end of the file.

To reproduce, I've installed a single very small package and added a comment on the last and third to last lines. After installing and running patch-package, the final comment is not applied.

In this repro it fails silently, but in my real project it was actually failing.