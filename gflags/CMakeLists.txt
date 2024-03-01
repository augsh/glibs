project(gflags)

add_library(${PROJECT_NAME} INTERFACE IMPORTED GLOBAL)
file(GLOB_RECURSE LIBS "./lib/lib*")
target_link_libraries(${PROJECT_NAME} INTERFACE ${LIBS})
target_include_directories(${PROJECT_NAME} INTERFACE include)

add_files(${OUT_3RDLIB} "lib/lib*")
