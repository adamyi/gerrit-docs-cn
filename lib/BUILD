exports_files(glob([
    "LICENSE-*",
]))

filegroup(
    name = "all-licenses",
    srcs = glob(
        ["LICENSE-*"],
        exclude = ["LICENSE-DO_NOT_DISTRIBUTE"],
    ),
    visibility = ["//visibility:public"],
)

java_library(
    name = "guava",
    data = ["//lib:LICENSE-Apache2.0"],
    visibility = ["//visibility:public"],
    exports = ["@guava//jar"],
    runtime_deps = [":j2objc"],
)

java_library(
    name = "args4j",
    data = ["//lib:LICENSE-args4j"],
    visibility = ["//visibility:public"],
    exports = ["@args4j//jar"],
)

java_library(
    name = "j2objc",
    data = ["//lib:LICENSE-Apache2.0"],
    visibility = ["//visibility:public"],
    exports = ["@j2objc//jar"],
)
