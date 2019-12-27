---
title: "go-dep"
linkTitle: "go-dep"
weight: 3
description: >
  Manual page for dep
---

{{% pageinfo %}}
All commands related to `dep` and their usages.
{{% /pageinfo %}}

## NAME

```
dep: - manual page for dep
```

## SYNOPSIS

```
dep <command>
```

## DESCRIPTION

```
      dep is a tool for managing dependencies for Go projects

      Commands:

      init    Initialize a new project with manifest and lock files

      status  Report the status of the project's dependencies

      ensure  Ensure a dependency is safely vendored in the project

      prune   Prune the vendor tree of unused packages

      version Show the dep version information
```

## EXAMPLES

```
      dep init
              set up a new project

      dep ensure
              install the project's dependencies

      dep ensure -update
              update the locked versions of all dependencies

      dep ensure -add github.com/pkg/errors
              add a dependency to the project

      Use "dep help [command]" for more information about a command.

      dep is a tool for managing dependencies for Go projects

      Usage: dep <command>

      Commands:

      init   Initialize a new project with manifest and lock files

      status Report the status of the project's dependencies

      ensure Ensure a dependency is safely vendored in the project

      prune  Prune the vendor tree of unused packages

      version
              Show the dep version information

       dep init
              set up a new project

      Use "dep help [command]" for more information about a command.
```

## OFFICIAL DOCUMENT

For more information about dep, please go through following link:

https://golang.github.io/dep/docs/introduction.html