cmake_minimum_required(VERSION 3.15)
project(CrowServer)

# Include vcpkg toolchain
set(CMAKE_TOOLCHAIN_FILE "${CMAKE_SOURCE_DIR}/vcpkg/scripts/buildsystems/vcpkg.cmake")

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)

# Define the executable
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/output")
add_executable(CrowServer src/main.cpp)

# Find packages
find_package(Crow CONFIG REQUIRED)

# Link Crow
target_link_libraries(CrowServer PRIVATE Crow::Crow)
