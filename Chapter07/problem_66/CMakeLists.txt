cmake_minimum_required (VERSION 3.7.0)
project(problem_66)

add_executable(problem_66 main.cpp)

if(UNIX)
  find_package(Threads REQUIRED)
  target_link_libraries(problem_66 Threads::Threads)
endif()

set_target_properties (problem_66 PROPERTIES FOLDER "07.Concurrency")