project(benchmark)

find_package(Threads REQUIRED)

add_library(${PROJECT_NAME} INTERFACE IMPORTED GLOBAL)
file(GLOB_RECURSE LIBS "./lib/x86_64-linux-gnu/*.a")
target_link_libraries(${PROJECT_NAME} INTERFACE ${LIBS} Threads::Threads)
target_include_directories(${PROJECT_NAME} INTERFACE include)
