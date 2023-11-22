# create RlImGui target (INTERFACE library) that exposes headers and source.
add_library(RlImGui INTERFACE)

# add header directory to RlImGui INTERFACE library
target_include_directories(RlImGui
    INTERFACE ${RLIMGUI_INCLUDE_DIR}
)

# add source to RlImGui INTERFACE library
target_sources(RlImGui INTERFACE
    ${RLIMGUI_INCLUDE_DIR}/rlImGui.cpp
)