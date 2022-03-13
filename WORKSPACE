workspace(name = "my_test")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Google proto

http_archive(
    name = "rules_proto_grpc",
   sha256 = "4202a150910712d00d95f11e240ad6da4c92e542d3b9fbb5b3a3d60abba3de77",
    strip_prefix = "rules_proto_grpc-4.0.0",
    urls = ["https://github.com/rules-proto-grpc/rules_proto_grpc/archive/4.0.0.tar.gz"],
)

load("@rules_proto_grpc//:repositories.bzl", "rules_proto_grpc_toolchains", "rules_proto_grpc_repos")
rules_proto_grpc_toolchains()
rules_proto_grpc_repos()

load("@rules_proto//proto:repositories.bzl", "rules_proto_dependencies", "rules_proto_toolchains")
rules_proto_dependencies()
rules_proto_toolchains()

load("@rules_proto_grpc//python:repositories.bzl", rules_proto_grpc_python_repos = "python_repos")
rules_proto_grpc_python_repos()

# End Google proto

