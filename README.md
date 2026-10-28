# ⛏ KinBeaver Launcher

Современный лаунчер Minecraft для Windows с каталогом Modrinth/FTB,
умной оптимизацией, автоподбором Java, изоляцией профилей по версиям
и продвинутой системой анимаций.

![Version](https://img.shields.io/badge/version-3.1.0-blue)
![Python](https://img.shields.io/badge/python-3.10+-green)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)
![License](https://img.shields.io/badge/license-MIT-yellow)

---

## ✨ Возможности

### 🎮 Игровой опыт
- **Каталог модов/модпаков/ресурспаков/шейдеров** — прямая интеграция с Modrinth API и FTB
- **Установка в один клик** — авто-резолв зависимостей, параллельные загрузки
- **Импорт `.mrpack`** — полноценная поддержка модпаков Modrinth
- **Изоляция по версиям** — каждый профиль со своими модами и конфигами, миры и скриншоты общие (через junction)
- **Microsoft Auth** — вход через device-code flow
- **CustomSkinLoader** — автосинхронизация скинов и плащей с игрой

### ⚡ Оптимизация
- **Smart Boost 3.0** — анализ железа, прогноз FPS, 4 профиля (производительность/стриминг/баланс/качество)
- **Автоподбор RAM** — по количеству модов, шейдеров, свободной памяти
- **Aikar's Flags** — автоматические JVM-флаги под вашу Java и RAM
- **Буст при запуске** — Java HIGH priority, trim RAM лаунчера, убийство зомби-java, Windows Game Mode
- **Тонкая настройка графики** — `options.txt`, Sodium, Iris под пресеты
- **Продвинутый Boost** — очистка логов, удаление устаревших версий, анализ крашей

### 🛡 Надёжность
- **Автопоиск Java** — JDK из PATH, JAVA_HOME, Program Files, Adoptium, Corretto, Zulu, GraalVM…
- **Каскадная установка лоадеров** — MCL → официальный installer.jar → зеркала
- **Проверка целостности** — SHA1 для модов, SHA256 для Java
- **Pre-flight check** — проверка classpath, main class, ассетов, нативов перед запуском
- **Парсер крашей** — `crash-reports/*.txt`, `hs_err_pid*.log`, exit-code → человекочитаемая подсказка
- **Безопасный режим** — отключение всех модов при краше в один клик
- **Авто-починка** — битые версии переустанавливаются автоматически
- **Fast-launch** — 2-й+ запуск версии мгновенный (все проверки пропущены)

### 🌐 Сеть
- **Зеркала Mojang** — bmclapi2, hkmc, bsmirror, ghproxy с автопереключением при ошибке
- **DNS-over-HTTPS** — обход DNS-блокировок провайдера
- **Прокси** — socks5/http
- **Range-загрузка** — параллельная для больших файлов

### 🎨 UI
- **8 тем** — тёмная, светлая, розовая, красная, оранжевая, фиолетовая, синяя, «бобровая»
- **Анимации** — stagger-появление карточек, shimmer-skeleton, hover-scale, pulse
- **Command palette** — Ctrl+K с поиском по действиям
- **Горячие клавиши** — Ctrl+R (запуск), Ctrl+L (консоль), Ctrl+1..7 (вкладки), F5
- **Toast-уведомления** — slide-in с overshoot
- **2D/3D viewer скинов** — псевдо-3D с тенями и вторым слоем

### 🔌 Расширяемость
- **Python-плагины** — `.py` из `userdata/extensions/`
- **Хуки** — `on_launcher_ready`, `on_game_start`, `on_game_exit`, `on_mod_installed`, `on_tab_open`
- **Свои вкладки** — `kb_api.add_tab()`
- **Кнопки на дашборде** — `kb_api.add_dashboard_button()`

---

## 📦 Установка

### Готовый `.exe`

1. Скачайте `KinBeaver_Setup.exe` из [Releases](../../releases)
2. Запустите установщик
3. Готово

### Из исходников

```bash
git clone https://github.com/arsashelov-star/KinBeaver-Launcher.git
cd KinBeaver-Launcher
pip install -r requirements.txt
python main.py
