load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "policy.go",
        "privkey.go",
        "randomreader.go",
        "sign_cookie.go",
        "sign_url.go",
    ],
    importpath = "github.com/aws/aws-sdk-go/service/cloudfront/sign",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = [
        "policy_test.go",
        "privkey_test.go",
        "sign_cookie_example_test.go",
        "sign_cookie_test.go",
        "sign_url_test.go",
    ],
    importpath = "github.com/aws/aws-sdk-go/service/cloudfront/sign",
    library = ":go_default_library",
    deps = ["//vendor/github.com/stretchr/testify/assert:go_default_library"],
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
