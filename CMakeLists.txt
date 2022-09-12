cmake_minimum_required(VERSION 3.24)

project ("BTrack" VERSION 1.0.0
                     DESCRIPTION "A C++ library for beat detectionn."
                     HOMEPAGE_URL "https://github.com/dadjeibaah/BTrack")
                     
include (GNUInstallDirs)

add_library (${PROJECT_NAME} INTERFACE)

target_include_directories (
  ${PROJECT_NAME}
  INTERFACE $<BUILD_INTERFACE:${${PROJECT_NAME}_SOURCE_DIR}/src>
            $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>)

target_compile_features (${PROJECT_NAME} INTERFACE cxx_std_11)

set (CMAKE_SUPPRESS_REGENERATION true)