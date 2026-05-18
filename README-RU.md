<h1 align="center">⏱️ chronos.yazi</h1>
<p align="center">
  <b>Измеряет время загрузки всех установленных внешних плагинов при запуске <a href="https://github.com/sxyazi/yazi">yazi</a></b><br>
</p>

<p align="center">
  <img src="assets/preview.png" width="850" alt="превью chronos" />
</p>

---

> [!TIP]
> **Английская версия:** [README.md](README.md)

## Установка

> [!IMPORTANT]
> Требуется Yazi v26.5.6+

```sh
ya pkg add WhoSowSee/chronos
```

```sh
# Ручная установка

# Linux/macOS
git clone https://github.com/WhoSowSee/chronos.yazi.git ~/.config/yazi/plugins/chronos.yazi

# Windows
git clone https://github.com/WhoSowSee/chronos.yazi.git $env:APPDATA\yazi\config\plugins\chronos.yazi
```

## Настройка

```lua
require("chronos"):setup({
	enable = true,
	notify_mode = "summary", -- "summary" | "detailed"
	detail_chunk_size = 12,
})
```

> [!IMPORTANT]
> Разместите этот вызов **в самом начале `init.lua`**, до любых других `require(...)`. Lua кэширует модули после первого `require`, поэтому любой плагин, загруженный раньше в `init.lua`, иначе был бы измерен как почти нулевой кэш-хит. Chronos очищает запись кэша каждого плагина перед его измерением.

## Опции

- `enable` (по умолчанию: `false`): включает/выключает бенчмарк запуска
- `notify_mode` (по умолчанию: `"summary"`):
  - `summary`: одно уведомление с общим временем
  - `detailed`: общее время + тайминги плагинов, разбитые на несколько уведомлений
- `detail_chunk_size` (по умолчанию: `12`): количество строк плагинов на подробную страницу. Должно быть положительным целым числом. Если страница выше вашего терминала, рендерер уведомлений Yazi обрежет её — в этом случае выберите меньшее значение

## История звёзд

<p align="center">
  <a href="https://starchart.cc/WhoSowSee/chronos.yazi">
    <picture>
      <source
        media="(prefers-color-scheme: dark)"
        srcset="https://starchart.cc/WhoSowSee/chronos.yazi.svg?variant=custom&background=%230d1117&axis=%238b949e&line=%232f81f7"
      />
      <source
        media="(prefers-color-scheme: light)"
        srcset="https://starchart.cc/WhoSowSee/chronos.yazi.svg?variant=custom&background=%23ffffff&axis=%2357606a&line=%230969da"
      />
      <img
        alt="Stargazers over time"
        src="https://starchart.cc/WhoSowSee/chronos.yazi.svg?variant=custom&background=%23ffffff&axis=%2357606a&line=%230969da"
      />
    </picture>
  </a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/footers/gray0_ctp_on_line.svg?sanitize=true" alt="catppuccin" />
</p>

<p align="center">
  <i><code>&copy 2026-present <a href="https://github.com/WhoSowSee">WhoSowSee</a></code></i>
</p>

<p align="center">
  <a href="https://github.com/WhoSowSee/chronos.yazi/blob/main/LICENSE"><img src="https://img.shields.io/github/license/WhoSowSee/chronos.yazi.svg?style=for-the-badge&color=CBA6F7&logoColor=cdd6f4&labelColor=302D41" alt="LICENSE"></a>
</p>
