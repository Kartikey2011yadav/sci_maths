# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(sci_maths_library VERSION 0.0.1 LANGUAGES C)

add_library(sci_maths SHARED
  "sci_maths.c"
)

set_target_properties(sci_maths PROPERTIES
  PUBLIC_HEADER sci_maths.h
  OUTPUT_NAME "sci_maths"
)

target_compile_definitions(sci_maths PUBLIC DART_SHARED_LIB)
