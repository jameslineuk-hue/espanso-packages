# Espanso package store

A private store for Espanso packages maintained by jameslineuk-hue.

Create and edit packages in [Espanso Package Workbench](https://espanso-package-workbench.jameslineuk.chatgpt.site).

## Add a package

1. Complete the package metadata and package checks in the Workbench.
2. Export the ZIP and extract it.
3. Add the extracted package-name folder at the root of this repository. Keep its version folder and all included files.
4. Commit and push your changes. Test expansions in Espanso before relying on them.

```text
package-name/
  0.1.0/
    _manifest.yml
    package.yml
    README.md
```

Optional scripts, assets, additional match files and LICENSE files belong inside the same version folder. Import additional match files from package.yml as needed. To publish an update, increase the manifest version and add a matching version folder.

The included `getting-started` package is a minimal example. Replace or extend it with your own packages.

## Install from this private store

Ensure Git is installed and your machine can clone this private repository using your GitHub credentials. Then run:

```sh
espanso install getting-started --git https://github.com/jameslineuk-hue/espanso-packages --external
```

Replace `getting-started` with the name of another package in this repository. This command is documented by Espanso for private external repositories; installation from this store has not yet been tested on your Espanso installation.

## Workflow notes

The Workbench saves drafts in your browser. It does not automatically push packages to this repository. Export the ZIP, extract it, and commit the contents here using Git or GitHub's upload interface.

This repository is private. Anyone installing a package needs access to this repository and working Git authentication.

## Reference

- [Creating packages](https://espanso.org/docs/packages/creating-a-package/)
- [Package specification](https://espanso.org/docs/packages/package-specification/)
- [Installing external packages](https://espanso.org/docs/packages/external-packages/)
