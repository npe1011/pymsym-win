cmake_minimum_required(VERSION 3.15)
project(pymsym_c_lib C)

include(GenerateExportHeader)

set(SRCS
    src/msym.c
    src/basis_function.c
    src/character_table.c
    src/context.c
    src/debug.c
    src/elements.c
    src/equivalence_set.c
    src/geometry.c
    src/linalg.c
    src/msym_error.c
    src/permutation.c
    src/point_group.c
    src/rsh.c
    src/subspace.c
    src/symmetrize.c
    src/symmetry.c
    src/symop.c
)

add_library(pymsym SHARED ${SRCS})

generate_export_header(pymsym
    BASE_NAME msym
    EXPORT_FILE_NAME msym_EXPORTS.h
)

target_include_directories(pymsym PRIVATE 
    include 
    src 
    ${CMAKE_CURRENT_BINARY_DIR}
)

if(MINGW)
    target_link_options(pymsym PRIVATE -static -static-libgcc)
endif()
