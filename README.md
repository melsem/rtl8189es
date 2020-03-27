# Пакет rtl8189es для OpenWrt-19.07 и 18.06 kernel-4.17:
* Дрaйвер wifi радиомодуля: rtl8189es
* Как AP работает нормально,
* но при сканировании iw вызывает панику ядра.
* А попытки вручную создать sta ни к чему не привели.
* Не коннектится.

* Поместить add-wifi-rtl8189es.patch в $(BUILD_DIR)
* и дать команду:
```
patch -p1 < add-wifi-rtl8189es.patch
```

* Compile
```
./scripts/feeds update -a
./scripts/feeds install -a
make menuconfig
make V=s
```

