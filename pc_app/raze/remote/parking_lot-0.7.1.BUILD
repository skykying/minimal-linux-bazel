"""
cargo-raze crate build file.

DO NOT EDIT! Replaced on runs of cargo-raze
"""
package(default_visibility = [
  # Public for visibility by "@raze__crate__version//" targets.
  #
  # Prefer access through "//raze", which limits external
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



rust_library(
    name = "parking_lot",
    crate_root = "src/lib.rs",
    crate_type = "lib",
    edition = "2015",
    srcs = glob(["**/*.rs"]),
    deps = [
        "@raze__lock_api__0_1_5//:lock_api",
        "@raze__parking_lot_core__0_4_0//:parking_lot_core",
    ],
    rustc_flags = [
        "--cap-lints=allow",
    ],
    version = "0.7.1",
    crate_features = [
        "default",
        "lock_api",
        "owning_ref",
    ],
)

