<p align="center">
  <img src="https://raw.githubusercontent.com/arsashelov-star/KinBeaver-Launcher/main/assets/icon.png" alt="KinBeaver Logo" width="140">
</p>

<h1 align="center">KinBeaver Launcher</h1>

<p align="center">
  <b>Умный Minecraft-лаунчер, который сам подбирает JVM, RAM и Java — играй, а не настраивай!</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-3.1.0-brightgreen?style=for-the-badge&logo=github" alt="Version">
  <img src="https://img.shields.io/badge/platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows" alt="Platform">
  <img src="https://img.shields.io/badge/python-3.10%2B-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/license-MIT-green?style=for-the-badge" alt="License">
</p>

<p align="center">
  <a href="https://github.com/arsashelov-star/KinBeaver-Launcher/releases/latest">
    <img src="https://img.shields.io/badge/Скачать-Latest_Release-3fb950?style=for-the-badge&logo=windows&logoColor=white" alt="Download">
  </a>
</p>

---

## 📸 Скриншоты

<p align="center">
  <img src="https://raw.githubusercontent.com/arsashelov-star/KinBeaver-Launcher/main/assets/dashboard.png" width="800" alt="Главное окно">
</p>

<details>
<summary><b>Посмотреть остальные скриншоты (Smart Boost, Каталог модов)</b></summary>
<br>
<table align="center">
  <tr>
    <td><img src="https://raw.githubusercontent.com/arsashelov-star/KinBeaver-Launcher/main/assets/boost.png" width="400" alt="Smart Boost"></td>
    <td><img src="https://raw.githubusercontent.com/arsashelov-star/KinBeaver-Launcher/main/assets/mods.png" width="400" alt="Каталог модов"></td>
  </tr>
</table>
</details>

---

## 🖥️ Системные требования

KinBeaver — оптимизированный лаунчер, но для стабильной работы Minecraft (особенно с модами) ваше железо должно соответствовать следующим параметрам:

| Компонент | 🟢 Минимальные | 🔥 Рекомендуемые |
| :--- | :--- | :--- |
| **ОС** | Windows 10 (64-bit) | Windows 10 / 11 (64-bit) |
| **Процессор** | Intel Core i3 / AMD Ryzen 3 | Intel Core i5 / AMD Ryzen 5 и выше |
| **Оперативная память** | **4 ГБ** (выделять 2 ГБ для игры) | **8–16 ГБ** (выделять 4–6 ГБ для игры) |
| **Видеокарта** | Встроенная (Intel HD 4000+) | Дискретная (GTX 1050 / RX 560 и выше) |
| **Место на диске** | 1 ГБ (для лаунчера + ядро игры) | 10+ ГБ (для модов, ресурспаков и миров) |
| **Java** | **Java 17** (64-bit) | **Java 21** (64-bit) для MC 1.20.5+<br>**Java 25** для MC 26.x |
| **Интернет** | Требуется для загрузки | Стабильное подключение |

> ⚠️ **Важно про Java:** Лаунчер **не скачивает** Java автоматически. Он умеет её находить в системе и проверять на совместимость. Если у вас не запускается игра — скачайте актуальную версию Java с [Adoptium (Temurin)](https://adoptium.net/).

---

## ✨ Главные фишки

*   ⚡ **Smart Boost 3.0** — встроенный AI-анализ системы. Сам подберет идеальные JVM-флаги, выделит нужное количество RAM и очистит память перед запуском.
*   🧠 **Auto-JVM Optimizer** — забыли про `-Xmx` и `-Xms`? Лаунчер сам подберет G1GC-флаги под вашу версию Java и количество модов.
*   🛡️ **Launch Preflight** — проверка перед запуском. Лаунчер проверит целостность файлов, наличие ассетов и совместимость модов. Вы увидите *вероятность успешного запуска в %*.
*   🔍 **Crash Parser** — если игра вылетела, лаунчер прочитает лог и напишет человеческим языком: *"Не хватает памяти"* или *"Конфликт миксинов в моде X"*.
*   📦 **Каталог модов (Modrinth)** — установка модов, ресурспаков и шейдеров в один клик. Зависимости скачиваются автоматически.
*   🎨 **8 тем оформления** — от классической тёмной до "Бобровой".
*   🔄 **Автообновление** — лаунчер сам проверяет новые версии на GitHub и обновляет себя. Ваши настройки и моды при этом не удаляются!

---

## 🚀 Установка

### Для игроков (Автоматическая сборка)
1. Перейдите в раздел [Releases](https://github.com/arsashelov-star/KinBeaver-Launcher/releases/latest).
2. Скачайте последний `.zip` архив.
3. Распакуйте в любую папку (например, `C:\KinBeaver`).
4. Запустите `KinBeaver.exe`.

> 🛡️ **Антивирусы (Windows Defender, Kaspersky и др.)** могут ругаться на `.exe`, собранный через PyInstaller. Это **ложное срабатывание**. Добавьте папку с лаунчером в исключения антивируса.

### Для разработчиков (Из исходников)
```bash
# 1. Клонируем репозиторий
git clone https://github.com/arsashelov-star/KinBeaver-Launcher.git
cd KinBeaver-Launcher

# 2. Создаем виртуальное окружение и ставим зависимости
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt

# 3. Запускаем
python main.py
