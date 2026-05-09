# clock-plate-fit

[English](README.md)

Пользовательский модуль для загрузчика
[illogical-impulse-plugins](https://github.com/Rom4ik-12/illogical-impulse-plugins).
Сужает плашку часов в баре под фактическую ширину часов вместо
фиксированной широкой `centerSideModuleWidth`.

## Что делает

Переключает одну строку в `modules/ii/bar/BarContent.qml`:

```qml
// выкл (дефолт системы — широкая, фиксированная)
implicitWidth: root.centerSideModuleWidth

// вкл (этот модуль — подстраивается)
implicitWidth: clockWidget.implicitWidth + 20
```

Когда модуль включён, плашка сужается вместе с часами (уже без даты,
ещё уже на маленьких экранах). Выключи — вернётся широкая.

## Установка

Самый простой способ — вставить ссылку в Settings → Modules → поле
установки:

```
https://github.com/Rom4ik-12/clock-plate-fit/releases/latest/download/clock-plate-fit.qsmod
```

Или скачай `.qsmod` со
[страницы релизов](https://github.com/Rom4ik-12/clock-plate-fit/releases) и
кинь его в "Выбрать файл…".

## Требования

- Загрузчик illogical-impulse-plugins **v1.4** и новее (указан
  `requiresLoader: "1.4"`, система предупредит при несовпадении).
