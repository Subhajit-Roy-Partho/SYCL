# SYCL
SYCL tutorial

For installing in Nvidia GPUs:
- Make double sure of the cuda version if correct, if there are plugins error after installation may be wrong cuda version is the reason.
- Install Intel oneAPI Base Toolkit (For now: wget https://registrationcenter-download.intel.com/akdlm/IRC_NAS/992857b9-624c-45de-9701-f6445d845359/l_BaseKit_p_2023.2.0.49397_offline.sh
    sudo sh ./l_BaseKit_p_2023.2.0.49397_offline.sh)
- Install codeplay packages for Nvidia.
- Setup llvm environment with . /opt/intel/oneapi/setvars.sh --include-intel-llvm
- Header in codeplay Nvidia <CL/sycl.hpp>, same as standard procedure.
- Compile with llvm `clang++ -fsycl -fsycl-targets=nvptx64-nvidia-cuda testSimple.cpp`



General comments:

- Now for opencl libraries sycl::buffer<sycl::opencl::cl_int, 1> Buffer(4) instead of sycl::buffer<sycl::cl_int, 1> Buffer(4);
