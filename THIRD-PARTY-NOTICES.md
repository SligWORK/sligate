# Сторонние компоненты

Sligate содержит следующие компоненты без изменений. Тексты лицензий лежат рядом с ними:
Windows — в папке установки (`bin\LICENSE-xray.txt`, `bin\LICENSE-wintun.txt`), Linux — в пакете
(`/usr/lib/Sligate/bin/LICENSE-xray.txt`), Android — внутри приложения (`assets/licenses/`).

## Xray-core

- Что: сетевое ядро и базы маршрутизации (`xray`, `geoip.dat`, `geosite.dat`) — официальные сборки из релизов XTLS (`Xray-windows-64.zip`, `Xray-linux-64.zip`, `Xray-android-arm64-v8a.zip`), проверяются по SHA-256 из релиза.
- Лицензия: Mozilla Public License 2.0.
- Исходный код: https://github.com/XTLS/Xray-core

## libXray (Android)

- Что: Xray-core в виде библиотеки для Android (`libxray-android.zip` из релизов XTLS), проверяется по SHA-256.
- Лицензия: MIT, Copyright (c) 2023-2025 XTLS.
- Исходный код: https://github.com/XTLS/libXray

## Wintun (Windows)

- Что: драйвер виртуального сетевого адаптера для режима «Весь трафик» (`bin\wintun.dll`, версия 0.14.1), подписан WireGuard LLC.
- Лицензия: Prebuilt Binaries License, WireGuard LLC — распространяется без изменений вместе с программой, которая использует его через API.
- Сайт: https://www.wintun.net/

## Прочее

- Шрифт Montserrat — SIL Open Font License 1.1.
- Флаги стран — [flag-icons](https://github.com/lipis/flag-icons), MIT.
- Оболочка приложения — [Tauri](https://tauri.app/), MIT / Apache-2.0.
- QR-коды на Android TV — [qrcode](https://github.com/kennytm/qrcode-rust), MIT / Apache-2.0.
