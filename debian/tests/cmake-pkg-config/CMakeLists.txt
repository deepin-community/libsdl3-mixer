# Copyright 2019 Collabora Ltd.
# SPDX-License-Identifier: Zlib

# Test use of sdl3-mixer in a CMake project by using pkg-config,
# extrapolating from how wesnoth-1.16 checks for SDL2_mixer.
cmake_minimum_required(VERSION 3.12)
project(test LANGUAGES C)
find_package(PkgConfig REQUIRED)
pkg_check_modules(SDL3MIXER REQUIRED sdl3-mixer>=3.0.0)
include_directories(SYSTEM ${SDL3MIXER_INCLUDE_DIRS})
add_executable(main main.c)
target_link_libraries(main ${SDL3MIXER_LIBRARIES})
