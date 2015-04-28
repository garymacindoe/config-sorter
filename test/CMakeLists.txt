include_directories(${gtest_SOURCE_DIR}/include ${config-sorter_SOURCE_DIR}/include)
set(test_sources

)
add_executable(test_config-sorter ${test_sources})
target_link_libraries(test_config-sorter gtest_main)

add_test(test_config-sorter test_config-sorter)
