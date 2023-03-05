# Системы аутентификации и защиты от несанкционированного доступа

Лабораторная работа №1

## Цель

Вывести информацию о системе

## Исходные данные

1.  ОС Windows 11
2.  RStudio Desktop
3.  WSL2
4.  Интерпретатор языка R 4.2.2

## План

1.  Выполнить команду uname -r
2.  Выполнить команду cat /proc/cpuinfo \| grep "model name"
3.  Выполнить команду journalctl -q -b \| tail -n 30

## Шаги

1\.  Сначала выполним команду uname -r для вывода информации о системе

```{bash}
uname -r
```

	5.15.90.1-microsoft-standard-WSL2


2\. Далее команда cat /proc/cpuinfo \| grep "model name" для вывода информации о процессоре, строки которой содержат "model name"

```{bash}
cat /proc/cpuinfo | grep "model name"
```
	
	model name      : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
	model name      : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
	model name      : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
	model name      : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
	model name      : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
	model name      : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
	model name      : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx
	model name      : AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx

3\. Также выполним команду journalctl -q -b \| tail -n 30 для вывода последних 30 строк логов

```{bash}
dmesg | tail -n 30
```

	[    5.385472] pci_bus f436:00: root bus resource [mem 0xbffe10000-0xbffe12fff window]
	[    5.388930] pci_bus f436:00: No busn resource found for root bus, will use [bus 00-ff]
	[    5.401462] pci f436:00:00.0: [1af4:1049] type 00 class 0x010000
	[    5.413693] pci f436:00:00.0: reg 0x10: [mem 0xbffe10000-0xbffe10fff 64bit]
	[    5.418701] 9pnet_virtio: no channels available for device drvfs
	[    5.420995] pci f436:00:00.0: reg 0x18: [mem 0xbffe11000-0xbffe11fff 64bit]
	[    5.429350] pci f436:00:00.0: reg 0x20: [mem 0xbffe12000-0xbffe12fff 64bit]
	[    5.459319] pci_bus f436:00: busn_res: [bus 00-ff] end is updated to 00
	[    5.462337] pci f436:00:00.0: BAR 0: assigned [mem 0xbffe10000-0xbffe10fff 64bit]
	[    5.469344] pci f436:00:00.0: BAR 2: assigned [mem 0xbffe11000-0xbffe11fff 64bit]
	[    5.476534] pci f436:00:00.0: BAR 4: assigned [mem 0xbffe12000-0xbffe12fff 64bit]
	[    5.521811] 9pnet_virtio: no channels available for device drvfs
	[    5.676310] hv_pci 8d3ce33f-8cd8-4d26-83ce-e7d0cd475779: PCI VMBus probing: Using version 0x10004
	[    5.833511] hv_pci 8d3ce33f-8cd8-4d26-83ce-e7d0cd475779: PCI host bridge to bus 8cd8:00
	[    5.837221] pci_bus 8cd8:00: root bus resource [mem 0xbffe14000-0xbffe16fff window]
	[    5.840550] pci_bus 8cd8:00: No busn resource found for root bus, will use [bus 00-ff]
	[    5.851731] pci 8cd8:00:00.0: [1af4:1049] type 00 class 0x010000
	[    5.861938] pci 8cd8:00:00.0: reg 0x10: [mem 0xbffe14000-0xbffe14fff 64bit]
	[    5.869565] pci 8cd8:00:00.0: reg 0x18: [mem 0xbffe15000-0xbffe15fff 64bit]
	[    5.878157] pci 8cd8:00:00.0: reg 0x20: [mem 0xbffe16000-0xbffe16fff 64bit]
	[    5.910302] pci_bus 8cd8:00: busn_res: [bus 00-ff] end is updated to 00
	[    5.913081] pci 8cd8:00:00.0: BAR 0: assigned [mem 0xbffe14000-0xbffe14fff 64bit]
	[    5.919890] pci 8cd8:00:00.0: BAR 2: assigned [mem 0xbffe15000-0xbffe15fff 64bit]
	[    5.926553] pci 8cd8:00:00.0: BAR 4: assigned [mem 0xbffe16000-0xbffe16fff 64bit]
	[    6.111602] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
	[    6.115191] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
	[    6.118611] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
	[    6.121983] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
	[    6.125443] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2
	[   50.675522] hv_balloon: Max. dynamic memory size: 3550 MB

## Оценка результата

В результате лабораторной работы мы получили основную информацию об ОС, процессоре и логи системы.

## Вывод

Таким образом, мы научились работать с базовыми командами Linux и получать информацию об операционной системе.