cmake_minimum_required(VERSION 3.10.0)

project(elec1601 VERSION 0.1.0 LANGUAGES C)
find_package(SDL2 REQUIRED)
set(SOURCES_FILE src)

add_executable(elec1601 WIN32 
${SOURCES_FILE}/formulas.c 
${SOURCES_FILE}/main.c 
${SOURCES_FILE}/robot.c 
${SOURCES_FILE}/wall.c)

target_include_directories(elec1601 PRIVATE ${PROJECT_SOURCE_DIR}/include)
target_link_libraries(elec1601 m SDL2)
add_definitions(-DSDL_MAIN_HANDLED)