# Introduction

This repository contains a slightly different version of the standard WSL2 Kernel.
Our version is compiled with Clang/LLVM using LTO/Polly optimizations, as well as
including the necessary kernel changes to properly run AppArmor and Snaps.

Included modules, kernel configurations and build flags can change at any time, as
this kernel build is tailored to our specific needs.

One important note is: do not use our build artifacts in production as they are automated
builds used exclusively for debugging purposes. Only our releases are properly tested
and even those could potentially bring you problems in mission critical deployments.

Exercise caution and keep hacking!

# Reporting Bugs or Requesting Features

If you discover an issue relating to our kernel build, please report it using 
our issue tracker and **DO NOT REPORT IT UPSTREAM**. If we find that the bug is
directly related to Microsoft's upstream version, we'll relay it for you.

# Feature Requests

Even if our build is very (very) workload specific, you can still ask us to include
features using our issue tracker we'll consider the possibility of including it. Please
note that inclusions aren't guaranteed, but we'll do our best to accommodate other needs
as we go.

# Build Instructions

Please refer to `.github/workflows/` as our builds are automated using GitHub Actions.
We'll work on documenting the process directly in the `.yml` files, but for now the code
**is** the documentation.

# Install Instructions

We plan on offering an install script in the future to automatically download and configure
our kernel builds for you, but for now please see the documentation on the 
[.wslconfig configuration file][install-inst] for information on using a custom built kernel.

[install-inst]: https://docs.microsoft.com/en-us/windows/wsl/wsl-config#configure-global-options-with-wslconfig

