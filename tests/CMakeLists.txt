
add_executable(test_opaquePointer
    main.cpp)

target_link_libraries(test_opaquePointer treasureV2_static)

set_property(TARGET test_opaquePointer
    PROPERTY CXX_STANDARD 11)

setup_target_for_coverage(
    NAME test_op_cov
    EXECUTABLE test_opaquePointer
)

install(TARGETS test_opaquePointer
    LIBRARY DESTINATION ${CMAKE_BINARY_DIR}/test
    RUNTIME DESTINATION ${CMAKE_BINARY_DIR}/test)
