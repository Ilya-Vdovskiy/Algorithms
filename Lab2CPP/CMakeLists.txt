add_executable(Lab2CPP lab2.cpp lab2.h main.cpp)
target_include_directories(Lab2CPP PUBLIC ../LibraryCPP)
target_link_libraries(Lab2CPP LibraryCPP)

add_executable(TestTasks ../tests/test_task2.cpp lab2.cpp)
target_include_directories(TestTasks PUBLIC .)
target_include_directories(TestTasks PUBLIC ../LibraryCPP)
target_link_libraries(TestTasks LibraryCPP)
add_test(TestTasks TestTasks ${CMAKE_SOURCE_DIR}/tests/input_test_task2.txt)