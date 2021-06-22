cmake_minimum_required(VERSION 3.19)
project(node_rpi_ws281x_native)

set(CMAKE_CXX_STANDARD 14)

include_directories(node_modules)
include_directories(node_modules/nan)
include_directories(~/.nvm/versions/node/v14.17.1/include/node)
include_directories(src/rpi_ws281x)
include_directories(src/rpi_ws281x/golang)
include_directories(src/rpi_ws281x/golang/ws2811)
include_directories(src/rpi_ws281x/golang/ws2811)

add_executable(node_rpi_ws281x_native
        node_modules/nan/nan.h
        node_modules/nan/nan_callbacks.h
        node_modules/nan/nan_callbacks_12_inl.h
        node_modules/nan/nan_callbacks_pre_12_inl.h
        node_modules/nan/nan_converters.h
        node_modules/nan/nan_converters_43_inl.h
        node_modules/nan/nan_converters_pre_43_inl.h
        node_modules/nan/nan_define_own_property_helper.h
        node_modules/nan/nan_implementation_12_inl.h
        node_modules/nan/nan_implementation_pre_12_inl.h
        node_modules/nan/nan_json.h
        node_modules/nan/nan_maybe_43_inl.h
        node_modules/nan/nan_maybe_pre_43_inl.h
        node_modules/nan/nan_new.h
        node_modules/nan/nan_object_wrap.h
        node_modules/nan/nan_persistent_12_inl.h
        node_modules/nan/nan_persistent_pre_12_inl.h
        node_modules/nan/nan_private.h
        node_modules/nan/nan_string_bytes.h
        node_modules/nan/nan_typedarray_contents.h
        node_modules/nan/nan_weak.h
        src/rpi_ws281x/golang/ws2811/ws2811.go.h
        src/rpi_ws281x/python/rpi_ws281x.i
        src/rpi_ws281x/clk.h
        src/rpi_ws281x/dma.c
        src/rpi_ws281x/dma.h
        src/rpi_ws281x/gpio.h
        src/rpi_ws281x/mailbox.c
        src/rpi_ws281x/mailbox.h
        src/rpi_ws281x/main.c
        src/rpi_ws281x/pcm.c
        src/rpi_ws281x/pcm.h
        src/rpi_ws281x/pwm.c
        src/rpi_ws281x/pwm.h
        src/rpi_ws281x/rpihw.c
        src/rpi_ws281x/rpihw.h
        src/rpi_ws281x/version.h
        src/rpi_ws281x/ws2811.c
        src/rpi_ws281x/ws2811.h
        src/rpi-ws281x.cc)
