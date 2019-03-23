workspace(name = "minimal_linux_bazel")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Kernel and drivers
load("//:kernel.bzl", "kernel_driver", "kernel_repository")

KERNEL_SHA256 = "5b22a60437f2604166679c29a08b51b4a6696829378a60ab745ae9f5a0b2d932"

KERNEL_NAME = "5.0.2.arch1-1-x86_64"

kernel_repository(KERNEL_NAME, KERNEL_SHA256)

kernel_driver("e1000", "net/ethernet/intel/e1000", KERNEL_NAME, KERNEL_SHA256)

# Rust stuff
http_archive(
    name = "io_bazel_rules_rust",
    sha256 = "c82118824b2448b77146f1dae97b6eaa717babedad0822aca4879f3cbbf2b7b5",
    strip_prefix = "rules_rust-3228ccd3814c2ad0d7307d2f87fb8ff9616149d7",
    urls = [
        # Master branch as of 2018-12-11
        "https://github.com/bazelbuild/rules_rust/archive/3228ccd3814c2ad0d7307d2f87fb8ff9616149d7.tar.gz",
    ],
)

http_archive(
    name = "bazel_skylib",
    sha256 = "eb5c57e4c12e68c0c20bc774bfbc60a568e800d025557bc4ea022c6479acc867",
    strip_prefix = "bazel-skylib-0.6.0",
    url = "https://github.com/bazelbuild/bazel-skylib/archive/0.6.0.tar.gz",
)

load("@io_bazel_rules_rust//:workspace.bzl", "bazel_version")

bazel_version(name = "bazel_version")

load("@io_bazel_rules_rust//rust:repositories.bzl", "rust_repository_set")

rust_repository_set(
    name = "rust_linux_x86_64",
    exec_triple = "x86_64-unknown-linux-gnu",
    extra_target_triples = [],
    version = "1.33.0",
)

load("//:fetch.bzl", "fetch_dependencies")

fetch_dependencies()
