set(LLVM_REQUIRES_RTTI ON)
set(LLVM_REQUIRES_EH ON)


kllvm_add_tool(parser
  main.cpp
)

target_link_libraries(parser Parser AST)

add_definitions(${LLVM_DEFINITIONS})
