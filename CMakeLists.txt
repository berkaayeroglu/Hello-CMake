cmake_minimum_required(VERSION "3.27.1")

project("HelloWord")

add_executable("${PROJECT_NAME}" "Main.cpp")

install(TARGETS "${PROJECT_NAME}" DESTINATION bin)
install(FILES "Main.cpp" DESTINATION src)

include(CTest)

add_test("test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")
