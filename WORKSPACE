# Needed for pip dependencies
git_repository(
    name = "io_bazel_rules_python",
    remote = "https://github.com/bazelbuild/rules_python.git",
    commit = "e003509e52a116f6431883f6a77115ec0d1a323f",
)
load("@io_bazel_rules_python//python:pip.bzl", "pip_repositories")
pip_repositories()

load("@io_bazel_rules_python//python:pip.bzl", "pip_import")

pip_import(
  name = "deps",
  requirements = "//:requirements.txt"
)
load("@deps//:requirements.bzl", "pip_install")
pip_install()

