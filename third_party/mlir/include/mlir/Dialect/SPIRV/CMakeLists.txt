set(LLVM_TARGET_DEFINITIONS SPIRVOps.td)
mlir_tablegen(SPIRVOps.h.inc -gen-op-decls)
mlir_tablegen(SPIRVOps.cpp.inc -gen-op-defs)
add_public_tablegen_target(MLIRSPIRVOpsIncGen)

set(LLVM_TARGET_DEFINITIONS SPIRVGLSLOps.td)
mlir_tablegen(SPIRVGLSLOps.h.inc -gen-op-decls)
mlir_tablegen(SPIRVGLSLOps.cpp.inc -gen-op-defs)
add_public_tablegen_target(MLIRSPIRVGLSLOpsIncGen)

set(LLVM_TARGET_DEFINITIONS SPIRVBase.td)
mlir_tablegen(SPIRVEnums.h.inc -gen-enum-decls)
mlir_tablegen(SPIRVEnums.cpp.inc -gen-enum-defs)
add_public_tablegen_target(MLIRSPIRVEnumsIncGen)

set(LLVM_TARGET_DEFINITIONS SPIRVOps.td)
mlir_tablegen(SPIRVSerialization.inc -gen-spirv-serialization)
add_public_tablegen_target(MLIRSPIRVSerializationGen)

set(LLVM_TARGET_DEFINITIONS SPIRVBase.td)
mlir_tablegen(SPIRVOpUtils.inc -gen-spirv-op-utils)
add_public_tablegen_target(MLIRSPIRVOpUtilsGen)
