# Получение сведений о системе
Сафрыгина Анастасия

## План

1.  Ввод команд в эмулятор терминала

2.  Анализ данных

## Ход работы

1.  Сначала выполним команду uname -r для вывода информации о системе

``` bash
uname -r
```

    5.15.90.1-microsoft-standard-WSL2

1.  Получение сведений о версии ядра:

``` bash
uname -a
```

    Linux LAPTOP-O1FJLJ41 5.15.90.1-microsoft-standard-WSL2 #1 SMP Fri Jan 27 02:56:13 UTC 2023 x86_64 x86_64 x86_64 GNU/Linux

1.  Получение сведений о процессоре:

``` bash
cat /proc/cpuinfo | grep "model name"
```

    model name  : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
    model name  : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
    model name  : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
    model name  : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
    model name  : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
    model name  : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
    model name  : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
    model name  : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx

Было определено, что используемый процессор - AMD Ryzen 5 3500U

1.  Получение последних 30 строк логов системы:

``` bash
dmesg | tail -n 30
```

    [    4.698899] hv_pci 65e3ffe4-eb3a-4e86-9d26-47ba67208c7e: PCI VMBus probing: Using version 0x10004
    [    4.708945] hv_pci 65e3ffe4-eb3a-4e86-9d26-47ba67208c7e: PCI host bridge to bus eb3a:00
    [    4.711934] pci_bus eb3a:00: root bus resource [mem 0x9ffe08000-0x9ffe0afff window]
    [    4.715585] pci_bus eb3a:00: No busn resource found for root bus, will use [bus 00-ff]
    [    4.725382] pci eb3a:00:00.0: [1af4:1049] type 00 class 0x010000
    [    4.734946] pci eb3a:00:00.0: reg 0x10: [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    4.742206] pci eb3a:00:00.0: reg 0x18: [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    4.749319] pci eb3a:00:00.0: reg 0x20: [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    4.778228] pci_bus eb3a:00: busn_res: [bus 00-ff] end is updated to 00
    [    4.781415] pci eb3a:00:00.0: BAR 0: assigned [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    4.789823] pci eb3a:00:00.0: BAR 2: assigned [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    4.796789] pci eb3a:00:00.0: BAR 4: assigned [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    5.130310] hv_pci dc9a302e-bfbb-4139-adb0-5f9a0ae81cba: PCI VMBus probing: Using version 0x10004
    [    5.142099] hv_pci dc9a302e-bfbb-4139-adb0-5f9a0ae81cba: PCI host bridge to bus bfbb:00
    [    5.145313] pci_bus bfbb:00: root bus resource [mem 0x9ffe0c000-0x9ffe0efff window]
    [    5.149184] pci_bus bfbb:00: No busn resource found for root bus, will use [bus 00-ff]
    [    5.161859] pci bfbb:00:00.0: [1af4:1049] type 00 class 0x010000
    [    5.171083] pci bfbb:00:00.0: reg 0x10: [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    5.177733] pci bfbb:00:00.0: reg 0x18: [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    5.186757] pci bfbb:00:00.0: reg 0x20: [mem 0x9ffe0e000-0x9ffe0efff 64bit]
    [    5.214534] pci_bus bfbb:00: busn_res: [bus 00-ff] end is updated to 00
    [    5.217386] pci bfbb:00:00.0: BAR 0: assigned [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    5.223493] pci bfbb:00:00.0: BAR 2: assigned [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    5.229658] pci bfbb:00:00.0: BAR 4: assigned [mem 0x9ffe0e000-0x9ffe0efff 64bit]
    [    6.006522] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    6.009643] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    6.013245] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    6.017953] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    6.021659] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2
    [   50.630909] hv_balloon: Max. dynamic memory size: 3550 MB

## Оценка результата

По итогам всех выполненных операций в лабораторной работе №1 была
получена базовая информация об используемой системе.

## Вывод

Таким образом, мы научились работать с базовыми командами Linux и
получать информацию об операционной системе.
