---
layout: post
title: QEMU Build Tips 
category: QEMU
tags: dev hacks build tips
---


Are you working on QEMU development and looking for ways to speed up your workflow? Here are some tips that can help you quickly modify and verify the correctness of QEMU files in Visual Studio Code(VSCode) and start QEMU virtual machines(VMs) from snapshots:

## Compiling Individual QEMU Files in VSCode
To save time, you can compile individual QEMU files instead of compiling all of them. This can then be turned into a VSCode task, based on the information in the c_cpp_properties.json file created by clang. For more details, check out this post on the [QEMU mailing list](https://www.mail-archive.com/qemu-devel@nongnu.org/msg806626.html).

## Starting QEMU VMs from Snapshots
Instead of starting each VM from scratch and going through the entire initialization process, which can take multiple seconds, you can use snapshots to skip the time-consuming initialization phase and start the VM in milliseconds. To do this, use the following QEMU command line option:

```sh

-loadvm snapshot_name

```
I hope these QEMU build tips help you speed up your development workflow!

_Edit: _
`compile_commands.json` file for QEMU is present in the build directory. For clangd server to find it out, you must set the following options in the `.vscode/settings.json`: 

```json
 "clangd.arguments": [
  "-background-index",
  "-compile-commands-dir=debug"
],
```
_From [StackOverflow](https://stackoverflow.com/questions/51402740/visual-studio-code-clangd-extension-configuration)_

