# HTML-Academy-Author-Test
I) <b>Специфичность селекторов</b>

Любой CSS-селектор имеет свою специфичность (вес), которая определяет, как взаимодействуют одни и те же свойства, которые заданы одним и тем же элементам в разных местах кода.
<br><br>Стоит заметить, что при равном весе селекторов применяются стили, объявленные в коде ниже.
<br><br>Но специфичность селекторов всегда необходимо просчитывать, поскольку иногда свойство, которое объявлено в коде ниже, перекрывается тем, что объявлено выше, из-за того, что селектор первого специфичнее второго (имеет больший вес).
<br><br>Специфичность селектора считается посредством условной разбивки по четырем буквенным составляющим — a, b, c, d:
- если стиль встроенный, то есть определён в атрибуте style (style = " "), то <b>а</b> равняется 1, иначе <b>a</b> равняется 0; 
<br>style="" 1,0,0,0 
- значением <b>b</b> является количество идентификаторов (#id) в селекторе;
<br>#id 0,1,0,0 
- значением <b>c</b> является количество классов (.class), псевдоклассов (:active) и селекторов атрибутов ([type="radio"]); 
<br>.class 0,0,1,0 
<br>:active 0,0,1,0 
<br>[type="radio"] 0,0,1,0
- значением <b>d</b> является количество селекторов типов элементов (li) и псевдо-элементов (::before).
<br>li 0,0,0,1
<br>::before 0,0,0,1

Универсальный селектор (*), комбинаторы (+, >, ~, ' ') и отрицающий псевдокласс (:not()) не влияют на специфичность. Однако селекторы, объявленные внутри :not(), влияют.

В результате данного преобразования вы получите число. Селектор, который обладает большим значением специфичности, обладает также и большим приоритетом.

II) <b>Порядок написания функции</b>
1)	Создайте функцию <b>calculateMiles</b> с параметром <b>distance</b>;
2)	В теле функции объявите переменную <b>percent</b>, равную <b>0.25</b>;
3)	С помощью условного оператора if задайте условие, в котором укажите, что переменная <b>distance больше 10500</b>;
4)	В теле оператора if задайте переменную <b>percent</b>, равную <b>0.35</b>;
5)	Функция <b>calculateMiles</b> должна возвращать произведение <b>distance</b> и <b>percent</b>;
6)	Выведите в консоль сообщение о том, сколько бонусных миль получит пассажир за полет на <b>2500</b> миль; 
7)	Выведите в консоль сообщение о том, сколько бонусных миль получит пассажир за полет на <b>5000</b> миль; 
