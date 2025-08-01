# Qt_Learning

Папка с проектами для практики в Qt/C++, автоматизации, работе с БД, документацией по ГОСТ и другим навыкам, необходимым инженеру-программисту в судоходной отрасли.

---

# Годовой план обучения: Инженер-программист в области корабельной навигации

## Цели
- Освоить C++, STL, Qt, Bash, GitLab, CMake/QMake, Boost, SQL, PVS-Studio, Redmine
- Изучить ГОСТы по разработке ПО (19.001, 19.103, 19.105, 19.301, 19.505, 15.203, 15.307)
- Реализовать проекты в области корабельной навигации

---

## Общая структура
| Этап       | Длительность | Технологии                          | Проекты                          |
|------------|--------------|-------------------------------------|----------------------------------|
| **Базовый**| 1-3 месяца   | C++, STL, Git, Bash                 | Консольные утилиты              |
| **Qt Core**| 4-6 месяцев  | Qt Core, CMake, SQL                 | Обработка навигационных данных  |
| **Продвинутый**| 7-9 месяцев| Qt GUI, Boost, PVS-Studio         | Визуализация карт               |
| **Проф.**  | 10-12 месяцев| Redmine, ГОСТы, оптимизация       | Комплексная система навигации   |

---

## Детальный план по месяцам и проекты

### Месяц 1: Основы C++, Git, Bash
**Темы:**
- Основы C++: типы данных, переменные, операторы, функции, основы ООП (классы, инкапсуляция)
- Git: базовые команды (init, add, commit, log, status), ветвление (branch, merge)
- Bash: файловая система, базовые команды, написание простых скриптов

**Проект:** Консольная утилита для расчёта дистанции между портами
- Класс GeoPoint (широта, долгота, преобразования)
- Реализация формулы Хаверсина
- Ввод координат с консоли, валидация
- Bash-скрипт для сборки и запуска
- Документация по ГОСТ (описание алгоритма, инструкция пользователя)
- Unit-тесты

### Месяц 2: STL и продвинутый C++
**Темы:**
- STL: контейнеры (vector, map, set), итераторы, алгоритмы (sort, find, for_each)
- Продвинутый C++: шаблоны, RAII, умные указатели, обработка ошибок (try/catch)
- Работа с файлами (fstream)

**Проект:** Обработчик сырых данных GPS с фильтрацией выбросов
- Парсер логов NMEA-0183 (C++)
- STL для хранения и фильтрации данных
- Алгоритмы фильтрации выбросов (например, медианный фильтр)
- Кэширование маршрутов (map/set)
- Вывод статистики по маршруту
- Документация по ГОСТ

### Месяц 3: Системы сборки и Qt Core
**Темы:**
- Системы сборки: основы CMake и QMake, структура CMakeLists.txt, qmake .pro-файлы
- Qt Core: сигналы и слоты, QObject, QTimer, основы событийной модели
- Многопоточность в Qt (QThread, QtConcurrent)
- Кроссплатформенная сборка (Astra Linux)

**Проект:** Сервис мониторинга судов с использованием AIS-потоков
- Многопоточная обработка входящих AIS-сообщений (Qt Core)
- Парсер AIS (C++/Qt)
- Сохранение данных в JSON/QSettings
- Bash-скрипт для запуска сервиса
- Документация по ГОСТ

### Месяц 4: Базы данных и SQL
**Темы:**
- Основы SQL: SELECT, INSERT, UPDATE, DELETE, JOIN, транзакции
- Qt SQL: подключение к SQLite, выполнение запросов, работа с результатами
- Оптимизация SQL-запросов
- Импорт/экспорт данных (CSV, S-57)

**Проект:** База данных навигационных карт с поиском точек интереса
- Проектирование структуры БД (SQLite)
- Импорт данных S-57 (или аналогичных)
- Реализация поиска по координатам и атрибутам
- Генерация отчётов (Qt SQL)
- Документация по ГОСТ

### Месяц 5: Qt GUI и визуализация
**Темы:**
- Qt Widgets: основы, QGraphicsView, создание и настройка виджетов
- Qt Quick (QML): основы, структура QML, анимации
- Рендеринг карт, работа с графикой
- Интерактивность: обработка событий мыши, масштабирование, панорамирование

**Проект:** Визуализатор морских карт с поддержкой слоёв
- Qt Widgets/QGraphicsView для отображения карт
- Слои: маршруты, навигационные знаки, зоны опасности
- Масштабирование, панорамирование, интерактивность
- Импорт данных из БД
- Документация по ГОСТ

### Месяц 6: Boost и безопасность
**Темы:**
- Boost: Boost.Geometry (основы, работа с геометрическими объектами), Boost.Asio (основы сетевого взаимодействия)
- PVS-Studio: статический анализ кода, устранение предупреждений
- Тестирование: Google Test, написание unit-тестов
- Оптимизация алгоритмов

