# ZMK Module Template

This repository contains a template for a ZMK module, as it would most frequently be used.

## Usage

### using [ZMK CLI](https://zmk.dev/docs/user-setup)

1. add this module: `zmk module add https://github.com/AkytharPandaaa/zmk-keyboard-module-pandawings-i`
2. add the keyboard to your config: `zmk keyboard add`
   1. the keyboard name is "pandawings-i"
   2. please choose the controller "xiao_ble"

## Keymap

There is a sample qwerty keymap added that can be further customized. I'm using a german layout so [mine](https://github.com/AkytharPandaaa/zmk-config/blob/main/config/pandawings-i.keymap) is different.

## More Info

For more info on modules, you can read through through the [Zephyr modules page](https://docs.zephyrproject.org/3.5.0/develop/modules.html) and [ZMK's page on using modules](https://zmk.dev/docs/features/modules). [Zephyr's west manifest page](https://docs.zephyrproject.org/3.5.0/develop/west/manifest.html#west-manifests) may also be of use.

## Troubleshooting

### Build Failed: Rename artifacts

Try using the `artifacts-name` option over at your `build.yaml`.

> The forward-slashes used within the controller's names (`//zmk`) are causing trouble due to them being used within the path for the rename process.

Recommended names:

- left-side: `artifact-name: pandawings-i_left_with_studio`
- right-side: `artifact-name: pandawings-i_right`
