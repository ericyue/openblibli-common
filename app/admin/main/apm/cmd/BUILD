package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)

go_binary(
    name = "cmd",
    embed = [":go_default_library"],
    tags = ["automanaged"],
)

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    data = ["apm-admin-test.toml"],
    importpath = "go-common/app/admin/main/apm/cmd",
    tags = ["automanaged"],
    deps = [
        "//app/admin/main/apm/conf:go_default_library",
        "//app/admin/main/apm/http:go_default_library",
        "//app/admin/main/apm/service:go_default_library",
        "//library/ecode/tip:go_default_library",
        "//library/log:go_default_library",
        "//library/os/signal:go_default_library",
        "//library/queue/databus/report:go_default_library",
        "//library/syscall:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
