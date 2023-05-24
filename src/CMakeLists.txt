# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(ffigen_app_test17754_library VERSION 0.0.1 LANGUAGES C)

add_library(ffigen_app_test17754 SHARED
  "ffigen_app_test17754.c"
)

set_target_properties(ffigen_app_test17754 PROPERTIES
  PUBLIC_HEADER ffigen_app_test17754.h
  OUTPUT_NAME "ffigen_app_test17754"
)

target_compile_definitions(ffigen_app_test17754 PUBLIC DART_SHARED_LIB)
