# Required packages and flags
## CUDA
set(CUDA_TOOLKIT_ROOT_DIR "/opt/nvidia/hpc_sdk/Linux_x86_64/21.7/cuda/11.4")
enable_language(CUDA)
find_package(CUDA REQUIRED)
if (CUDA_FOUND)
    message("CUDA FOUND, Version: " ${CUDA_VERSION_STRING})
endif ()

SET(CMAKE_CXX_COMPILER pgc++)

## CUDA
cuda_add_executable(cuda cuda.cu ../matrix.cpp ../matrix.hpp)
target_link_libraries(cuda)
