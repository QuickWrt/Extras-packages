### Extra Packages for OpenWrt 24.10

1. Add new opkg key:

  ```bash
  wget https://raw.githubusercontent.com/QuickWrt/Extras-packages/refs/heads/master/key-build.pub && opkg-key add key-build.pub
  ```

2. Add opkg repository:

  ```bash
  echo "src/gz quickwrt_extras https://raw.githubusercontent.com/QuickWrt/Extras-packages/$(. /etc/openwrt_release ; echo $DISTRIB_ARCH)" >> /etc/opkg/customfeeds.conf
  ```

3. Update opkg sources:

  ```bash
  opkg update
  ```

4. Now you can go to luci and search for packages to install. After the first installed, you need to reboot.
