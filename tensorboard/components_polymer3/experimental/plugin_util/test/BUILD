load("//tensorboard/defs:web.bzl", "tf_web_library", "tf_web_test")

package(
    default_testonly = True,
    default_visibility = ["//tensorboard:internal"],
)

licenses(["notice"])  # Apache 2.0

tf_web_test(
    name = "test",
    src = "/tf-plugin-util/test/tests.html",
    tags = ["manual"],
    web_library = ":test_web_library",
)

# This test is disabled now that plugin_util has migrated to Polymer 3.
tf_web_library(
    name = "test_web_library",
    srcs = [
        # "plugin-test.ts",
        # "testable-iframe.html",
        # "tests.html",
        "//tensorboard/components_polymer3/experimental/plugin_lib/test:testable_plugin_bundle.js",
    ],
    path = "/tf-plugin-util/test",
    deps = [
        "//tensorboard/components/tf_imports:web_component_tester",
        "//tensorboard/components_polymer3/experimental/plugin_util:plugin_host",
    ],
)
