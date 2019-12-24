---
title: "Release"
linkTitle: "Release"
weight: 1
description: >
  Important release workflow need to keep in mind.
---

{{% pageinfo %}}
This is a placeholder page that shows you important workflows which all developers in the team need to follow.
{{% /pageinfo %}}

Releasing is one of the core processes. It’s very important to follow its steps as any failure could have a huge impacts on our users.

1. Make sure all included branches were reviewed with a PR, and PR approved.
2. Merge all PRs and open branches to dev.
3. Make sure CI build did not fail.
4. Make sure to run all tests suites.
5. Make a normal run.
6. Run a full random check with the most extensive db available.
7. Bump version infos.
8. Update Changelog.
9. Tag commit with version number.
10. Merge dev to release branch.
11. Merge dev to master.
12. Send release email informing team of the new release + ask them to run there own tests if they have