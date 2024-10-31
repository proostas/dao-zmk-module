# Dao (Unofficial) ZMK Module

This repository contains the board files for the [Dao](https://github.com/yumagulovrn/dao-choc-ble) to allow users to build firmware. 
This can be done by adding the module to the west.yml found in your zmk-config's config directory. 
There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the Dao module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: proostas
      url-base: https://github.com/proostas
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: dao-zmk-module
      remote: proostas
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.
