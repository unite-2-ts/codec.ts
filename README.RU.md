# 🏠 IDC-L2 (Canary) 🏠

## 📱 Что это такое? 📱

Это PWA приложение, представляющее из себя подобие мобильного launcher (пусковой экран), web-top, домашней страницы или экрана, новой вкладки, и всё это вместо в одном. Даже можно запустить в теории в Electron.

## 📚 Моими словами 📚

> 📓 Среда рабочего экрана второй ревизии. 📓

Разработка подобного проекта начиналась ещё в феврале 2024 году на голом энтузиазме. Со временем стало ясно что код стал слишком деформирован, заросшим, замусоренным (да и сейчас далек от идеала), и было принято решение его переписать практически заново, теперь уже используя новые стеки. С недавних пор заработало и на Mozilla Firefox (Nightly сборки).

### 🎈 Интересные функции 🎈

- Обои рабочего стола не размываются при повороте экрана и могут сохраняться на месте.
- Иконки также способны сохранять исходную позицию при поворотах экрана.
- Возможность редактировать эти самые иконки.
- Подобие дизайна из Windows 10 и Material You (т.е. Monet).

### 🚧 Запланированные функции 🚧

- [ ] Самое главное - экран приветствия, обещанное ещё с прошлого проекта.
- [ ] Сайд-бар с настройками (toggle'ы).
  - [ ] Блокировка поворотов экрана, с запоминанием
- [ ] Больше настроек...
  - [ ] Такие как кастомизация разметки.
  - [ ] Включение или выключение некоторых элементов.
  - [ ] Возможность включить или отключить статус-бар.
- [x] Статус бар самого PWA приложения как таковой.
  - [x] Использование часов (через Temporal API).
  - [ ] (Даже планируется поддержка часовых поясов).
  - [x] Battery API (индикатор).
  - [x] Индикатор подключения к сети.
  - [ ] Возможная реализация энергосбережения.
- [ ] Возможность синхронизации по облакам (причём serverless)
  - [ ] (Из коробки предполагается Яндекс.Облако.)
- [ ] Элементы и аспекты умного дома.
  - [ ] (В основном по облаку, вроде `Tuya Smart`).
- [ ] Возможно подумаю о реализации различных плагинов.
  - [ ] (В теории из `OPFS` можно прогрузить сторонние скрипты).
  - [ ] (Предполагается использование различного API).
- [ ] Больше элементов интерфейса (вроде выпадающего списка).
- [ ] Реализация менеджера плагинов и файловой системы (`OPFS`).
- [ ] Реализация ПИН-кода (или экрана блокировки).

### ❌ Утраченные функции с прошлого проекта ❌

- [x] Возможность импорта и экспорта настроек (экспериментальное).
- [ ] Возможность синхронизации по `IPFS` (Web 3.0).
- [x] Обои рабочего окружения работают теперь через Canvas а не стили.
  - [x] Для нас главное чтобы эта функция вообще была как таковая.
  - [x] Такой подход (через Canvas) просто придаёт большую стабильность.

## 📏 Аспекты которые стоило было внедрить в 2024 году 📏

### Со стороны 🥬 CSS4 🥬

- Логические размерности (`inline-size`, `block-size` и т.д.)
- Относительные цвета и смешения (на цветовой модели OkLch).
- Практически полная реализация темной и светлой темы.
- (Отчасти с JS) экспериментальная реализация масштабирования экрана.
- Использование пре-процессоров вроде SASS/SCSS.
- Адаптивность и отзывчивость (пока что мало где применимо).

### Со стороны 🍊 JavaScript 🍊

- Современный и новые синтаксис и семантика.
- Объектная ориентированность.
- Новые WeakMap/WeakRef технологии.
- Возможность использовать собственные обои благодаря OPFS.
- Возможность создавать свои иконки на рабочем столе (с указанием ссылки).
- Активное использование localStorage для ряда состояний и настроек.
- (Не тестировалось) возможность использовать в offline режиме.

### 🐱 Прочие нововведения 🐱

- Новый stack с Svelte + Vite.
- Использование Fastify сервера в готовом bundle.
- Система развёртывания конечного результата компиляции.

## 🚀 Возможность запуска данного проекта 🚀

### 💿 Просто демонстрация 💿

- 🐴 **[IDC-LX.ru](https://idc-lx.ru)** 🐴 (рекомендуется браузер *Chrome* или *Edge* от **126** версии и выше)

### 📝 Сборка из исходников 📝

**Обязательно** клонируем проект вместе с суб-модулями!

Рекомендуется NodeJS 22 версии и выше.

1. `npm install`
2. `npm run build`

Либо (сервер разработки):

1. `npm install`
2. `vite`

Операционная система Linux также в поддержке, но нет в данный момент скриптов `.sh` для запуска.

### 👨‍⚖️ Юридический аспект (открытость по лицензии) 👨‍⚖️

Поставляется по LGPL-v3 и Creative Commons BY-CA. Права (мои) частично защищены.

(Хотя стоит признать что я не силах защитить свои авторские или какие-либо права.)