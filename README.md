# nx-tools-nx-container-provenance-issue

This repo is related to a issue raised in nx-tools to fix a bug.
Note this repo was largely built with co-pilot.

To test the bug follow the below commands and inspect the output docker buildx build command to see the absence of the provenance flag

1. cd org
2. npx nx run @org/test-provenance:ci --dry-run | grep buildx
