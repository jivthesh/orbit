# Copyright (c) 2020 The Orbit Authors. All rights reserved.
# Use of this source code is governed by a BSD-style license that can be
# found in the LICENSE file.

project(OrbitTest)

add_executable(OrbitTest)

target_compile_options(OrbitTest PRIVATE ${STRICT_COMPILE_FLAGS})

target_sources(OrbitTest PRIVATE main.cpp OrbitTest.cpp)
target_sources(OrbitTest PUBLIC OrbitTest.h)

target_include_directories(OrbitTest PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(OrbitTest PRIVATE Threads::Threads)
