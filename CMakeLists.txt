# Stubs for the pico-sdk with intent of supporting RPI Pico based projects in a way that can be simulated on a host machine.
# Related Project: https://github.com/brandonbraun653/pico-mock

file(GLOB SIM_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)
add_library(pico_lib_sim STATIC ${SIM_SOURCES})
target_link_libraries(pico_lib_sim PRIVATE pico_mock_headers)
