## Дисциплина "Программирование электронных приборов и систем" МИРЭА 3 курс, 5 семестр

# Практика №2

Код предназначен для управления последовательным включением и выключением светодиодов, подключенных к Arduino. 

**Краткое объяснение:**

1. **Инициализация:**
   - Определено количество светодиодов (`ledCount = 5`) и массив пинов (`leds`), к которым подключены светодиоды.
   - В функции `setup()` все пины, указанные в массиве `leds`, настроены как выходы (`OUTPUT`).

2. **Главный цикл `loop()`:**
   - **Первый цикл:** Светодиоды зажигаются по очереди:
     - Включается текущий светодиод с помощью `digitalWrite(leds[i], HIGH)`.
     - После короткой задержки (`delayTime = 100` мс) он выключается (`digitalWrite(leds[i], LOW)`).
   - **Обратный цикл:** Светодиоды зажигаются в обратном порядке, кроме первого и последнего:
     - То же самое, но в обратном направлении (`for (int i = ledCount - 2; i > 0; i--)`).

**Итог:**
Светодиоды зажигаются последовательно вперед, затем последовательно назад (создавая "движущийся" эффект). Цикл повторяется бесконечно.

https://wokwi.com/projects/416084084383470593
