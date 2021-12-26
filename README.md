[![Clang/LLVM WSL2-Linux-Kernel Build](https://github.com/INCT-DD/WSL2-Linux-Kernel-clang/actions/workflows/5.10-clang.yml/badge.svg?branch=linux-msft-wsl-5.10.y.clang)](https://github.com/INCT-DD/WSL2-Linux-Kernel-clang/actions/workflows/5.10-clang.yml)

# Introduction

This repository contains a slightly different version of the standard WSL2 Kernel,
compiled with Clang/LLVM using LTO/Polly optimizations, geared towards data workloads,
and including the necessary kernel changes to properly run AppArmor and Snaps.

**Important**: do not use our build artifacts in production as they are automated
builds used exclusively for debugging purposes. Only our releases are properly tested
and even those could potentially bring you problems in mission critical deployments as
we only test those kernels for our own purposes. So exercise caution and keep hacking!

For more information, take a look at our [wiki][wiki]

# Reporting Bugs or Requesting Features

If you discover an issue relating to our kernel build, please report it using 
our issue tracker and **DO NOT REPORT IT UPSTREAM**. If we find that the bug is
directly related to Microsoft's upstream version, we'll relay it for you.

# Feature Requests

Even if our build is very workload specific, you can still ask us to include
features using our issue tracker and we'll consider the possibility of including it. Please
note that inclusions aren't guaranteed, but we'll do our best to accommodate other needs
as we go.

# Build Instructions

Please refer to `.github/workflows/` as our builds are automated using GitHub Actions.
We'll work on documenting the process directly in the `.yml` files, but for now the code
**is** the documentation.

# Install Instructions

We plan on offering an install script in the future to automatically download and configure
our kernel builds for you, but for now please see the documentation on the 
[.wslconfig configuration file][install-inst] for information on using a custom built kernel and
check our [wiki][wiki] for our own installation instructions.

[install-inst]: https://docs.microsoft.com/en-us/windows/wsl/wsl-config#configure-global-options-with-wslconfig
[wiki]: https://github.com/INCT-DD/WSL2-Linux-Kernel-clang/wiki
