# android_device_xiaomi_popsicle-kernel (SoftOS)

**Türkçe** · [English](#english)

Xiaomi 17 Pro Max (`popsicle`, SM8850) için ön-derlenmiş **stok** çekirdek dizini. LineageOS 24 ağacında
`device/xiaomi/popsicle-kernel` yoluna bağlanır ([local manifest](https://github.com/softos-rom/local_manifests)).
Çekirdek derlenmez ve değiştirilmez.

| Yol | Kaynak | Depoda mı |
|---|---|---|
| `kernel`, `dtb/`, `dtbo.img`, `vendor_ramdisk/`, `vendor_dlkm/`, `system_dlkm/` | Stok HyperOS **OS4.0.5.0.XPBCNXM** fastboot paketi, `./extract-files.sh <dump>` ile | Hayır (üretilir) |
| `kernel-headers/` | [xiaomi17-pudding-dev/device_xiaomi_pudding-kernel](https://github.com/xiaomi17-pudding-dev/device_xiaomi_pudding-kernel) `90cc7f13d49e151ddbd74ef9ce638b80f78e7435` (GPL-2.0 UAPI) | Evet |
| `extract-files.sh` | aynı depo (Apache-2.0, The LineageOS Project) | Evet |

Stok çekirdek: `6.12.69-android16-6-g43b5ab7e247d-abogki558343811-4k`. Başlıklar aynı ACK hattından
(6.12.69 android16-6), Qualcomm HAL'larının kaynaktan derlenmesi için kullanılır.
Firmware bu depoda yoktur ve telefona yazılmaz.

**Çekirdek kaynağı (GPL-2.0):** Xiaomi'nin yayımladığı kaynak
[MiCode/Xiaomi_Kernel_OpenSource `popsicle-w-oss`](https://github.com/MiCode/Xiaomi_Kernel_OpenSource/tree/popsicle-w-oss)
(Xiaomi 17 / 17 Pro / 17 Pro Max, Android 16); GKI ortak çekirdek
[android16-6.12](https://android.googlesource.com/kernel/common/+/refs/heads/android16-6.12).
SoftOS çekirdekte değişiklik yapmaz.

---

## English

Prebuilt **stock** kernel directory for the Xiaomi 17 Pro Max (`popsicle`, SM8850), used at
`device/xiaomi/popsicle-kernel` in a LineageOS 24 tree. The kernel is neither built nor modified.

- `kernel`, `dtb/`, `dtbo.img`, `vendor_ramdisk/`, `vendor_dlkm/`, `system_dlkm/`: extracted from the stock
  HyperOS OS4.0.5.0.XPBCNXM fastboot package with `./extract-files.sh <dump>` (not in git).
- `kernel-headers/`: from xiaomi17-pudding-dev/device_xiaomi_pudding-kernel `90cc7f1` (GPL-2.0 UAPI).
- `extract-files.sh`: same origin (Apache-2.0, The LineageOS Project).

**Kernel source (GPL-2.0):** Xiaomi's published source
[MiCode/Xiaomi_Kernel_OpenSource `popsicle-w-oss`](https://github.com/MiCode/Xiaomi_Kernel_OpenSource/tree/popsicle-w-oss);
GKI common kernel [android16-6.12](https://android.googlesource.com/kernel/common/+/refs/heads/android16-6.12).
SoftOS does not change the kernel. No firmware is included in this repository.
