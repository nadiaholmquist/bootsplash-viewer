cmake_minimum_required(VERSION 2.6.0)
project(bootsplash-viewer C)

find_package(PkgConfig REQUIRED)
pkg_check_modules(SDL2 REQUIRED sdl2)

add_executable(bootsplash-viewer bootsplash-viewer.c)
target_include_directories(bootsplash-viewer PRIVATE ${SDL2_INCLUDE_DIRS} .)
target_link_libraries(bootsplash-viewer ${SDL2_LIBRARIES})
install(TARGETS bootsplash-viewer RUNTIME DESTINATION ${CMAKE_INSTALL_PREFIX}/bin)
