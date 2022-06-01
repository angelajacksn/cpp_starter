function(define_tests test_name)
    add_executable(${test_name} ${test_name}.cpp)
    target_link_libraries(${test_name} PRIVATE ${my_project_lib})
    add_test(NAME ${test_name} COMMAND ${test_name})
endfunction()

# Add tests here
