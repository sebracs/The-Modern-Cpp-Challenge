cmake_minimum_required (VERSION 3.7.0)
project(problem_43)

add_definitions(-DINSTALL=${LIBS_PATH}/date)
include_directories(${LIBS_PATH}/date/include/date)
include_directories(${LIBS_PATH}/date/include)

add_executable(problem_43 ${LIBS_PATH}/date/src/tz.cpp main.cpp)

if (UNIX)
  set(CURL_LIBRARY "-lcurl")
  find_package(CURL REQUIRED)
  include_directories(${CURL_INCLUDE_DIR})
  target_link_libraries(problem_43 ${CURL_LIBRARIES})
endif()

set_target_properties (problem_43 PROPERTIES FOLDER "05.Datetime")
