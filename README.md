# Differential-Equations-Solver

Работа выполнена в рамках лабораторной практической задачи по распределенным вычислениям. Более подробно с задачей можно ознакомиться
[здесь](https://github.com/temiksvyatov/Differential-Equations-Solver/blob/master/Complete_Task.pdf).

## 1. Решение системы обыновенных дифференциальных уравнений

Дано $N$ материальных точек с массами $m_{k}$, положения которых в
начальный момент времени заданы радиус-векторами $r_{k}$, а скорости векторами $v_{k}$, $k = \overline{1, N}$.
Требуется определить траектории всех частиц во все моменты времени от 0 до $t_{end}$.

### Формат ввода

На вход программе дается файл с массами, начальными координатами и скоростями всех материальных точек.
Первая строка файла состоит из одного числа $n$ — количества точек.

### Формат вывода

Файл формата csv, каждая строка которого имеет следующий вид:
<p align="center">
$t$ $x1$ $y1$ $x2$ $y2$ $. . .$ $xn$ $yn$
</p>

## Решение первой задачи

Обе версии решения ([итеративная](https://github.com/temiksvyatov/Differential-Equations-Solver/tree/master/Iterative%20Ver) и [парараллельная](https://github.com/temiksvyatov/Differential-Equations-Solver/tree/master/Parallel%20Ver)) приводят к детерменированному решению.

Операции над векторами и замера времени расположены в заголовочных файлах [labVector](https://github.com/Raincwail/Differential-Equations-Solver/blob/master/labVector.h) и [letsTimeIt](https://github.com/Raincwail/Differential-Equations-Solver/blob/master/letsTimeIt.h), соответственно.

Данная работа со всеми замерами была проведена при следующих конфигурациях:
| Характеристика устройства | Значение                                      |
| ------------------------- | --------------------------------------------- |
| Процессор                 | AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx |
| Тактовая частота          | 2.10 GHz                                      |
| RAM                       | 8,00 Гб                                       |

Обе версии были подвергнуты следующим экспериментам:

* 100 тел движущиеся в течение 100, 10000 и 10000 шагов
* 1000 тел движущиеся в течение 100, 1000 шагов
* 10000 тел движущиеся в течение 10 шагов

Генерация тел: [genInput](https://github.com/temiksvyatov/Differential-Equations-Solver/tree/master/Input%20Gen)

<!--## 2. Решение уравнения в частных производных

Реализовать решение задачи Дирихле для определения стационарного распределения
температур на пластине с внешними источниками тепла, на краях которой
поддерживается заданный температурный режим:
<p align="center">
$\dfrac{∂^{2}u(x, y)}{∂x^{2}} +
\dfrac{∂^{2}u(x, y)}{∂y^{2}} = f(x, y), 0 < x < 1, 0 < y < 1 $
</p>
<p align="center">
$u(0, y) = u(1, y) = u(x, 0) = u(x, 1) = c$
</p>

При организации параллельных вычислений использовать метод
Гаусса-Зейделя с разбиением сетки на горизонтальные полосы.

## Решение второй задачи

Аналогично первой, вторая задача решена [итеративно](https://github.com/Raincwail/Differential-Equations-Solver/blob/master/Dirihlet%20Distribution/iterative_ver.c) и [параллельно](https://github.com/Raincwail/Differential-Equations-Solver/blob/master/Dirihlet%20Distribution/parallel_ver.c).

Для задания переменных уравнения, используется заголовок [base](https://github.com/Raincwail/Differential-Equations-Solver/blob/master/Dirihlet%20Distribution/base.h).-->
