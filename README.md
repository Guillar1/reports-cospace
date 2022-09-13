# CoSpace

Setup a `CoSpace` to link multiple (mono)repos together!

## Powered by

- [vscode multi-root workspace](https://code.visualstudio.com/docs/editor/multi-root-workspaces)
- [pnpm workspaces](https://pnpm.io/workspaces)
- [lage](https://microsoft.github.io/lage/)

## Getting started

1. Clone all the repos you want to link together under the `repos` directory.

1. Update the [pnpm-workspace.yaml](pnpm-workspace.yaml) file with all the packages you want to add to your CoSpace.

1. Update the [cospace.code-workspace](cospace.code-workspace) file with all the repos you want to add to your VsCode multi root workspace.

1. PNPM installation

   - If you're using Node.js version ^14.19 or ^16.9 you just need to enable pnpm via corepack.
   - Otherwise install via `npm i -g pnpm@6.32.3`

1. Run `pnpm install` to install all the packages you've added to your CoSpace.

1. Run `pnpm build` to build all the packages you've added to your CoSpace using your monorepo task runner. I'm using [lage](https://microsoft.github.io/lage/), but [turborepo](https://turborepo.org/docs) should theoretically work.

## Updating packages in Viewer Components React

- Must be done in another folder. Running `rush install` or `rush update` within the CoSpace will break it.
