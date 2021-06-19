# asdf-terraform-build

Terraform plugin with go build for the asdf version manager

Japanese post: [Apple Silicon Mac で複数 Terraform バージョンを管理するために asdf\-terraform\-build を作った \| tsub's blog](https://blog.tsub.me/post/create-asdf-terraform-build/)

## Motivation

I want to manage multiple versions of Terraform on my Apple Silicon Mac.

Terraform currently does not provide pre-built binaries for Apple Silicon.
(see https://github.com/hashicorp/terraform/issues/27257)

Also, [asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp) terraform plugin only supports binary installations.
The same is true for [tfenv](https://github.com/tfutils/tfenv).

Terraform provided by Homebrew supports Apple Silicon, but is not suitable for multiple version control.

That's why I created an asdf plugin that allows you to build Terraform from source and manage multiple versions.

:warning: As Terraform begins offering pre-built binaries for Apple Silicon, this plugin will probably be archived.

## Requirements

* asdf
* Go
* jq
* git

## Installation

```
$ asdf plugin add terraform-build https://github.com/tsub/asdf-terraform-build.git
```

## Usage

```
$ asdf install terraform 1.0.0
$ asdf local terraform 1.0.0
$ terraform version
Terraform v1.0.0
on darwin_arm64
```

Read the [asdf documentation](https://asdf-vm.com/#/core-commands) for more details on how to use it.
