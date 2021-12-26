cmake_minimum_required(VERSION 3.10)
#set(CMAKE_C_COMPILER "gcc.exe")
#set(CMAKE_CXX_COMPILER "g++.exe")
#starts new cmake project. detects default c and c++ compiler
project(helloworld)

add_executable("${PROJECT_NAME}" main.cpp)

install(TARGETS "${PROJECT_NAME}" DESTINATION bin) 
#add_subdirectory(include)
install(FILES "main.cpp" DESTINATION src) #${CMAKE_INSTALL_PREFIX}/src
#build target app created. invokes the compiler to compile an executable app from given source file main and foo
include(CTest)

add_test("test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")



