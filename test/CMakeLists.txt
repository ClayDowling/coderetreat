enable_testing()

SET(UNIT_UNDER_TEST
    ../src/rules.cpp
)

INCLUDE_DIRECTORIES(../src)
SET(TEST_NAME test-${PROJECT_NAME})

ADD_EXECUTABLE(${TEST_NAME}
    ${UNIT_UNDER_TEST}
    test_rules.cpp
)

TARGET_LINK_LIBRARIES(${TEST_NAME}
    gtest_main
)