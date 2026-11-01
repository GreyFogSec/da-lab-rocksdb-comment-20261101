# Meta RocksDB AI-review artifact lab

This lab mirrors the `meta/rocksdb` review-publication split:

- a read-only PR workflow uploads a Markdown review and immutable metadata;
- a trusted `workflow_run` caller invokes a reusable workflow;
- the reusable workflow checks out trusted scripts, downloads into `_artifact`, and posts a PR comment with `issues: write`/`pull-requests: write`.

The committed `_artifact` symlink is an artificial DA-01 positive-control prerequisite and is absent upstream. The lab proves an out-of-boundary write and records its hash in a harmless PR comment. It does not claim code execution in the real RocksDB workflow.
