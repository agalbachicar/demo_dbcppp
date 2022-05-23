cmake_minimum_required(VERSION 3.12)
project(demo_dbcpp)

if(NOT CMAKE_C_STANDARD)
  set(CMAKE_C_STANDARD 99)
endif()

if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 17)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(libdbcppp REQUIRED)

add_executable(demo_dbcppp
  src/demo_dbcppp.cc
)
target_link_libraries(demo_dbcppp
  libdbcppp
)

install(
  TARGETS demo_dbcppp
  EXPORT ${PROJECT_NAME}-targets
  ARCHIVE DESTINATION lib
  LIBRARY DESTINATION lib
  RUNTIME DESTINATION bin
)
