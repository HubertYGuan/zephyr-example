# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(app)

FILE(GLOB app_sources tests/zlib/*.c)
target_sources(app PRIVATE ${app_sources})
