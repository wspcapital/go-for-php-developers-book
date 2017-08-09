# Подготовка к работе

## Установка

Под linux ставим из пакетов `apt install golang`

Пользователи MacOS могут воспользоваться `brew install go`

## Настройка окружения

В основном, вся настройка сводится к установке переменной окружения GOPATH, данная
переменная определяет путь к рабочей директории (workspace). GOPATH как и переменная PATH
может содержать несколько директорий разделенных двоеточием (для unix). Именно в этих
директориях Go будет искать пакеты при импорте, сначала пакет будет искаться в первой
указанной директории, затем во второй и т.д.

Подробную информацию о GOPATH можно получить введя команду ```go help gopath```.

## Структура рабочей директории

Каждая рабочая директория содержит три основных поддиректории:

- src - исходные коды
- pkg - скомпилированные пакеты
- bin - выполняемые файлы

Все примеры которые приведены в далнейшем находтся в папке `src` данного репозитория.
Вы можете склонировать данный репозиторий, чтобы а дальнейшем не набирать примеры.  

```
git clone git@github.com:pahanini/go-for-php-developers-book.git
```

Сделаем директорию репозитория рабочей.

```
cd go-for-php-developers-book && export GOPATH=`pwd`
```

В дальнейшем говоря, о рабочей директории, будем иметь ввиду директорию
с репозиторием.

## IDE

[IDEA](https://www.jetbrains.com/idea/) и [Atom](https://atom.io/) поддерживают работу
с Go через соответсвующие плагины.