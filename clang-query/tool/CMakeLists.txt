if(HAVE_LIBEDIT)
  include_directories(${CMAKE_CURRENT_SOURCE_DIR}/..)

  add_clang_executable(clang-query ClangQuery.cpp)
  target_link_libraries(clang-query
    edit
    clangFrontend
    clangQuery
    clangTooling
    )
endif()
