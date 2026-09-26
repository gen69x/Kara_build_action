# Project-KARA Kernel Build Action + KernelSU

## Fitur

- Source: `gen69x/Project-KARA` (branch `EOL`)
- Defconfig: `onclite-perf_defconfig`
- Toolchain: **Proton Clang** (`kdrag0n/proton-clang`)
- KernelSU terintegrasi
- AnyKernel3: `https://github.com/gen69x/AnyKernel3`
- Auto Release ke GitHub Releases

## Konfigurasi Saat Ini

| Item                  | Nilai                                      |
|-----------------------|--------------------------------------------|
| Kernel Source         | https://github.com/gen69x/Project-KARA     |
| Branch                | EOL                                        |
| Defconfig             | onclite-perf_defconfig                     |
| Arch                  | arm64                                      |
| Toolchain             | **Proton Clang** (kdrag0n/proton-clang)    |
| KernelSU              | **Enabled**                                |
| AnyKernel3            | https://github.com/gen69x/AnyKernel3       |
| Auto Release          | Ya                                         |

## Tips Troubleshooting (Kernel 4.9)

Kernel Onclite berbasis **Linux 4.9** (sangat lama). Jika build gagal:

1. **LTO error**  
   Uncomment baris `# disable-lto: true`

2. **KernelSU gagal**  
   Coba set `ksu-lkm: true` (build sebagai module) atau ganti versi KernelSU yang lebih lama.

3. **Proton Clang terlalu baru**  
   Bisa ganti `other-clang-branch` ke commit/tag lama jika perlu.

## Credits
- Kernel: [gen69x/Project-KARA](https://github.com/gen69x/Project-KARA)
- AnyKernel3: [gen69x/AnyKernel3](https://github.com/gen69x/AnyKernel3)
- Toolchain: [kdrag0n/proton-clang](https://github.com/kdrag0n/proton-clang)
- Build Action: [dabao1955/kernel_build_action](https://github.com/dabao1955/kernel_build_action)
- KernelSU: [tiann/KernelSU](https://github.com/tiann/KernelSU)
