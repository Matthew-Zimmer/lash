
target_include_directories(lash INTERFACE 
    $<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}> 
    $<INSTALL_INTERFACE:include/lash>)

set(headers 
    initializable.hpp
    operator_helpers.hpp
    reflection.hpp
    variables.hpp)

install(FILES ${headers} DESTINATION include/lash)