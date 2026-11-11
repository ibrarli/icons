# Changelog

All notable changes to apen-icons. This project follows [semantic versioning](https://semver.org).

## 1.3.0

100 new icons, for 391 in total. Nothing is renamed or removed.

### Added

- **Actions:** `CheckCheck`, `MousePointer`, `Move`, `RotateCcw`, `RotateCw`, `ToggleLeft`, `ToggleRight`, `Unlink`
- **Alerts:** `BadgeAlert`, `BellPlus`, `BellRing`, `OctagonAlert`
- **Charts:** `AreaChart`, `BarChartHorizontal`, `Gauge`, `Presentation`
- **Commerce:** `Banknote`, `Calculator`, `Coins`, `QrCode`, `ShoppingBasket`, `Store`, `Ticket`
- **Communication:** `MailOpen`, `MessageSquareText`, `Messages`, `PhoneCall`, `PhoneIncoming`, `PhoneOff`, `PhoneOutgoing`
- **Design:** `Contrast`, `Eraser`, `PenTool`, `Ruler`, `Wand`
- **Development:** `Binary`, `Braces`, `GitCommit`, `GitFork`, `GitMerge`, `GitPullRequest`, `Workflow`
- **Devices:** `BatteryCharging`, `BatteryLow`, `HardDrive`, `Plug`, `Speaker`, `Watch`
- **Files:** `FileCode`, `FileImage`, `FileMinus`, `FileSearch`, `FolderCheck`, `FolderX`
- **Layout:** `AppWindow`, `Kanban`, `LayoutTemplate`, `PanelBottom`, `PanelTop`
- **Maps:** `Bike`, `Car`, `Locate`, `Mountain`, `Plane`, `Route`, `Train`
- **Media:** `Disc`, `FastForward`, `Film`, `ImagePlus`, `ListMusic`, `Radio`, `Rewind`
- **Security:** `KeyRound`, `ScanFace`, `ShieldOff`, `Siren`
- **Shapes:** `Cube`, `Octagon`, `Pentagon`
- **Social:** `Coffee`, `Crown`, `Medal`, `Rocket`
- **Text:** `Heading`, `Pilcrow`, `Quote`, `WrapText`
- **Time:** `AlarmClock`, `CalendarClock`, `CalendarDays`, `CalendarMinus`
- **Users:** `IdCard`, `UserLock`, `UserSearch`
- **Weather:** `CloudLightning`, `CloudSnow`, `CloudSun`, `Sunrise`, `Sunset`

### Changed

- README and banner show the new icon count.

## 1.2.1

### Changed

- README: new banner, plus Styling, Categories and TypeScript sections. No code changes.

## 1.2.0

The whole set is redrawn on one grid, and icons are now generated from SVG files.

### Added

- 160 new icons, for 291 in total: dashboard and layout, files, commerce, media, charts, text editing, devices, weather, time and maps.
- Solid variants `PlayFill`, `PauseFill`, `StarFill` and `BookmarkFill`.
- `absoluteStrokeWidth` and `title` props. Icons are `aria-hidden` unless they have a `title` or `aria-label`.
- Every icon gets the classes `apen-icon` and `apen-icon-<name>`.
- `createIcon`, `IconProps`, `IconNode` and `ApenIcon` are exported.
- Raw SVG files ship in the package: `apen-icons/icons/<name>.svg`, plus `apen-icons/meta.json`.
- Editor hover previews for every icon.

### Changed

- Every icon is redrawn on a 24 × 24 grid with a 2px rounded stroke and rounded corners, so sizes and weights match.
- Icons that were solid (`Search`, `Settings`, `Folder`, `Play`, `Pause`, `Bookmark` and others) are now outlined. Use the `*Fill` icons for solid versions.
- `Bolt` is now a lightning bolt, matching its tags.
- The UMD global is `apenIcons`.

### Deprecated

Duplicates were merged. The old names still work as aliases and will be removed in 2.0:
`Cross` → `X`, `CircleCross` → `CircleX`, `Dash` → `Minus`, `SquareOutline` → `Square`, `Kebab` / `KebabMenu` → `MenuKebab`, `User2` → `User`, `Eye2` → `Eye`, `Moon2` → `Moon`, `VideoCamera` → `Video`, `Joystick2` → `Joystick`, `Home2` → `Home`, and `Home2Plus`, `Home2Minus`, `Home2Check`, `Home2X`, `Home2Pen`, `Home2Alert`, `Home2One`, `Home2Two` → the same names without the `2`.

### Fixed

- `react-router-dom` is no longer installed with the library.
- The CommonJS entry point uses a `.cjs` extension so `require('apen-icons')` loads the icons correctly.

### Internal

- Icons live as SVG files in `icons/` with metadata in `icons/meta.json`. `npm run icons` validates them against the grid rules and generates the components; the hand-written versioned folders are gone.
- The website is rebuilt with the Apen UI design system (Tailwind v4).
