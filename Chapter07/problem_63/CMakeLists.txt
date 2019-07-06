cmake_minimum_required (VERSION 3.7.0)
project(problem_63)

add_executable(problem_63 main.cpp)

if(UNIX)
  find_package(Threads REQUIRED)
  target_link_libraries(problem_63 Threads::Threads)
endif()

set_target_properties (problem_63 PROPERTIES FOLDER "07.Concurrency")