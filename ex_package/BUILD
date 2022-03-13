load("@rules_python//python:defs.bzl", "py_binary")
load("@rules_proto//proto:defs.bzl", "proto_library")
load("@rules_proto_grpc//python:defs.bzl", "python_proto_library")

proto_library(
    name = "my_proto",
    srcs = ["my.proto"],
)

python_proto_library(
    name = "my_py_pb2",
    protos = [":my_proto"],
    srcs_version = "PY3",
)

py_binary(
  name = "a",
  srcs = ["a.py"],
  srcs_version = "PY3",
  deps = ["my_py_pb2"],
  legacy_create_init = False,
)

sh_binary(
    name = "b",
    srcs = ["b.sh"],
    deps = ["@bazel_tools//tools/bash/runfiles"],
    data = [":a"],
)

