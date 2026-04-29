cmake_minimum_required(VERSION 3.13)

project(pico_w_keypad_leds C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# This source uses Arduino APIs (setup/loop, Keypad library).
# Build this project with an Arduino-compatible RP2040 core (e.g. Earle Philhower core)
# or adapt to raw Pico SDK if desired.
add_custom_target(info ALL
  COMMAND ${CMAKE_COMMAND} -E echo "Use Arduino RP2040 toolchain/core to compile src/main.cpp"
)
