cmake_minimum_required(VERSION 3.10)

project(macos-raw-usb-helper)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(SOURCE_FILES
        main.cpp
        Helper.h
)

add_executable(macos-raw-usb-helper MACOSX_BUNDLE ${SOURCE_FILES})

set_target_properties(macos-raw-usb-helper PROPERTIES
        MACOSX_BUNDLE_INFO_PLIST ${CMAKE_CURRENT_SOURCE_DIR}/Info.plist
)

# If you're linking against any library, use target_link_libraries.
# For example, if you need the Foundation framework:
# find_library(FOUNDATION_LIBRARY Foundation)
# target_link_libraries(HelperTool ${FOUNDATION_LIBRARY})
