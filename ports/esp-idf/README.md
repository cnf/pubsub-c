# ESP-IDF component

In your ESP-IDF project, edit your `idf_component.yml`:

```yaml
dependencies:
  pubsub-c:
    git: https://github.com/jaracil/pubsub-c
    version: "*"
    path: ports/esp-idf
```

and add `pubsub-c` to your main `CMakeLists.txt`:

```cmake
idf_component_register(
  SRCS ${SRC} 
  REQUIRES pubsub-c
)
```

The [Component Manager](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/tools/idf-component-manager.html) will automatically download pubsub-c, and make it available to your project.