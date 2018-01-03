package(default_visibility = ["//visibility:public"])

load("//tools/bzl:asciidoc.bzl", "documentation_attributes")
load("//tools/bzl:asciidoc.bzl", "genasciidoc")
load("//tools/bzl:asciidoc.bzl", "genasciidoc_zip")

exports_files([
    "replace_macros.py",
])

filegroup(
    name = "prettify_files",
    srcs = [
        ":prettify.min.css",
        ":prettify.min.js",
    ],
)

genrule(
    name = "prettify_min_css",
    srcs = ["//resources/com/google/gerrit/prettify:client/prettify.css"],
    outs = ["prettify.min.css"],
    cmd = "cp $< $@",
)

genrule(
    name = "prettify_min_js",
    srcs = ["//resources/com/google/gerrit/prettify:client/prettify.js"],
    outs = ["prettify.min.js"],
    cmd = "cp $< $@",
)

filegroup(
    name = "resources",
    srcs = glob([
        "images/*.jpg",
        "images/*.png",
    ]) + [
        ":prettify_files",
    ],
    visibility = ["//visibility:public"],
)

DOC_DIR = "Documentation"

SRCS = glob(["*.txt"])

# For the same srcs, we can have multiple genasciidoc_zip rules, but only one
# genasciidoc rule. Because multiple genasciidoc rules will have conflicting
# output files.
genasciidoc(
    name = "Documentation",
    srcs = SRCS,
    attributes = documentation_attributes(),
    backend = "html5",
    visibility = ["//visibility:public"],
)

genasciidoc_zip(
    name = "html",
    srcs = SRCS,
    attributes = documentation_attributes(),
    backend = "html5",
    directory = DOC_DIR,
    visibility = ["//visibility:public"],
)

genasciidoc_zip(
    name = "searchfree",
    srcs = SRCS,
    attributes = documentation_attributes(),
    backend = "html5",
    directory = DOC_DIR,
    searchbox = False,
    visibility = ["//visibility:public"],
)
