# Copyright 2020 The IREE Authors
#
# Licensed under the Apache License v2.0 with LLVM Exceptions.
# See https://llvm.org/LICENSE.txt for license information.
# SPDX-License-Identifier: Apache-2.0 WITH LLVM-exception

load("//build_tools/bazel:build_defs.oss.bzl", "iree_compiler_cc_library")

package(
    default_visibility = ["//visibility:public"],
    features = ["layering_check"],
    licenses = ["notice"],  # Apache 2.0
)

iree_compiler_cc_library(
    name = "Bytecode",
    srcs = [
        "ArchiveWriter.cpp",
        "ArchiveWriter.h",
        "BytecodeEncoder.cpp",
        "BytecodeEncoder.h",
        "BytecodeModuleTarget.cpp",
        "DebugDatabaseBuilder.cpp",
        "DebugDatabaseBuilder.h",
        "TranslationRegistration.cpp",
    ],
    hdrs = [
        "BytecodeModuleTarget.h",
    ],
    deps = [
        "//compiler/src/iree/compiler/Dialect/Util/IR",
        "//compiler/src/iree/compiler/Dialect/Util/Transforms",
        "//compiler/src/iree/compiler/Dialect/VM/Analysis",
        "//compiler/src/iree/compiler/Dialect/VM/IR",
        "//compiler/src/iree/compiler/Dialect/VM/Transforms",
        "//compiler/src/iree/compiler/Dialect/VM/Utils:CallingConvention",
        "//compiler/src/iree/compiler/Utils",
        "//runtime/src/iree/schemas:bytecode_module_def_c_fbs",
        "@llvm-project//llvm:Support",
        "@llvm-project//mlir:IR",
        "@llvm-project//mlir:Pass",
        "@llvm-project//mlir:Support",
        "@llvm-project//mlir:Transforms",
        "@llvm-project//mlir:TranslateLib",
    ],
)
