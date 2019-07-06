cmake_minimum_required (VERSION 3.7.0)
project(problem_61)

add_executable(problem_61 main.cpp)

if(UNIX)
  find_package(Threads REQUIRED)
  target_link_libraries(problem_61 Threads::Threads)
endif()

set_target_properties (problem_61 PROPERTIES FOLDER "07.Concurrency")