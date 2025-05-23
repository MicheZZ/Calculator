# Calculator


Go-библиотека для вычислений: сумма, среднее значение, медиана, отсортированная медиана, дисперсия, диапазон, минимум, максимум, моды, стандартное отклонение и многое другое.

---

## 🚀 Начало работы

### Установка

Подключите библиотеку в своём Go-проекте:

```go
import (
    "github.com/greenpau/go-calculator"
)
```

### Инициализация калькулятора

Вы можете создать калькулятор из различных типов данных:

```go
// Из строки
calc, _ := calculator.NewString("1, 2, 3, 4.5, 5.4, 6, 7")

// Из массива uint64
arr := []uint64{1, 2, 3, 4, 5, 6, 7}
calc, _ := calculator.NewUint64(arr)

// Из массива int64
arr := []int64{1, 2, 3, 4, 5, 6, 7}
calc, _ := calculator.NewInt64(arr)

// Из массива int
arr := []int{1, 2, 3, 4, 5, 6, 7}
calc, _ := calculator.NewInt(arr)

// Из массива float64
arr := []float64{1, 2, 3, 4, 5, 6, 7}
calc, _ := calculator.NewFloat64(arr)

if calc == nil {
    log.Fatal("не удалось инициализировать калькулятор")
}
```

---

## 📊 Доступные вычисления

```go
calc.Total()                 // сумма
calc.Mean()                  // среднее
calc.Median(true)            // отсортированная медиана
calc.Median(false)           // обычная медиана
calc.Modes()                 // моды
calc.Range()                 // диапазон
calc.Min()                   // минимум
calc.Max()                   // максимум
calc.MinWithIndices()        // минимум и его индексы
calc.MaxWithIndices()        // максимум и его индексы
calc.Variance()              // дисперсия
calc.StandardDeviation()     // стандартное отклонение
```

### Все расчёты сразу

```go
calc.RunAll()
```

---

## 📥 Получение результатов

```go
fmt.Printf("Сумма: %.2f\n", calc.Register.Total)
```

---

## 🖨 Пример вывода через `Print()`

```
Данные: [554801 61602 763767 277578 167822 617342
  847743 801166 894535 254904 354657 389371
  543430]
Сумма: 6528718.000000
Среднее: 502209.076923
Медиана: 732542.500000
Отсортированная медиана: 466400.500000
Максимум: 894535.000000
Индексы максимума: [8]
Минимум: 61602.000000
Индексы минимума: [1]
Дисперсия: 69299542922.378693
Стандартное отклонение: 0.000000
Моды: []
Количество повторов моды: 0
```

---

