cmake_minimum_required (VERSION 3.7.0)
project(problem_65)

add_executable(problem_65 main.cpp)

if(UNIX)
  find_package(Threads REQUIRED)
  target_link_libraries(problem_65 Threads::Threads)
endif()

set_target_properties (problem_65 PROPERTIES FOLDER "07.Concurrency")