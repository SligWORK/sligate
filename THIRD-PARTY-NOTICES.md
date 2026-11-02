# Сторонние компоненты

Sligate содержит следующие компоненты. Все они без изменений, кроме прокси Telegram и способов режима «Без сервера» (см. ниже). Тексты лицензий лежат рядом с ними:
Windows — в папке установки (`bin\LICENSE-xray.txt`, `bin\LICENSE-wintun.txt`, `bin\LICENSE-tg-ws-proxy.txt`), Linux — в пакете
(`/usr/lib/Sligate/bin/LICENSE-xray.txt`), Android — внутри приложения (`assets/licenses/`).

Файлы режима «Без сервера» в установщик не входят: они скачиваются при первом включении режима, и лицензии лежат в них же. На компьютере это `C:\ProgramData\Sligate\bypass\module\<хеш>\licenses\` и `C:\ProgramData\Sligate\bypass\pack\<версия>\licenses\`, в релизах — папка `licenses/` внутри архивов `module-*.zip` и `pack-*.zip`.

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

## Режим «Без сервера» (Windows)

### zapret2

- Что: основной движок режима (`winws2.exe`, файлы Lua), официальная сборка zapret2 1.0.6, проверяется по SHA-256.
- Лицензия: MIT, Copyright (c) 2016-2026 bol-van.
- Исходный код: https://github.com/bol-van/zapret2/tree/v1.0.6

### zapret

- Что: запасной движок режима (`winws.exe`), официальная сборка zapret 72.13, проверяется по SHA-256.
- Лицензия: MIT, Copyright (c) 2016-2024 bol-van.
- Исходный код: https://github.com/bol-van/zapret/tree/v72.13

### LuaJIT

- Что: вкомпилирован в `winws2.exe`, версия 2.1-20250826.
- Лицензия: MIT, Copyright (C) 2005-2025 Mike Pall.
- Исходный код: https://github.com/openresty/luajit2/tree/v2.1-20250826

### zlib

- Что: вкомпилирован в `winws2.exe` и `winws.exe`.
- Лицензия: zlib license.
- Сайт: https://zlib.net

### WinDivert

- Что: драйвер и библиотека для работы с сетевыми пакетами (`WinDivert.dll`, `WinDivert64.sys`), версия 2.2.2, из выпусков zapret2 и zapret. `WinDivert.dll` из выпуска zapret2 отличается только флагом DYNAMICBASE и контрольной суммой файла, код тот же. Библиотеку можно заменить своей сборкой с тем же интерфейсом.
- Лицензия: на выбор LGPLv3 или GPLv2.
- Исходный код: https://github.com/basil00/WinDivert/tree/v2.2.2

### Cygwin

- Что: библиотека `cygwin1.dll`, версия 3.4.10, из выпусков zapret2 и zapret. Её можно заменить своей сборкой с тем же интерфейсом.
- Лицензия: LGPLv3 или новее.
- Исходный код: https://github.com/cygwin/cygwin/tree/cygwin-3.4.10, сайт https://cygwin.com

### Способы и списки сайтов

Из них собран пакет `pack-*.zip`: списки сайтов и заготовки пакетов без изменений, способы переведены в формат пакета Sligate.

- [zapret-discord-youtube](https://github.com/Flowseal/zapret-discord-youtube/tree/1.10.4) 1.10.4: списки сайтов, заготовки пакетов и способы для zapret.
- [PR #18202](https://github.com/Flowseal/zapret-discord-youtube/pull/18202) этого проекта: способы для zapret2 и файл `lua/blobs.lua`, коммит [`84ca2eeb`](https://github.com/SnAnVl/zapret-discord-youtube/tree/84ca2eeb471982d9cc43e440c74301bf746c46e0) из SnAnVl/zapret-discord-youtube.
- Лицензия обоих: MIT, Copyright (c) 2016-2026 bol-van, Copyright (c) 2024-2026 Flowseal.

## Прокси Telegram (Windows)

### tg-ws-proxy-rs

- Что: локальный прокси Telegram, вкомпилирован в программу. Это урезанная и изменённая копия версии 2.5.10, коммит `14828a5`.
- Лицензия: MIT, Copyright (c) 2026 valnesfjord, текст в `bin\LICENSE-tg-ws-proxy.txt`.
- Исходный код: https://github.com/valnesfjord/tg-ws-proxy-rs/tree/14828a5dad73ca6a60d3bde1929af315f5626b9e

### tg-ws-proxy

- Что: исходный проект на Python, который tg-ws-proxy-rs переносит на Rust. С ним мы сверяли поведение (коммит `2085861`).
- Лицензия: MIT, Copyright (c) 2026 Flowseal.
- Исходный код: https://github.com/Flowseal/tg-ws-proxy

## Прочее

- Шрифт Montserrat — SIL Open Font License 1.1.
- Флаги стран — [flag-icons](https://github.com/lipis/flag-icons), MIT.
- Оболочка приложения — [Tauri](https://tauri.app/), MIT / Apache-2.0.
- QR-коды на Android TV — [qrcode](https://github.com/kennytm/qrcode-rust), MIT / Apache-2.0.
- Шифрование в сетевых соединениях — [ring](https://github.com/briansmith/ring), Apache-2.0 и ISC.
- Обмен ключами при проверке сайтов в режиме «Без сервера» — [ml-kem](https://github.com/RustCrypto/KEMs), Apache-2.0 / MIT.
