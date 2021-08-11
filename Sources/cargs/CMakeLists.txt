# Target name
set(target cargs)
set(ROOT_DIR ${PROJECT_SOURCE_DIR})
set(PUBLIC_HDR_DIR ${PROJECT_SOURCE_DIR}/Includes/cargs)
set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR})

# Set public headers
set(PUBLIC_HDRS
    ${PUBLIC_HDR_DIR}/cargs.hpp
)

# Set Sources
set(SRCS
    ${SRC_DIR}/cargs.cpp
)

# Build library
add_library(${target} ${SRCS})

# Project options
set_target_properties(${target}
    PROPERTIES
    ${DEFAULT_PROJECT_OPTIONS}
    PUBLIC_HEADER "${PUBLIC_HDRS}"
)

#Include directories
target_include_directories(${target}
    PUBLIC
    $<BUILD_INTERFACE:${PUBLIC_HDR_DIR}>
    $<INSTALL_INTERFACE:${CMAKE_INSTALL_PREFIX}/include>
    PRIVATE
    ${PUBLIC_HDR_DIR}
)

# Compile options
target_compile_options(${target}
    PRIVATE
    ${DEFAULT_COMPILE_OPTIONS}
)

# Link libraries
target_link_libraries(${target}
    PUBLIC
    ${DEFAULT_LINKER_OPTIONS}
	${DEFAULT_LIBRARIES}
)

# Compile definitions
target_compile_definitions(${target}
    PRIVATE
    ${DEFAULT_COMPILE_DEFINITIONS}
)

# Install
install(TARGETS  ${target}
        EXPORT   ${target}-config
        RUNTIME  DESTINATION bin
        LIBRARY  DESTINATION lib
        ARCHIVE  DESTINATION lib
        PUBLIC_HEADER DESTINATION include
)
install(EXPORT   ${target}-config
        DESTINATION share/${target}
)