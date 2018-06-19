# Meta repository

To simplify development of the Nano Node API, the meta tool can be used. This is entirely optional, but strongly encouraged if you're making changes that span multiple repositories, such as updating the Protobuffer specification.

`meta` is an easy-to-use node.js tool that helps you treat lots of repositories as monorepo without many of the downsides. Basically it allows you to keep CI integration simple and repositories small, while allowing git (and other) commands to be executed on all registered repositories.

## Install meta

`npm i -g meta`

## Clone the meta repository

`meta git clone https://<username>@github.com/nanoapi/meta.git`

This will clone all API related repositories under the meta directory.

## Sync registered repositories

`meta git pull`

## Execute arbitrary commands across repositories

As an example, the following command will generate Protobuffer code for all language bindings, based on the most recently committed protobuf specification.

meta exec ci/protobuf-gen.sh
