find_package(Threads)
add_executable(tcp_echo_server main.cpp)
target_link_libraries(tcp_echo_server ${CMAKE_THREAD_LIBS_INIT})
if(HAIKU)
	target_link_libraries(tcp_echo_server network)
endif(HAIKU)
