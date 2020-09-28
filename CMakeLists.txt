cmake_minimum_required(VERSION 3.13)
cmake_policy(VERSION 3.13)
project(qpbo)

set(QPBO_VERSION_MAJOR 1)
set(QPBO_VERSION_MINOR 4)
set(QPBO_VERSION_PATCH 0)
set(QPBO_VERSION_STRING "${QPBO_VERSION_MAJOR}.${QPBO_VERSION_MINOR}.${QPBO_VERSION_PATCH}")

set(SRC_FILES QPBO.cpp QPBO_extra.cpp QPBO_maxflow.cpp QPBO_postprocessing.cpp)

add_library(qpbo_shared SHARED ${SRC_FILES})
add_library(qpbo_static STATIC ${SRC_FILES})
set_target_properties(qpbo_shared qpbo_static PROPERTIES OUTPUT_NAME qpbo)
