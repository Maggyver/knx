cmake_minimum_required(VERSION 2.7)
project(knx-linux)
set(LIBRARIES_FROM_REFERENCES "")
add_executable(knx-linux 
	../src/knx/address_table_object.cpp 
	../src/knx/apdu.cpp 
	../src/knx/application_layer.cpp 
	../src/knx/application_program_object.cpp 
	../src/knx/association_table_object.cpp 
	../src/knx/bau.cpp 
	../src/knx/bau07B0.cpp 
	../src/knx/bau57B0.cpp 
	../src/knx/bau_systemB.cpp 
	../src/knx/bits.cpp 
	../src/knx/cemi_frame.cpp 
	../src/knx/data_link_layer.cpp 
	../src/knx/device_object.cpp 
	../src/knx/group_object.cpp 
	../src/knx/group_object_table_object.cpp 
	../src/knx/interface_object.cpp 
	../src/knx/ip_data_link_layer.cpp 
	../src/knx/ip_parameter_object.cpp 
	../src/knx/memory.cpp 
	../src/knx/network_layer.cpp 
	../src/knx/npdu.cpp 
	../src/knx/table_object.cpp 
	../src/knx/tpdu.cpp 
	../src/knx/tpuart_data_link_layer.cpp 
	../src/knx/transport_layer.cpp 
	../src/knx/platform.cpp 
	main.cpp 
	../src/linux_platform.cpp 
	../src/knx_facade.cpp 
	../src/knx/dptconvert.cpp
	../src/knx/knx_value.cpp
	../src/knx/dpt.cpp)
target_link_libraries(knx-linux  "${LIBRARIES_FROM_REFERENCES}")
include_directories(../src)
set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -Wall -Wno-unknown-pragmas -Wno-switch -g -O0")
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -Wall -Wno-unknown-pragmas -Wno-switch -g -O0")
