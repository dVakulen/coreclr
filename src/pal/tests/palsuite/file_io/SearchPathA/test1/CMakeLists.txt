cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  SearchPathA.c
)

add_executable(paltest_searchpatha_test1
  ${SOURCES}
)

add_dependencies(paltest_searchpatha_test1 CoreClrPal)

target_link_libraries(paltest_searchpatha_test1
  pthread
  rt
  m
  CoreClrPal
)
