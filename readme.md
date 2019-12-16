# ITV DOCUMENT

## Introduction

## Usage

Make a local working copy of the example site directly using `git clone`:

```
git clone https://github.com/NguyenHoaiPhuong/itv-doc.git
```

Switch to the root of the cloned project:

```
cd itv-doc
```

Get local copies of the project submodules so you can build and run your site locally:

```
git submodule update --init --recursive
```

Build your site:

```
hugo server
```

Preview your site in your browser at: http://localhost:1313/. You can use Ctrl + c to stop the Hugo server whenever you like.

## Prerequisites

- Framework: Hugo version 0.53 or later
- Theme : Docsy

## Get Started

### Create new Hugo site and add docsy theme

- To create a new Hugo site project, run the following commands from project’s root directory:

    ```
    hugo new site itv-doc
    cd itv-doc
    git init
    ```

- To add the Docsy theme to an existing site, run the following commands from your project’s root directory:

    ```
    git submodule add https://github.com/google/docsy.git themes/docsy
    echo 'theme = "docsy"' >> config.toml
    git submodule update --init --recursive
    ```

-  To push project to a new repository:

    1. Create a new repository in GitHub for the site with the chosen repo name.

    2. Configure `origin` in the project. From the site’s root directory, set the URL for origin to the new repo:

        ```
        git remote set-url origin https://github.com/NguyenHoaiPhuong/itv-doc.git
        ```

    3. Verify that remote is configured correctly by running:

        ```
        git remote -v
        ```

    4. Push itv-doc to the repository:

        ```
        git push -u origin master
        ```


### Basic site configuration

- 