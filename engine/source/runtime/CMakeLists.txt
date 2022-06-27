set(TARGET_NAME MatrixRuntime)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

file(GLOB_RECURSE HEADER_FILES CONFIGURE_DEPENDS *.h)
file(GLOB_RECURSE SOURCE_FILES CONFIGURE_DEPENDS *.cpp *.c)

source_group(TREE "${CAMKE_CURRENT_SOURCE_DIR}" FILES ${HEADER_FILES} ${SOURCE_FILES})

add_executable(${TARGET_NAME} ${HEADER_FILES} ${SOURCE_FILES})

set_target_properties(${TARGET_NAME} PROPERTIES FOLDER "Engine")

target_link_libraries(${TARGET_NAME} PUBLIC glfw)

target_link_directories(${TARGET_NAME} PUBLIC glm)

target_include_directories(${TARGET_NAME} PRIVATE glad/include)