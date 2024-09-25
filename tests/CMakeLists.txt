include_directories(${CMAKE_SOURCE_DIR} ${CMAKE_SOURCE_DIR}/tests)

add_executable(main_test thread.c tests-core-atomic.c)
add_executable(atomicity_test thread.c atomicity.c)
add_executable(spmc_test thread.c spmc.c)

if(APPLE)
    target_compile_options(main_test PUBLIC -Wno-incompatible-pointer-types)
    target_compile_options(atomicity_test PUBLIC -Wno-incompatible-pointer-types)
    target_compile_options(spmc_test PUBLIC -Wno-incompatible-pointer-types)
endif()

add_test(NAME main_test COMMAND main_test)
add_test(NAME atomicity_test COMMAND atomicity_test)
add_test(NAME spmc_test COMMAND spmc_test)
