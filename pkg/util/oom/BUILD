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
        "oom.go",
        "oom_fake.go",
        "oom_linux.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//vendor:github.com/golang/glog",
        "//vendor:github.com/opencontainers/runc/libcontainer/cgroups/fs",
        "//vendor:github.com/opencontainers/runc/libcontainer/configs",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["oom_linux_test.go"],
    library = "go_default_library",
    tags = ["automanaged"],
    deps = ["//vendor:github.com/stretchr/testify/assert"],
)
