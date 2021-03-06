# TensorFlow Quantitative Finance general math functions.

licenses(["notice"])

package(default_visibility = ["//tf_quant_finance:__subpackages__"])

py_library(
    name = "math",
    srcs = ["__init__.py"],
    srcs_version = "PY3",
    deps = [
        ":diff_ops",
        ":gradient",
        ":piecewise",
        ":root_search",
        ":segment_ops",
        "//tf_quant_finance/math/integration",
        "//tf_quant_finance/math/interpolation",
        "//tf_quant_finance/math/optimizer",
        "//tf_quant_finance/math/pde",
        "//tf_quant_finance/math/random_ops",
    ],
)

py_library(
    name = "root_search",
    srcs = ["root_search.py"],
    srcs_version = "PY3",
    deps = [
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "root_search_test",
    size = "small",
    timeout = "moderate",
    srcs = ["root_search_test.py"],
    python_version = "PY3",
    deps = [
        ":root_search",
        # test util,
        # tensorflow dep,
    ],
)

py_library(
    name = "diff_ops",
    srcs = ["diff_ops.py"],
    srcs_version = "PY3",
    deps = [
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "diff_ops_test",
    size = "small",
    srcs = ["diff_ops_test.py"],
    python_version = "PY3",
    deps = [
        "//tf_quant_finance",
        # test util,
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "gradient",
    srcs = ["gradient.py"],
    srcs_version = "PY3",
    deps = [
        # tensorflow_probability dep,
    ],
)

py_test(
    name = "gradient_test",
    size = "small",
    srcs = ["gradient_test.py"],
    python_version = "PY3",
    shard_count = 4,
    deps = [
        ":math",
        # test util,
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "segment_ops",
    srcs = ["segment_ops.py"],
    srcs_version = "PY3",
    deps = [
        ":diff_ops",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "segment_ops_test",
    size = "small",
    srcs = ["segment_ops_test.py"],
    python_version = "PY3",
    deps = [
        ":segment_ops",
        # test util,
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "piecewise",
    srcs = ["piecewise.py"],
    srcs_version = "PY3",
    deps = [
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "piecewise_test",
    size = "medium",
    srcs = ["piecewise_test.py"],
    python_version = "PY3",
    shard_count = 5,
    deps = [
        ":piecewise",
        # test util,
        # numpy dep,
        # tensorflow dep,
    ],
)

filegroup(
    name = "docs",
    srcs = [
        "README.md",
    ],
    data = [
        "//tf_quant_finance/math/interpolation:docs",
        "//tf_quant_finance/math/optimizer:docs",
        "//tf_quant_finance/math/pde:docs",
        "//tf_quant_finance/math/random_ops:docs",
    ],
)
