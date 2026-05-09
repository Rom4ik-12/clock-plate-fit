# clock-plate-fit

[Русский](README.ru.md)

A user module for the [illogical-impulse-plugins](https://github.com/Rom4ik-12/illogical-impulse-plugins) loader.
Shrinks the bar's clock plate to hug the actual clock width instead of using
the fixed wider `centerSideModuleWidth` slot.

## What it does

Toggles a single line in `modules/ii/bar/BarContent.qml`:

```qml
// off (system default — wider, fixed)
implicitWidth: root.centerSideModuleWidth

// on  (this module — auto-fit)
implicitWidth: clockWidget.implicitWidth + 20
```

When the module is enabled, the plate shrinks down with the clock
(narrower in non-verbose mode, narrower again on small screens). Disable
to fall back to the roomy fixed plate.

## Install

Easiest way — paste the URL into Settings → Modules → install field:

```
https://github.com/Rom4ik-12/clock-plate-fit/releases/latest/download/clock-plate-fit.qsmod
```

Or grab the `.qsmod` from the [releases page](https://github.com/Rom4ik-12/clock-plate-fit/releases)
and drop it on the picker.

## Requirements

- illogical-impulse-plugins loader **v1.4** or newer (declared via
  `requiresLoader: "1.4"` so the system warns you on a mismatch).
