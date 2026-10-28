# Сторонние компоненты

Установщик Sligate содержит следующие компоненты без изменений. Тексты лицензий лежат рядом с ними
в папке установки (`bin\LICENSE-xray.txt`, `bin\LICENSE-wintun.txt`).

## Xray-core

- Что: сетевое ядро (`bin\xray.exe`, `bin\geoip.dat`, `bin\geosite.dat`) — официальная сборка `Xray-windows-64.zip`, проверяется по SHA-256 из релиза.
- Лицензия: Mozilla Public License 2.0.
- Исходный код: https://github.com/XTLS/Xray-core

## Wintun

- Что: драйвер виртуального сетевого адаптера для режима «Весь трафик» (`bin\wintun.dll`, версия 0.14.1), подписан WireGuard LLC.
- Лицензия: Prebuilt Binaries License, WireGuard LLC — распространяется без изменений вместе с программой, которая использует его через API.
- Сайт: https://www.wintun.net/

## Прочее

- Шрифт Montserrat — SIL Open Font License 1.1.
- Флаги стран — [flag-icons](https://github.com/lipis/flag-icons), MIT.
- Оболочка приложения — [Tauri](https://tauri.app/), MIT / Apache-2.0.
