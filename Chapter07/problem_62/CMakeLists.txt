cmake_minimum_required (VERSION 3.7.0)
project(problem_62)

add_executable(problem_62 main.cpp)

if(UNIX)
  find_package(Threads REQUIRED)
  target_link_libraries(problem_62 Threads::Threads)
endif()

set_target_properties (problem_62 PROPERTIES FOLDER "07.Concurrency")