# scc Snap Package [![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/felicianotech/snap-scc/trunk/LICENSE)

A tool similar to cloc, sloccount and tokei.
For counting physical the lines of code, blank lines, comment lines, and physical lines of source code in many programming languages.

Goal is to be the fastest code counter possible, but also perform COCOMO calculation like sloccount and to estimate code complexity similar to cyclomatic complexity calculators.

This repository provides the source code for the `scc` snap which is available in the [Snapcraft Store](https://snapcraft.io/scc).
The snap is maintained by [FelicianoTech](https://www.Feliciano.Tech) meanwhile the code for `scc` itself is maintained by Ben Boyter.
The upstream repository can be found [here](https://github.com/boyter/scc).


## Installation

`scc` can be installed via snap on Ubuntu 18.04+, Fedora, and many Linux distros with `snapd` installed  by running:

```
sudo snap install scc
```

If you don't have the `snap` command available, you might be able to find instructions for your distro [here](https://snapcraft.io/docs/installing-snapd).
Otherwise you can manually install a binary from the project's [GitHub Releases page](https://github.com/boyter/scc/releases).


## Usage

Basic usage of `scc` is simply:

```
scc path/to/code
```

`scc` will then run its analysis and generate a table of results for you.
**Note:** If you use `scc` via the snap, the codebase you are checking needs to be within your user's home directory in order for it to have the correct permissions to run.
More usage instructions can be found in the upstream repo's [usage secction](https://github.com/boyter/scc#usage) though the easiest way would be to run `scc --help`.


## Development

This snap is built with [Snapcraft](https://snapcraft.io/) v3.0+ and [Multipass](https://github.com/CanonicalLtd/multipass).

On Ubuntu:


```
sudo snap install --classic snapcraft multipass
snapcraft pack
```

### Publishing

CircleCI support is dropped. Thought was given to support Snapcraft's GitHub builder or their GitHub Actions but both seem to not be well maintained. Instead, like [Pocket Casts Desktop App](https://github.com/FelicianoTech/pocket-casts-desktop-app), I will run `snapcraft remote-build` locally when ready to publish. Not ideal but it works.


## License

Both the code for this snap as well as `scc` itself is licensed under the MIT license.
This repo's license can be found [here](./LICENSE) while the license for `scc` can be found [here](https://github.com/boyter/scc/blob/trunk/LICENSE).
