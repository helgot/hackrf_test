load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_foreign_cc",
    # TODO: Get the latest sha256 value from the latest release on the releases page
    #       https://github.com/bazelbuild/rules_foreign_cc/releases
    #
    # sha256 = "...",
    sha256 = "4b33d62cf109bcccf286b30ed7121129cc34cf4f4ed9d8a11f38d9108f40ba74",
    strip_prefix = "rules_foreign_cc-0.11.1",
    url = "https://github.com/bazelbuild/rules_foreign_cc/archive/refs/tags/0.11.1.tar.gz",
)

load("@rules_foreign_cc//foreign_cc:repositories.bzl", "rules_foreign_cc_dependencies")

rules_foreign_cc_dependencies()

_ALL_CONTENT = """\
filegroup(
    name = "all_srcs",
    srcs = glob(["**"]),
    visibility = ["//visibility:public"],
)
"""

http_archive(
    name = "libhackrf",
    build_file_content = _ALL_CONTENT,
    urls = ["https://github.com/greatscottgadgets/hackrf/archive/refs/tags/v2024.02.1.tar.gz"],
    sha256 = "16e4707b80d0d16db3a9e2149745d7a1bc253dea88c9c542d3ae062df5cbd9e3",
    strip_prefix = "hackrf-2024.02.1/host",
)

http_archive(
    name = "libusb",
    build_file_content = _ALL_CONTENT,
    urls = ["https://github.com/libusb/libusb/archive/refs/tags/v1.0.27.tar.gz"],
   sha256 = "e8f18a7a36ecbb11fb820bd71540350d8f61bcd9db0d2e8c18a6fb80b214a3de",
    strip_prefix = "libusb-1.0.27",
)
