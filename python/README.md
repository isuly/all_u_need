# all_u_need
Questions u can meet on Python interview

PYTHON

###### 1. Замыкание

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
  <p>
Замыкание (closure), это такая функция, которая ссылается на локальные переменные (использует их в своём теле) в области видимости, в котток я орой она была создана. Этим замыкание отличается от обычной функции, которая может использовать только свои аргументы и глобальные переменные.
  </p>
def mul(a):
  def helper(b):
    return a * b
  return helper
  <p>
<b> Local </b>
  
Эту область видимости имеют переменные, которые создаются и используются внутри функций.

<b> Enclosing</b> 
  
Суть данной области видимости в том, что внутри функции могут быть вложенные функции и локальные переменные, так вот локальная переменная функции для ее вложенной функции находится в enclosing области видимости.

<b> Global</b> 

Переменные области видимости global – это глобальные переменные уровня модуля

<b> Built-in</b> 

Уровень Python интерпретатора. В рамках этой области видимости находятся функции open, len и т.п., также туда входят исключения. Эти сущности доступны в любом модуле Python и не требуют предварительного импорта. Built-in – это максимально широкая область видимости.
</p>
</p>
</details>


###### 2. Декоратор

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
Декораторы — это, по сути, "обёртки", которые дают нам возможность изменить поведение функции, не изменяя её код.
Декоратор:

      def wraper(func):
          def wrapper():
              print('1')
              func()
              print('3')
          return wrapper

      @wraper
      def decorated_func():
          print('2')


      Декоратор с параметром:
      def parametr_decorator(param: str):
          def decorator(func):
              def new_func():
                  print('1')
                  func()
                  print('3')
              return new_func
          print(param)
          return decorator


      @parametr_decorator('parametr')
      def decorated():
          print('2')

</p>
</details>

###### 3. Генератор/итератор

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 4. Send/Throw/Close в генераторе

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 5. Множественное наследование + mro

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 6. Интерфейс/абстрактный класс

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 7. Метаклассы

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 8. Сравнение объектов

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 9. Отличие staticmethod от classmethod

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 10. Property

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 11. Изменяемые/Неизменяемые типы

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 12. Как удалить повторяющиеся элементы из списка

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 13. Тернарный оператор

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>


###### 14. Лист/Дикт комприхейшн

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 15. Классы mixins

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

</p>
</details>

###### 16. Где быстрее поиск элемента — в списке или множестве?

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

Во множестве, потому что множество работает как словарь. Значение ищется по хешу ключа. Вычисление хеша и сопоставление адреса – операции постоянной сложности, поэтому принято говорить, что поиск в словаре равен O(1).

Исключение работает только для очень маленьких списков длиной до 5 элементов. В этом случае интерпретатору будет быстрей пробежаться по списку, чем считать хеш.

</p>
</details>

###### 17. Что такое *args, **kwargs, в каких случаях они требуются?

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:

Выражения *args и ** kwargs объявляют в сигнатуре функции. Они означают, что внутри функции будут доступны переменные с именами args и kwargs (без звездочек). Можно использовать другие имена, но это считается дурным тоном.

args – это кортеж, который накапливает позиционные аргументы. kwargs – словарь позиционных аргументов, где ключ – имя параметра, значение – значение параметра.

Важно: если в функцию не передано никаких параметров, переменные будут соответственно равны пустому кортежу и пустому словарю, а не None.
</p>
</details>

###### 18. Garbage Collector

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
Python управляет объектами с помощью подсчета ссылок. Это означает, что диспетчер памяти отслеживает количество ссылок на каждый объект в программе. Когда счетчик ссылок объекта падает до нуля, что означает, что объект больше не используется, сборщик мусора (часть диспетчера памяти) автоматически освобождает память от этого конкретного объекта.

</p>
</details>

###### 19. reverse для list

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
txt = "Hello World"[::-1]

</p>
</details>

###### 20. LIST

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
Объект списка в CPython представлен нижеследующей структурой в C.

    typedef struct {
        PyObject_VAR_HEAD
        PyObject **ob_item;
        Py_ssize_t allocated;
    } PyListObject;
    
  PyObject_VAR_HEAD – заголовок;
  ob_item – массив указателей на элементы списка;
  allocated – количество выделенной памяти под элементы списка;

Объект списка хранит указатели на объекты, а не на сами объекты

</p>
</details>


###### 21. DICTIONARY

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
Словари в Python реализуются с помощью хэш-таблиц. Они представляют собой массивы, индексы которых вычисляются с помощью хэш-функций. Цель хэш-функции – равномерно распределить ключи в массиве. Хорошая хэш-функция минимизирует количество коллизий, т.е. вероятность того, что разные ключи будут иметь один хэш. В Python нет такого рода хэш-функций. Его наиболее важные хэш-функции (для строк и целочисленных значений) выдают похожие значения в общих случаях

Для хранения записи в словаре используется следующая структура C: пара ключ/значение. Хранятся хэш, ключ и значение. PyObject является базовым классом для объектов в Python.

    typedef struct {
        Py_ssize_t me_hash;
        PyObject *me_key;
        PyObject *me_value;
    } PyDictEntry;

Ключами словаря могут являться только объекты, поддерживающие хеширование. Таким образом, использовать в качестве ключей списки, словари и другие изменяемые типы не получится.

Если в словарь будут добавлены несколько значений с одним и тем же ключом, словарь сохранит последнее.
</p>
</details>

###### 22. Хешируемые Объекты

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
Объект является хешируемым, если у него есть хеш-значение, которое никогда не изменяется в течение его времени жизни (ему нужен __hash__()метод), и его можно сравнить с другими объектами (ему нужен метод __eq__()или __cmp__()). Хэшируемые объекты, которые сравниваются равными, должны иметь одинаковое хеш-значение.

Hashability делает объект пригодным для использования в качестве ключа словаря и члена набора, потому что эти структуры данных используют значение хеша внутри.

Все неизменяемые встроенные объекты Python являются хэшируемыми, в то время как нет изменяемых контейнеров (таких как списки или словари). Объекты, которые являются экземплярами пользовательских классов, по умолчанию могут быть хэшируемыми;

для того, чтобы класс был идентифицирован как изменяемый достаточно чтобы его собственная реализация __hash__() возвращала None - это будет "сигналом" для интерпретатора, что такой класс нельзя использовать в качестве ключа для словарей. 
</p>
</details>


###### 23. Скорость доступа к элементам

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
СПИСОК:
Вставка: O(n).
Получение элемента: O(1).
Удаление элемента: O(n).
Проход: O(n).
Получение длины: O(1).

СЛОВАРЬ:
Получение элемента: O(1).
Установка элемента: O(1).
Удаление элемента: O(1).
Проход по словарю: O(n).
</p>
</details>


###### 24. Lambda

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
Это анонимные функции. Они не резервируют имени в пространстве имен. Лямбды часто передают в функции map, reduce, filter.
(lambda x: x + 1)(2)
В теле лямбды может быть только выражение. pass и raise являются операторами.
</p>
</details>


###### 25. Что такое фабрика декораторов?

<details><summary><b>Ответ</b></summary>
<p>

#### Ответ:
см. декоратор с параметром
Это функция, которая возвращает декоратор. Такой декоратор редко помещают в отдельную переменную. Вместо этого декорируют результатом вызова фабрики декораторов.
</p>
</details>
