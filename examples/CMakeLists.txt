# Build examples simple and editor. Currently only tested on MacOS.

# Simple Example
set(EXAMPLE_SIMPLE_APP_NAME simple)
add_executable(${EXAMPLE_SIMPLE_APP_NAME} simple.cpp)
target_include_directories(${EXAMPLE_SIMPLE_APP_NAME} PRIVATE ${imgui_SOURCE_DIR})
target_link_libraries(${EXAMPLE_SIMPLE_APP_NAME} PRIVATE
    raylib
    imgui
    RlImGui
)

if (APPLE)
    target_link_libraries(${EXAMPLE_SIMPLE_APP_NAME} PRIVATE
        "-framework IOKit"
        "-framework Cocoa"
        "-framework OpenGL"
    )
endif ()
