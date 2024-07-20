add_compile_options(-fexceptions)

add_llvm_component_library(LLVMZK
        FieldArithmetics.cpp
        ADDITIONAL_HEADER_DIRS
        ${LLVM_MAIN_INCLUDE_DIR}/llvm/ZK

        LINK_LIBS
        crypto3::algebra
        crypto3::block
        crypto3::blueprint
        crypto3::codec
        crypto3::math
        crypto3::multiprecision
        crypto3::pkpad
        crypto3::pubkey
        crypto3::random
        crypto3::zk
        crypto3::marshalling-core
        crypto3::marshalling-algebra
        crypto3::marshalling-multiprecision
        crypto3::marshalling-zk

        LINK_COMPONENTS
        Support
)
