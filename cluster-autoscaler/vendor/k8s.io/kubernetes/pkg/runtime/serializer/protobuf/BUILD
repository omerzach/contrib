package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
    "go_test",
    "cgo_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "protobuf.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/runtime:go_default_library",
        "//pkg/runtime/schema:go_default_library",
        "//pkg/runtime/serializer/recognizer:go_default_library",
        "//pkg/util/framer:go_default_library",
        "//vendor:github.com/gogo/protobuf/proto",
    ],
)

go_test(
    name = "go_default_xtest",
    srcs = ["protobuf_test.go"],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/install:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/runtime:go_default_library",
        "//pkg/runtime/schema:go_default_library",
        "//pkg/runtime/serializer/protobuf:go_default_library",
        "//pkg/util/diff:go_default_library",
    ],
)
