# Fh-loader
源码来自于https://github.com/Rivko/android-firmware-qti-sdm670/tree/main/boot_images/QcomPkg/Tools/storage/fh_loader

添加对Simg的CRC区块支持，添加跳过设备自动配置以规避某些特殊设备。代码根目录为官方编译版本。

Windows使用MSVC编译，仅提供64位版本。

cl fh_cobs.c fh_crc.c fh_hsuart_packet.c fh_loader.c fh_loader_sha.c fh_transfer.c fh_transport.c fh_transport_com.c fh_transport_hsuart.c fh_transport_linux_pipe.c stringl/memscpy.c stringl/memsmove.c stringl/strlcat.c stringl/strlcpy.c -I./ -I./stringl/

macOS使用gcc编译，替换部分头文件为macOS平台实现，可能导致意料外的行为。

Linux为高通官方适配，理论上不应存在问题。

注意：该仓库代码仅供参考学习，与实际release所用代码并不一致。
