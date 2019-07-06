cmake_minimum_required (VERSION 3.7.0)
project(problem_64)

add_executable(problem_64 main.cpp)

if(UNIX)
  find_package(Threads REQUIRED)
  target_link_libraries(problem_64 Threads::Threads)
endif()

set_target_properties (problem_64 PROPERTIES FOLDER "07.Concurrency")