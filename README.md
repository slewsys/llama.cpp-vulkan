# Build and install llama.cpp for HIP/ROCm

The script `install-llama.cpp-rocm` is intended to be run on
Fedora 43. It builds UCX, OpenMPI and llama.cpp with support for AMD
ROCm. I are built with ROCm support as well. `llama-server`,
`llama-cli`, et al. and their shared libraries are installed
(properly) under */usr/local*.

The `asdf` version manager is installed as necessary to provide a
local Python v3.12 and golang. Shell init files (e.g., ~/.bashrc,
~/.bash_profile) are not modified. To benefit from `asdf`, add the
asdf install directory and shims path to the shell init files :

```
: ${ASDF_DATA_DIR:="${HOME}/.asdf"}

export PATH=${ASDF_DATA_DIR}/shims:${PATH}:${HOME}/bin
```
