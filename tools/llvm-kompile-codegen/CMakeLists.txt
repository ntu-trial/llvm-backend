set(LLVM_REQUIRES_RTTI ON)
set(LLVM_REQUIRES_EH ON)
kllvm_add_tool(llvm-kompile-codegen
  main.cpp
)

target_link_libraries(llvm-kompile-codegen Codegen Parser AST gmp yaml-cpp)

llvm_config(llvm-kompile-codegen
  ${LLVM_TARGETS_TO_BUILD}
)

add_definitions(${LLVM_DEFINITIONS})
