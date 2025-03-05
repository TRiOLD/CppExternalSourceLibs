cmake_minimum_required(VERSION 3.10)
project(alglib)

set(ALGLIB_DIR ${CMAKE_CURRENT_SOURCE_DIR})

set(ALGLIB_FILES
    ${ALGLIB_DIR}/source/alglibinternal.cpp
    ${ALGLIB_DIR}/source/alglibmisc.cpp
    ${ALGLIB_DIR}/source/ap.cpp
    ${ALGLIB_DIR}/source/dataanalysis.cpp
    ${ALGLIB_DIR}/source/diffequations.cpp
    ${ALGLIB_DIR}/source/fasttransforms.cpp
    ${ALGLIB_DIR}/source/integration.cpp
    ${ALGLIB_DIR}/source/interpolation.cpp
    ${ALGLIB_DIR}/source/kernels_avx2.cpp
    ${ALGLIB_DIR}/source/kernels_fma.cpp
    ${ALGLIB_DIR}/source/kernels_sse2.cpp
    ${ALGLIB_DIR}/source/linalg.cpp
    ${ALGLIB_DIR}/source/optimization.cpp
    ${ALGLIB_DIR}/source/solvers.cpp
    ${ALGLIB_DIR}/source/specialfunctions.cpp
    ${ALGLIB_DIR}/source/statistics.cpp
)

add_library(alglib SHARED ${ALGLIB_FILES})
target_include_directories(alglib PUBLIC ${ALGLIB_DIR}/include)