Ebuilds to install ROCm on Gentoo Linux

-> https://github.com/RadeonOpenCompute/ROCm

**Please report all problems here first, if you tried ebuilds of this repository.**<br>
All ebuilds which are already exist in Gentoo portage will be removed from this repository.<br>
If you have a problem with an ebuild from Gentoo portage then submit a bugreport at https://bugs.gentoo.org/.

**The ebuilds for ROCm 2.9.0 are in a good state now.**<br>
**And the ebuilds for ROCm 2.10.0 seem to be in a good state now too.**<br>

**Thanks to all contributors.**

The following tables show all ebuilds tested (2019-11-30) in this repository. <br>
All other ebuilds can be out of date!

Kernel, driver, libraries, compiler and tools:

|Ebuild|Current Version|State| FHS | in Gentoo portage| 
|---|---|---|---|---|
|sys-kernel/rocm-sources| 2.10 | based on linux kernel 5.0.0-rc1 | (ok) |  |
|dev-util/rocm-cmake| 2.10 | | Yes | :heavy_check_mark:<br> 0.2, 2.7.0, 2.8.0, 2.9.0, 2.10.0 |
|dev-libs/roct-thunk-interface| 2.10 |  | Yes | :heavy_check_mark:<br> 2.6.0, 2.7.0, 2.8.0, 2.9.0, 2.10.0 |
|dev-libs/rocr-runtime| 2.10 | | Yes | :heavy_check_mark:<br> 2.6.0, 2.7.0, 2.8.0, 2.9.0, 2.10.0 |
|dev-libs/rocm-device-libs | 2.10 | | Yes | :heavy_check_mark:<br> 2.6.0, 2.7.0, 2.8.0, 2.9.0, 2.10.0 |
|dev-libs/rocm-opencl-driver | 2.10 | | Yes | :heavy_check_mark:<br> 2.6.0, 2.7.0, 2.8.0, 2.9.0, 2.10.0 |
|dev-libs/rocm-opencl-runtime| 2.10 | "clinfo" reports suitable informations.<br> Simple "Hello World" program from "OpenCL Programming Guide" works. | Yes | :heavy_check_mark:<br> 2.6.0, 2.8.0, 2.9.0, 2.10.0 |
|dev-libs/RCCL | 2.10 |  | (ok) | |
|media-libs/hsa-amd-aqlprofile| 1.0.0 | | (ok) | |
|media-libs/hsa-ext-rocr| 1.1.9.122 | | Yes | :heavy_check_mark:<br> V1.1.9.112, V1.1.9.122 |
|dev-util/rocm-bandwidth-test| 2.10 | Reports suitable informations. | (ok) |  |
|dev-util/rocprofiler| 2.10 |  | (ok) | |
|dev-libs/rocm-smi-lib| 2.10 |  | (ok) | |
|dev-util/rocm-smi| 2.10 | Reports suitable informations. | (ok) | |
|dev-util/rocminfo| 2.10 | Reports suitable informations. | Yes | :heavy_check_mark:<br> 2.6.0, 2.7.0, 2.8.0, 2.9.0, 2.10.0 |
|dev-libs/rocm-comgr| 2.10 | | Yes | :heavy_check_mark:<br> 2.6.0, 2.7.0, 2.8.0, 2.9.0, 2.10.0 | 
|dev-libs/rocr-debug-agent | 2.10 |  | (ok) | |
|dev-util/roctracer| 2.9 | No release yet. | (ok) | |
|dev-util/rocm-clang-ocl| 2.10 | | (ok) | |
|dev-util/rcp| 5.6 |   | (ok) | |
|sys-devel/llvm-roc | 2.10 | | Yes |:heavy_check_mark:<br> 2.6.0, 2.7.0, 2.8.0, 2.9.0, 2.10.0 | |
|sys-devel/hcc| 2.10 |  | (ok) | |
|sys-devel/hip| 2.10 | currently depends on HCC, building based on clang (HIP-clang) is currently under test | (ok) | |
|sys-devel/amd-rocm-meta| 2.10 | Currently roctracer is disabled! | (ok) | |

<br>
ROCm Libraries:

|Ebuild|Current Version|State|FHS|in Gentoo portage|
|---|---|---|---|---|
|sci-libs/rocBLAS| 2.10 | Installs, not tested yet. | (ok) | |
|sci-libs/rocPRIM| 2.10 | Installs, not tested yet. | (ok) | |
|sci-libs/rocSPARSE| 2.10 | Installs, not tested yet.  | (ok) | |
|sci-libs/rocALUTION| 2.10 | Installs, not tested yet. | (ok) | |
|sci-libs/rocThrust| 2.10 | Installs, not tested yet. | (ok) | |
|sci-libs/rocFFT| 2.10 | Installs, not tested yet | (ok) | |
|sci-libs/rocRAND| 2.10 | Installs, not tested yet | (ok) |  |
|sci-libs/rocSOLVER| 9999 | Installs, not tested yet | (ok) | |
|sci-libs/hipCub | 2.10 | Installs, not tested yet. | (ok)| |
|sci-libs/hipBLAS | 2.10 | Installs, not tested yet. | (ok) | |
|sci-libs/hipSPARSE | 2.10 | Installs, not tested yet. | (ok) | |
|sci-libs/MIOpenGEMM | 1.1.6 | Installs, not tested yet. | (ok) | |
|sci-libs/MIOpen | 2.10 | Installs, not tested yet. | (ok) | |
|sci-libs/MIVisionX | | No ebuild exist, any contribution is appreciated. | | |
|sci-libs/MIGraphX | | No ebuild exist, any contribution is appreciated. | | | 

<br>
Systems known to work:

| No | CPU | PCIe |  GPU | additional information |
|---|---|---|---|---|
| 1 | Intel Core i5 8400 | PCIe 3.0 | Radeon RX 560 (POLARIS11) | |
| 2 | Intel Core i7 6700k | PCIe 3.0 over Thunderbolt 3 | Radeon VII | |
| 3 | AMD Ryzen 1700 | PCIe 3.0 | Radeon RX 580 | |

<br>
=== For tensorflow-rocm ===

``` emerge miopen rocFFT rocRAND rocBLAS rccl rocm-smi rocminfo ```

=== AMDGPU wiki page ===

https://wiki.gentoo.org/wiki/AMDGPU#SME
https://wiki.gentoo.org/wiki/AMDGPU#Kernel

=== udev rule for ROCm ===

This is so ROCm utilities and libraries can function correctly.

``` echo 'SUBSYSTEM=="kfd", KERNEL=="kfd", TAG+="uaccess", GROUP="video"' | sudo tee /etc/udev/rules.d/70-kfd.rules ```

You probably also want to add a video group if you don't already have one and add yourself to it.

Add a video group:
``` emerge acct-group/video ```

Add your user account to the group:
``` sudo usermod -a -G video $LOGNAME ```

=== ROCm debugging tools ===

In no particular order some helpful utilities for testing ROCm are:

Note: clinfo might not work with a noexec /tmp

``` rocminfo && rocm-smi && hipconfig && clinfo && MIOpenDriver pool ```
