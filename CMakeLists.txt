cmake_minimum_required(VERSION 2.6.4)
project(CFS_CI_LAB C)

set(CMAKE_TOOLCHAIN_FILE "/home/morgan/src/cFSHelloWorld/sample_defs/toolchain-armv7-unknown-linux-gnueabihf.cmake")
include_directories(fsw/mission_inc)
include_directories(fsw/platform_inc)

aux_source_directory(fsw/src APP_SRC_FILES)

# Create the app module
add_cfe_app(ci_lab ${APP_SRC_FILES})


