project(metal-cpp LANGUAGES CXX)

add_library(${PROJECT_NAME} SHARED
    ${CMAKE_CURRENT_SOURCE_DIR}/Metal.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC
    "${CMAKE_CURRENT_SOURCE_DIR}/metal-cpp"
)

target_link_libraries(${PROJECT_NAME} PUBLIC
    "-framework Metal"
    "-framework Foundation"
    "-framework QuartzCore"
)