**Проект:** Модуль расчёта безопасных маршрутов
- Boost.Geometry для расчётов
- Алгоритмы обхода опасных зон
- Визуализация маршрута и опасных зон
- Интеграция с PVS-Studio для анализа кода
- Unit-тесты
- Документация по ГОСТ

### Месяц 7: Интеграция и ГОСТы
**Темы:**
- ГОСТ 19.001, 19.103, 19.105, 19.301, 19.505, 15.203, 15.307: требования к документации
- Redmine: основы работы, управление задачами, ведение документации
- CI/CD: основы, настройка GitLab CI, автоматизация сборки и тестирования
- Docker: основы контейнеризации

**Проект:** Система документооборота для навигационного ПО
- Хранение и версияция документов (Qt/SQL)
- Формирование ТЗ, тест-планов, отчётов по ГОСТ
- Интеграция с Redmine (экспорт задач, статусов)
- CI/CD для автоматизации публикации документов

### Месяц 8: Комплексное приложение (ядро навигации)
**Темы:**
- Архитектура ПО: слоистая архитектура, паттерны проектирования
- Интеграция модулей: взаимодействие между компонентами
- Протоколирование событий, логирование
- Документирование архитектуры

**Проект:** Ядро ECDIS (Electronic Chart Display and Information System)
- Интеграция модулей: карты, БД, расчёты маршрутов
- Протоколирование событий по ГОСТ
- Архитектура с разделением на слои (данные, логика, UI)
- Документация архитектуры

### Месяц 9: GUI и оптимизация
**Темы:**
- QML: создание интерфейсов, работа с OpenGL
- Qt Sensors: интеграция с аппаратными датчиками (GPS, IMU)
- Оптимизация рендеринга, профилирование
- UX/UI: основы проектирования интерфейсов

**Проект:** Интерактивная панель управления судном
- QML/OpenGL для визуализации интерфейса
- Интеграция с аппаратными датчиками (GPS, IMU)
- Отображение состояния судна, маршрута, предупреждений
- Оптимизация рендеринга

### Месяц 10: Тестирование и документирование
**Темы:**
- Нагрузочное тестирование: методики, инструменты
- Оформление документации по ГОСТ 19.505-79
- PVS-Studio: аудит кода
- Redmine: управление релизами, отслеживание ошибок

**Проект:** Комплект документации для системы навигации
- Оформление документации по ГОСТ 19.ххх
- Автоматизация генерации документации (скрипты, шаблоны)
- Подготовка инструкций для пользователей и разработчиков

### Месяц 11: Внедрение и обратная связь
**Темы:**
- Пользовательское тестирование: методики, сбор обратной связи
- Сбор и анализ метрик производительности
- Адаптация под Astra Linux
- Интеграция с GLONASS/GPS

**Проект:** Полевые испытания прототипа
- Проведение тестирования на реальном оборудовании (Raspberry Pi, GPS)
- Сбор и анализ метрик производительности
- Подготовка отчёта по результатам испытаний

### Месяц 12: Финальная доработка
**Темы:**
- Исправление замечаний по итогам тестирования
- Оптимизация памяти и CPU
- Подготовка презентации
- Реализация резервного контура (fallback-сценарии)
- Подготовка к сертификации

**Проект:** Финальная версия навигационного ПО с сертификацией
- Исправление всех замечаний по итогам тестирования
- Оптимизация по памяти и CPU
- Подготовка презентации для заказчика
- Реализация резервного контура (fallback-сценарии)
- Подготовка к сертификации

---

## Дополнительные идеи для проектов (по желанию):
- **Симулятор навигации** — 3D-визуализация движения судна, моделирование манёвров, учёт ветра и течений.
- **Планировщик маршрутов с учётом погодных условий** — интеграция с API погоды, построение оптимального маршрута.
- **AIS-трекер целей** — анализ и визуализация AIS-сообщений, отслеживание судов в реальном времени.
- **Система оповещения о столкновениях** — расчёт вероятности столкновения, визуальное и звуковое оповещение.
- **Модель судового журнала** — электронный журнал событий и маршрутов.

---

## Рекомендации
1. Все проекты собирать под Astra Linux SE или Common Edition
2. Использовать стенд с реальными GPS-модулями для тестирования
3. Документацию вести в Redmine с привязкой к ГОСТам
4. Аппаратное обеспечение: Raspberry Pi 4, датчики GPS/ГЛОНАСС, IMU
5. Использовать GitLab CI/CD для автоматизации сборки и тестирования
6. Писать тесты и проводить ревью кода
7. В конце каждого месяца делать ретроспективу

---

## Критерии успеха
- Реализация 3+ проектов из списка
- Полное соответствие кода стандартам C++17
- Успешное прохождение аудита PVS-Studio
- Документация по ГОСТ 19.ххх
- Работоспособность на Astra Linux
