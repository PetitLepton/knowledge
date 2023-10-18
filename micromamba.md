# nix

To make `micromamba` works globally from the main `nix` profile, one has to add the following environment variables to `.bashrc`.
```bash
export MAMBA_EXE="$HOME/.nix-profile/bin/micromamba";
export MAMBA_ROOT_PREFIX="$HOME/micromamba";
```

# random

`micromamba` does not use `base` environment, see [here](https://prefix.dev/docs/mamba/environments#the-base-environment).
> Micromamba (the evolution of the mamba package manager) comes as a single binary. That means, it does not need a base environment for any dependencies.

The list of environments is contained in `.conda/environments.txt`. `micromamba` reads the content for `micromamba env list`, see [`conda`'s code](https://github.com/conda/conda/blob/a6fbbbef210bf2f6f9480394f946185e5d2fc54f/conda/core/envs_manager.py#L23).

