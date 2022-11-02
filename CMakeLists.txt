#
#
#

project (ccc)
cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
# set(CMAKE_CXX_EXTENSIONS OFF)

find_package(OpenMP REQUIRED)


add_executable(luDecomp
	c++/luDecomp/critical.cpp
	c++/luDecomp/critical.hpp
	c++/luDecomp/luDecomp.cpp
	)
target_link_libraries(luDecomp PUBLIC OpenMP::OpenMP_CXX)
