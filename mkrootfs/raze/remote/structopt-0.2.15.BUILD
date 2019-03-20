"""
cargo-raze crate build file.

DO NOT EDIT! Replaced on runs of cargo-raze
"""
package(default_visibility = [
  # Public for visibility by "@raze__crate__version//" targets.
  #
  # Prefer access through "//mkrootfs/raze", which limits external
  # visibility to explicit Cargo.toml dependencies.
  "//visibility:public",
])

licenses([
  "notice", # "Apache-2.0,MIT"
])

load(
    "@io_bazel_rules_rust//rust:rust.bzl",
    "rust_library",
    "rust_binary",
    "rust_test",
)


# Unsupported target "argument_naming" with type "test" omitted
# Unsupported target "arguments" with type "test" omitted
# Unsupported target "at_least_two" with type "example" omitted
# Unsupported target "author_version_about" with type "test" omitted
# Unsupported target "basic" with type "example" omitted
# Unsupported target "custom-string-parsers" with type "test" omitted
# Unsupported target "deny-warnings" with type "test" omitted
# Unsupported target "deny_missing_docs" with type "example" omitted
# Unsupported target "doc-comments-help" with type "test" omitted
# Unsupported target "doc_comments" with type "example" omitted
# Unsupported target "enum_in_args" with type "example" omitted
# Unsupported target "enum_tuple" with type "example" omitted
# Unsupported target "example" with type "example" omitted
# Unsupported target "flags" with type "test" omitted
# Unsupported target "flatten" with type "example" omitted
# Unsupported target "flatten" with type "test" omitted
# Unsupported target "git" with type "example" omitted
# Unsupported target "group" with type "example" omitted
# Unsupported target "keyvalue" with type "example" omitted
# Unsupported target "nested-subcommands" with type "test" omitted
# Unsupported target "no_version" with type "example" omitted
# Unsupported target "options" with type "test" omitted
# Unsupported target "privacy" with type "test" omitted
# Unsupported target "raw_attributes" with type "example" omitted
# Unsupported target "raw_attributes" with type "test" omitted
# Unsupported target "rename_all" with type "example" omitted
# Unsupported target "simple_group" with type "example" omitted

rust_library(
    name = "structopt",
    crate_root = "src/lib.rs",
    crate_type = "lib",
    edition = "2015",
    srcs = glob(["**/*.rs"]),
    deps = [
        "@raze__clap__2_32_0//:clap",
        "@raze__structopt_derive__0_2_15//:structopt_derive",
    ],
    rustc_flags = [
        "--cap-lints=allow",
    ],
    version = "0.2.15",
    crate_features = [
        "clap",
        "default",
    ],
)

# Unsupported target "subcommand_aliases" with type "example" omitted
# Unsupported target "subcommands" with type "test" omitted
