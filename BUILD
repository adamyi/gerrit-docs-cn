genrule(
    name = "gen_version",
    outs = ["version.txt"],
    cmd = ("cat bazel-out/volatile-status.txt bazel-out/stable-status.txt | " +
           "grep STABLE_BUILD_CNDOC_LABEL | cut -d ' ' -f 2 > $@"),
    stamp = 1,
    visibility = ["//visibility:public"],
)
