cmake_minimum_required(VERSION 3.12)

add_subdirectory(external/fmt EXCLUDE_FROM_ALL)

set(my_project_name "cpp_starter")
set(my_project_description "Project description")
set(my_project_version 0.1.0)
set(my_project_lib ${my_project_name}_lib)
set(my_project_exe ${my_project_name}_exe)

project(${my_project_name} DESCRIPTION ${my_project_description} VERSION ${my_project_version})

option(BUILD_TESTING "Build tests for ${my_project_name}" OFF)
if (BUILD_TESTING)
    enable_testing()
    add_subdirectory(tests)
endif ()

add_executable(${my_project_exe} src/main.cpp)
target_link_libraries(${my_project_exe} PRIVATE fmt::fmt)
