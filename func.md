# Функции

Функции в Go отличаются от PHP тем что:

- объявляются с помощью ключевого слова `func`
- тип каждого аргумента функции и возвращаемого значения должен быть указан
- функция может иметь несколько возвращаемых значений

Простой пример:

```go
// Функция с двумя параметрами int и одним возвращаемым значением типа int
func add(x int, y int) int {
  return x + y
}
```

Если несколько аргументов имеют одинаковый тип, что можно перечислить их через запятую:

```go
// Краткий аналог предыдущего примера
func add(x, y int) int {
  return x + y
}
```

Возврат нескольких значений:

```go
// Нет аргументов, но два возвращаемых параметра
func minMax() (int, int) {
    return 5, 6
}

// Так можно получить несколько значений
min, max := minMax()
```

Можно указывать пустой return возвращая при этом данные (naked return). Для этого
переменные должны быть объявлены сигнатуре функции.

```go
// Можно дать имена возвращаемым переменным, так можно использовать return без
// перечисления переменных
func minMax() (min int, max int) {
    max = 5 // Используется =, а не := так как переменная уже объявлена
    return
}

min, max := minMax() // Какое значение будет у min?
```

Если одно из возвращаемых значений нам не нужно, то следует
использовать пустую переменную `_`

```go
_, max := minMax()
```