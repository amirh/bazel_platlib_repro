load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

rules_python_version = "c37ba2215eccab53ae1da5f827a335281f81b9e1" # Latest @ 2021-03-11

http_archive(
    name = "rules_python",
    sha256 = "c1de63ef53c7dfea9107dfb8b824dbd33669557ae6ca1950e2543d6436e6d42e",
    strip_prefix = "rules_python-{}".format(rules_python_version),
    url = "https://github.com/bazelbuild/rules_python/archive/{}.zip".format(rules_python_version),
)
load("@rules_python//python:pip.bzl", "pip_install")

pip_install(
   name = "repro_deps",
   requirements = "//repro:requirements.txt",
)
