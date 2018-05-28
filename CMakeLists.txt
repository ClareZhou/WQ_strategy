cmake_minimum_required(VERSION 3.10)
project(test222)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -g -pthread -lgtest")
set(SRC ${PROJECT_SOURCE_DIR}/main.cpp)
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)
set(CMAKE_EXE_LINKER_FLAGS "-pthread -lgtest")
set(SHARE_LIB_PREFIX /usr/local)
set(CMAKE_CXX_STANDARD 11)

LINK_DIRECTORIES(
        ${PROJECT_SOURCE_DIR}/lib
        /usr/local/lib
        /usr/lib
)



INCLUDE_DIRECTORIES(
        #        ${PROJECT_SOURCE_DIR}/include
        /usr/local/include
        /usr/include
)




link_directories(${LINK_DIRECTORIES})
add_executable(test222 ${SRC})
target_link_libraries(test222 -lpthread -lgtest)
