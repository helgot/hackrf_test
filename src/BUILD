cc_binary(
	name = "hello-world",
	srcs = ["main.cpp"],
	deps = [":Libhackrf"],
)

load("@rules_foreign_cc//foreign_cc:defs.bzl", "cmake")

cmake(
    name = "Libhackrf",
    lib_source = "@libhackrf//:all_srcs",
    out_shared_libs = ["libhackrf.so.0.9.0"],
)
