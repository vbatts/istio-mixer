load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "evaluator.go",
        "expr.go",
        "func.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/attribute:go_default_library",
        "//pkg/config/proto:go_default_library",
        "//pkg/pool:go_default_library",
        "@com_github_golang_glog//:go_default_library",
        "@com_github_hashicorp_go_multierror//:go_default_library",
        "@com_github_hashicorp_golang_lru//:go_default_library",
        "@io_istio_api//:mixer/v1/config/descriptor",
    ],
)

go_test(
    name = "go_default_test",
    size = "small",
    srcs = [
        "benchmark_test.go",
        "eval_test.go",
        "expr_test.go",
        "func_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "//pkg/attribute:go_default_library",
        "//pkg/config/proto:go_default_library",
        "@com_github_hashicorp_golang_lru//:go_default_library",
        "@io_istio_api//:mixer/v1/config/descriptor",
    ],
)
