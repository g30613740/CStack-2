  # Данный проект - это моё решение представленной ниже задачи _с использованием STL_.

  Определить класс `CStack` для работы со стеком целых чисел ограниченного размера. Глубина стека задаётся в конструкторе класса.
  В классе должны быть определены необходимые конструкторы (в том числе конструктор копирования и перемещения), деструктор,
  операторы присваивания (копированием и перемещением), `<<`, инкремент `++` и декремент `--` (справа и слева, работают как `push` и `pop`),
  сложения (результатом является стек из содержимого обоих из содержимого обоих стеков, при этом глубины суммируются, использовать `push` и `pop`),
  функции `push` (добавление числа в стек, если это возможно, возвращает информацию об успешности) 
  и `pop` (удаление вершины, если это возможно, с сохранением вытесненной вершины, возвращает информацию об успешности).
  В этом классе должна быть создана **чисто** виртуальная функция вывода данных класса в файл вида
  ```ruby
  virtual int output() = 0;
  ```
  От класса `CStack` надо породить два класса `CData0` и `CData1`, в первом из которых переопределить функцию
  `int output();` как функцию вывода данных класса в файл в одну строку, а во втором данную функцию определить как функцию вывода данных класса в столбец 
  (т.е. по одному элементу данных в одну строку). В файле с исходными данными в каждой строке задаются данные для одного экземпляра класса,
  порождённого от `CStack`. Данные задачи даются в виде:
  ```
  I FileName Data
  ```
  где `I = 0` или `I = 1`, `FileName` - имя выходного файла, `Data` - все данные стека, разделённые пробелами без указания длины,
  которая определяется как минимально возможная.
  Для каждой строки исходного файла надо создать объект класса `CData0`, 
  если   `I == 0`, либо экземпляр класса `CData1`, если `I == 1` и заполнить его данными `Data`. 
  Имя выходного файла следует занести в соответствующее поле созданного класса.
  Указатели на созданные объекты надо поместить в массив указателей на базовый класс `CStack** arr`. Каждый новый объект должен создаваться функцией вида
  ```ruby
  CStack* CreateData(const char *str, CFabricData **f);
  ```
  где `f` - массив фабрик для создания I-го дочернего класса от `CStack`.
  Далее надо в цикле для каждого объекта из массива arr вызвать функцию ```output()```.
  
  Также надо написать разумный тест на все реализованные функции класса. Тест должен содержать сложение объектов,
  на которые указывают сохранённые в массиве arr указатели и их циклический сдвиг.

  ### Работа на ЭВМ, IV семестр механико-математическиго факультета МГУ, преподаватель - В.М.Староверов.
