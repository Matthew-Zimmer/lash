cmake_minimum_required(VERSION 3.13)

project(lash)

add_library(lash)

add_subdirectory(include)
add_subdirectory(src)
# add_subdirectory(test)

target_compile_features(lash INTERFACE cxx_std_20)

# set(CMAKE_CXX_FLAGS "-Wall" "-Wextra")

install(TARGETS lash EXPORT lash DESTINATION lib/lash)
install(EXPORT lash DESTINATION lib/lash)
install(FILES lash-config.cmake DESTINATION lib/lash)