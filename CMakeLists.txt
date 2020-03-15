cmake_minimum_required(VERSION 2.8.12)
project(py-geometry-utils-lib)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
find_package(Eigen3 REQUIRED)
add_subdirectory(lib/pybind11)
add_subdirectory(lib/geometry-utils-lib)
include_directories(
  lib/geometry-utils-lib/include
  ${EIGEN3_INCLUDE_DIRS}
)

pybind11_add_module(utils_quat    src/plugins/quat.cpp)
pybind11_add_module(utils_xform   src/plugins/xform.cpp)
