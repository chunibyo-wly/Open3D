cmake_minimum_required(VERSION 3.20)

set(CMAKE_C_COMPILER icx)
set(CMAKE_CXX_COMPILER icpx)

project(Open3D)

add_executable(main Main.cpp)
target_compile_options(main PRIVATE -fsycl -fsycl-unnamed-lambda)
target_link_libraries(main PRIVATE sycl -fsycl)
