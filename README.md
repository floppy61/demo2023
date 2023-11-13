# Техническое задание: База данных для хранения информации о кинофильмах в кинотеатре (MS SQL Server)

**Группа: ПО-42**

**Разработчик:**
- [Пашков В.](https://github.com/floppy61 "Разработчик баз данных")

# База данных

Для хранения информации используется Microsoft SQL Server 2022. Ниже приведены сведения о таблицах базы данных.

## Таблица `Администраторы`

Таблица для хранения информации об учётных записях администраторов.

| Поле      | Тип данных | Описание                     |
|-----------|------------|------------------------------|
| `ID_администратора` | Целочисленный | Уникальный идентификатор администратора |
| `ФИО` | Строковый | ФИО администратора |
| `Дата_рождения` | Дата | Дата рождения администратора |
| `Паспорт` | Строковый | Паспортные данные администратора |
| `Номер_телефона` | Строковый | Номер телефона администратора |
| `Адрес_электронной_почты` | Строковый | Адрес электронной почты администратора |
| `Логин` | Строковый | Логин администратора |
| `Пароль` | Строковый | Пароль администратора |

## Таблица `Фильмы`

Таблица для хранения информации о фильмах.

| Поле      | Тип данных | Описание                     |
|-----------|------------|------------------------------|
| `ID_фильма` | Целочисленный | Уникальный идентификатор фильма |
| `Название` | Строковый | Полное наименование фильма |
| `Жанр` | Строковый | Наименование товара |
| `Режиссёр` | Строковый | ФИО режиссёра (-ов) фильма |
| `Актёры` | Строковый | ФИО актёров фильма |
| `Хронометраж` | Строковый | Продолжительность фильма |
| `Страна` | Строковый | Страна (-ы) производства фильма |
| `Год` | Строковый | Год производства фильма |
| `Описание` | Строковый | Подробное описание фильма, его сюжет |

## Таблица `Залы`

Таблица для хранения информации о залах кинотеатра.

| Поле      | Тип данных | Описание                     |
|-----------|------------|------------------------------|
| `ID_зала` | Целочисленный | Уникальный идентификатор зала |
| `Название` | Строковый | Полное наименование зала в кинотеатре |
| `Количество_мест` | Целочисленный | Количество мест в зале |
| `Описание` | Строковый | Дополнительная информация о зале |

## Таблица `Сеансы`

Таблица для хранения информации о сеансах в залах кинотеатра.

| Поле      | Тип данных | Описание                     |
|-----------|------------|------------------------------|
| `ID_сеанса` | Целочисленный | Уникальный идентификатор сеанса |
| `ID_фильма` | Целочисленный | Уникальный идентификатор фильма |
| `ID_зала` | Целочисленный | Уникальный идентификатор зала |
| `Дата_и_время_начала` | Дата и время | Дата и время начала фильма |
| `Дата_и_время_окончания` | Дата и время | Дата и время окончания фильма |
| `Стоимость_билета` | Денежный | Стоимость одного места в зале для данного сеанса |

## Таблица `Билеты`

Таблица для хранения информации о приобретённых билетах.

| Поле      | Тип данных | Описание                     |
|-----------|------------|------------------------------|
| `ID_билета` | Целочисленный | Уникальный идентификатор билета |
| `ID_сеанса` | Целочисленный | Уникальный идентификатор сеанса |
| `Ряд` | Целочисленный | Номер выбранного ряда в зале |
| `Место` | Целочисленный | Номер выбранного места в зале |
| `ФИО_покупателя` | Строковый | ФИО владельца билета |
| `Номер_телефона` | Строковый | Номер телефона владельца билета |
| `Адрес_электронной_почты` | Строковый | Адрес электронной почты владельца билета |
