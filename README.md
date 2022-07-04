# Вопросы на собеседовании iOS разработчика.

Здесь собраны на мой взгляд самые распространненные вопросы на собеседовании iOS разработчиков разного уровня. К большинству из них даны ответы и примеры кода, где это необходимо. Ниже представлена легенда, по которой я буду маркировать вопросы разного уровня. Данная маркировка весьма условна и лишь является моим видением того, какую информацию человек должен знать, если он претендует на тот или иной уровнеь. Каждый следующий уровень включает в себя все вопросы предыдущего.

## Легенда

🟢 - `Junior` уровень  
🟡 - `Middle` уровень  
🔴 - `Senior` уровень

##### Пример кода:

```swift
let example = "Hello, Example!"
```  
> Мои комментарии данного вопроса, если есть

## Общие вопросы

### 1. 🟢 Назовите основные принципы `OOP`.

Три основных принципа OOP - `Инкапсуляция`, `Наследование`, `Полиморфизм`.

`Инкапсуляция` - механизм изолирования реализации (переменных и функций) под область видимости одного объекта.  
`Наследование` - механизм, при котором один объект может получить все свойства другого объекта, который является его предком.  
`Полиморфизм` - механим представления одного объекта через другой объект, при условии, что оба объекта являются родственниками.

> Наверное, самый стандартный и одновременно всех задолбавший вопрос на собеседовании, без которого, наверное, планета уже давно сошла бы с оси.

<br/>

### 2. 🟢 Что такое `POP`? Чем отличается `POP` от `OOP`?

`POP` - Protocol Oriented Programming, подход, при котором структура программы реализуется через протоколы (интерфейсы) и их реализацию. `POP` отличается от `OOP` тем, что при использовании `POP`, вы создаете протоколы, которые затем реализуют ваши объекты, а не создаете объекты, которые потом необходимо наследовать.

<br/>

### 3. 🟢 Чем отличается фукнция от метода?

Функция отличается от метода областью видимости. Функцию можно вызвать глобально и она не привязана ни к какому обекту, в то время, как метод можно вызвать только у экземпляра объекта. При этом метод имеет доступ ко всем полям и другим методам данного экзепляра.

<br/>

### 4. 🟡 Что такое `KVO`/`KVM`? Для чего их исользуют?

`KVO` - Key-Value Observing - механизм, при котором мы можем отслеживать изменения свойства объекта, получая доступ к данному свойству по ключу.  
`KVM` - Key-Value Modification - механизм, который позволяет нам модифицировать свойство объекта, получая доступ к данному свойству по ключу.

> Данный вопрос встречается довольно редко, поэтому многих может застать врасплох

<br/>

### 5. 🟡 Какие алгоритмы поиска и сортировки вы знаете? Какие исользуете в работе?

Здесь я рекомендую назвать только те, которые вы реально знаете, так как их могут попросить реализовать на месте. Если вы знаете и помните наизусть много алгоритмов, можете назвать пару-тройку из них.

> Лично я крайне негативно отношусь к данному вопросу, так как все мы прекрасно понимаем, что в реальности в 99% случаях будет использованы `sort()` и `filter()` из стандартной библиотеки.

<br/>

### 6. 🟡 Что такое рекурсия? Как ее правильно использовать и какие у нее есть нюансы?

`Рекурсия` - это механизм, который позволяет функции вызвать саму себя. При неосторожном использовании рекурсии, программа может провалиться в бесконечный цикл вызовов, что в итоге приведет к крашу в тот момент, когда переполнится стэк вызова функций. Для того, чтобы избежать подобного сценария у рекурсии должно быть так называемое `дно` - точка выхода из рекурсии, где функция больше не вызывает саму себя.

<br/>

### 7. 🟡 Что такое `Big-O notation`? Для чего используется?

`Big-O notation` - показатель сложности алгоритма. Данный показатель может использоваться для оценки сложности алгоритма по скорости или по памяти.

```swift
пример кода
```

> Этот вопрос очень любят, рекомендую изучить данную тему

<br/>

### 8. 🟡 Что такое реактивное программирование? Есть ли опыт написания программ реактивно?

`Реактивное программирование` - программирование, при котором общение между объектами программы происходит посредством налаживанием каналов связи между объектами. Реактивный подход очень активно использует функциональное программирование - тип программирования, при котором значения не хранятся в переменных, а высчитываются, пропускаясь через цепочку функций.

<br/>

### 9. 🟡 Что такое `Future/Promise`?

`Future` или `Promise` - два названия одного и того же подхода, одного из способов реализации рективного программирования. Это прокси (контейнер), в котором должно быть значение в каком-то времени в будущем. Изначально данный контейнер может быть пуст и при попытки получить его значение, выполнение программы блокируется до тех пор, пока значение в контейнере не появится.

<br/>

### 10. 🟡 Что такое `Publisher`/`Subscriber`?

`Publisher` и `Subscriber` - это еще один подход, с помощью которого возможна реализация реактивного программирования.  
`Publisher` - объект, который выдает значения в течении некоторого или неограниченного времени.  
`Subscriber` - объект, который подписывается на выдачу значений `publisher`'a и обрабатывает получаемые значения от него.

<br/>

### 11. 🔴 Что такое слабосвязанный код? В чем его преимущество перед сильносвязанным?

`Слабосвязанный код` - это код, который написан такм образом, при котором один фрагмент кода может быть заменен на другой фрагмент кода, не требуя при этом изменений в других фрагментах кода. Как правило это достигается при помощи протоколов. Преимущество перед сильносвязанным кодом в том, что мы можем с куда меньшими затратами сил и времени менять часть программы.
  
```swift
пример кода
```

<br/>

### 12. 🔴 Как вы оптимизируете время компиляции программы?

Вопрос достаточно обширный и зависит от методов и предпочтений каждого. Можете перечислить все, что вы используете, желательно максимально детально.

<br/>

### 13. 🔴 Как вы оптимизируете время запуска программы?

Аналогично предыдущему вопросу, просто перечисляем все способы, которые реально использовали на практике. Существует несколько самых распространенных способов данной оптимизации, они довольно легко ищутся в интернете.

<br/>

## Swift

### 1. 🟢 Какие структуры данных есть в Swift?

В Swift существуют следующие структуры данных:
* `enum`
* `struct`
* `class`
* `actor`
* `protocol`

<br/>

### 2. 🟢 Каике структуры данных относятся к `value type`? Какие к `reference type`?

К `value type` относятся `enum` и `struct`.  
К `reference type` относятся `class`, `actor` а так же `closure` и `func`. Последние две не являются структурами данных.

<br/>

### 3. 🟢 В чем отличие `value type` и `reference type` с точки зрения памяти и хранения?

Экземпляры `value type` хранятся в стеке (stack), в то время, как `reference type` хранятся в куче (heap).  
Так же, при присваивании одного экземпляра `value type` другому экземпляру того же типа, происходит копирование из одного экземпляра в другой, в то время, как при присваивании одного экземпляра `reference type` к другому экземпляру того же типа, происходит копирование ссылки на объект, а не самого объекта.

<br/>

### 4. 🟢 Что такое `closure` и зачем они нужны? Чем отличаются от `func`?

`closure` или замыкания - это анонимные функции, которые не могут принадлежать типу, но могут храниться в переменной. Так же `closure` можно определить в том месте, где ожидается параметр-функция. По своей сути `closure` и `func` - это одно и тоже.

<br/>

### 5. 🟢 `closure` - это `value type` или `reference type`? Почему? А `func`?

`closure` - это `reference type`. Если бы closure была бы `value type`, то при передаче ее в функцию, она бы копировалась, что привело бы к копированию всех объектов, которые попадают в ее список захвата и потерю контекста, где `closure` была определена.  
`func` - это так же `reference type`. По своей сути `closure` и `func` - это одно и тоже, так что и "под капотом" они реализованы одинаково. 

<br/>

### 6. 🟢 Что такое `CoW` (Copy on Write)? Как и где он реализован в Swift?

`CoW` - это механизм, при котором при присваивании одного экземпляра к другому, копирование объекта не происходит до тех пор, пока один из экземпляров не будет модифицирован. Данный механизм используется во всех `value type` типах в Swift.

<br/>

### 7. 🟢 Что такое `mutating`?

`mutating` - это ключевое слово в Swift, которое позволяет методу, который указан как `mutating`, менять `self` в `value type` типах. По умолчанию все методы `value type` типов `nonmutating`.

<br/>

### 8. 🟢 В чем отличие между `var` и `let`? Есть ли разница между `value type` и `reference type` с точки зрения `var` и `let`?

`var` - ключевое слово для объявления переменной.  
`let` - ключевое слово для объявления константы.

Переменные `value type` и `reference type` ведут себя одинаково.  
Константе `value type` не может быть присвоен другой экземпляр данного типа, а так же все ее внутренние поля не могут быть изменены.  
Константе `reference type` не может быть присвоен другой экземпляр данного типа, но ее внутренние изменяемые поля могут быть изменены.

<br/>

### 9. 🟢 Назовите все уровни доступа и что они означают в Swift?

`private` - самый закрытый уровень доступа. Поля и методы типа с данным уровнем доступа видны только внутри объявления типа и расширениях, объявленных в данном файле.  
`fileprivate` - поля и методы типа с данным уровнем доступа видны снаружи объявления типа, но только в пределах данного файла.    
`internal` - уровень доступа по умолчанию. Поля и методы типа видны снаружи объявления типа в пределах данного модуля.  
`public` - поля и методы типа видны снаружи объявления типа внутри и за пределами данного модуля. Однако, за пределами данного модуля тип с данным уровнем доступа не может быть наследован, а поля и методы перегружены.  
`open` - самый открытый уровень доступа. Тоже самое, что и `public`, но наследование и перегрузка не запрещены.

<br/>

### 10. 🟢 Чем отличается `public` и `open`?

`public` типы не могут наследоваться, а `public` поля и методы не могут перегружаться за пределами данного модуля. `open` типы, поля и методы могут.

<br/>

### 11. 🟢 Что такое `final`?

`final` - ключевое слово, которое запрещает дальнейшее наследование типа или перегрузку поля или метода типа.

<br/>

### 12. 🟢 Назовите особенности `enum` в Swift

`enum` в Swift может иметь `rawValue` отличный от `Int`, в отличии от многих языков программирования. Так же, каждое значение перечисления может иметь вложенные значения любого типа в любом количестве, включая данное перечисление. Если вложенное значение является данным перечислением, перед объявлением данного значения ставится ключевое слово `indirect`. 

<br/>

### 13. 🟢 Что такое `Optional`?

`optional` - специальное перечисление в Swift, которое позволяет показать, что значение отсутствует, что обозначается ключевым словом `nil`. 

<br/>

### 14. 🟢 Что такое `if let`?

`if let` - это конструкция безопасного разворачивания `optional`. Код внутри блока `if let` будет выполнен только в том случае, если проверяемый `optional` не равен `nil`.

```swift
var myNumber: Int? = 12
if let number = myNumber {
    print("My number is \(number)")
}
```

<br/>

### 15. 🟢 Что такое `guard`?

`guard` - это ключевое слово контроля выполнения кода, которое проверяет условие на истинность. У `guard` есть только блок `else`, который выполнится, если условие не действительно. `else` блок `guard` обязан прервать выполнение блока кода, в котором объявлен `guard`.

```swift
func increment(number: Int) -> Int {
    guard number >= 10 else {
        return number
    }
    
    return number + 1
}

let incrementedNumber = increment(number: 4) // result is 5
let notIncrementedNumber = increment(number: 13) // result is 13
```

<br/>

### 16. 🟢 В чем разница между `if let` и `guard let`?

Обе данных конструкции безопасно разворачивают `optional` и выполняют блок кода только в том случае, если значение `optional` не равно `nil`. Единственное различие в том, что `else` блок `guard` обязан выйти из блока кода, где был объявлен `guard`.

<br/>

### 17. 🟢 Что делают операторы `?`, `!` и `??`?

Оператор `?` - это оператор опционального связывания при доступе к значению `optional`.

```swift
struct Person {
    var name: String
    var lastName: String
}

var me: Person? = Person(name: "Karl", lastName: "Brown")
me?.name = "Mark"
```

Оператор `!` - это оператор небезопасного разворачивания `optional`. Должен использоваться только тогда, когда вы на 100% уверенны, что значение `optional` не равно `nil`.

```swift
var number: Int? = 10
var noNumber: Int?

print(number!) // ok, prints 10
print(noNumber!) // crash, unexpectedly found nil while unwrapping an optional value
```

Оператор `??` - это оператор безопасного разворачивания `optional` и использования его значения или предоставления значения по умолчанию, если значение `optional` равно `nil`.

```swift
var number: Int? = 10
var noNumber: Int?

print(number ?? 12) // prints 10
print(noNumber ?? 12) // prints 12
```

<br/>

### 18. 🟢 Что такое `extension`? Что может быть в `extension`, а чего нет?

`extension` или расширение - дополнение уже существующего типа. Расширить можно любой тип или протокол. `extension` может содержать методы, вычисляемые переменные, статические переменные/константы/методы. `extension` не может объявлять хранимые переменные/константы. `extension` не может перегружать переменные/методы, за исключением тех, которые имеют `objc` аттрибут или объявлены в `objc` коде. Однако, не рекомендуется перегружать подобные переменные/методы в любом случае, так как это может привести к неопределенному поведению системы.  
`extension` так же используют для предоставления протоколам реализации по умолчанию.

<br/>

### 19. 🟢 Что такое `protocol`? Для чего они используются?

`protocol` - особый тип данных, экземпляры которого не могут быть созданы. Протоколы описывают будущий функционал, но не реализовывают его. Имплементация протокола кладется на плечи конкретного типа, который собирается его реализовать. Протоколы используются для обеспечения менее связанного кода и предоставление гибкости при разработке, так как можно не полагаться на конкретные типы, а на протоколы. При таком подходе любой тип, который реализует протокол, может быть использован в данном месте программы.

<br/>

### 20. 🟢 Что такое `Any`? Что такое `AnyObject`? Для чего они используются?

`Any` - специальный тип, который является всем сразу и ничем одновременно. Каждый тип в Swift может быть привиден к типу `Any`. `Any` используется тогда, когда мы не можем использовать `generics`, но при этом хотим иметь гибкость передачи аргументов разного типа. Недостаток у такого подхода всего один: так как в итоге тип данных будет `Any`, мы должны наверняка знать, какой тип был до этого, чтобы получить возможность восстановить данные после получения.  
`AnyObject` - специальный тип, такой же, как и `Any`, но с ограничением только на `reference type`. Каждый `AnyObject` может быть `Any`, но обратное не всегда верно. Ключевое слово `AnyObject` так же используется для ограничения протокола на реализацию только `reference type` типами.

<br/>

### 21. 🟢 Назовите типы для работы с коллекциями, которые есть в Swift

В Swift есть три типа для работы с коллекциями - `Array`, `Set` и `Dictionary`.  
`Array` - массив данных. Элементы имеют порядок, доступ к элементам происходит по индексу.  
`Set` - неупорядоченное множество. В множестве не может быть двух одинаковых элементов. Равенство элементов достигается проверкой `hash` значения каждого элемента. В связи с этим элементы множества обязаны реализовать протокол `Hashable`. Доступ по индексу невозможен.  
`Dictionary` - словарь, элементы которого представляют из себя пару (ключ, значение). Ключи словаря должны быть уникальны. Это достигается ровно так же, как и в случае с множеством, через протокол `Hashable`. Значения словаря могут быть любым типом, на них не накладываются ограничения. Так же значения не должны быть уникальными. Доступ осуществляется по ключу и возвращает `optional` значение, так как элемента по заданному ключу может не быть. Реализован через `hash table`.

> Скорее всего здесь вас попросят рассказать про `hash table` поподробнее. Данный вопрос я освещать не буду, так как он чисто документальный и скорее всего никогда в жизни вам не пригодится на практике.

<br/>

### 22. 🟢 Что будет, если добавить в `Set` два объекта с одинаковым значением `hash`?

Если в `Set` попытаться положить два объекта с одинаковым значением `hash`, то при добавлении первого элемента, он будет успешно добавлен в множество. При попытке добавить второй элемент в множество, элемент добавлен не будет.

<br/>

### 23. 🟢 Что такое `forEach`/`map`/`filter`/`reduce`? Какие еще примеры функционального программирования вы знаете в Swift?

`forEach`, `map`, `filter` и `reduce` - функции протокола `Collection` в Swift, которые дают возможность работать с коллекциями, используя функциональный подход.
В данном случае:

`forEach` - выполняет блок кода для каждого элемента коллекции.

```swift
let arr = [1, 2, 3, 4]
arr.forEach { print($0) }

// prints
// 1
// 2
// 3
// 4
```

`map` - выполняет блок кода для каждого элемента коллекции, в результате чего образовывается новая коллекция такого же размера, но тип значений коллекции может быть изменен, в зависимости от того, как реализован блок кода, который передается в `map`.

```swift
let arr = [1, 2, 3, 4]
let result = arr.map { "\($0)" } // result = ["1", "2", "3", "4"] 
```
  
`filter` - выполняет блок кода для каждого элемента коллекции, результатом которого есть значение `Bool`. При возврате из блока `false`, элемент исключается из результирующей коллекции.

```swift
let map = [
    "weather": "Good",
    "temperature": 27,
    "humidity": 34.3
]

let result = map.filter { (key, _) in
    key == "temperature"
} // result = ["temperature": 27]
```
  
`reduce` - выполняет блок кода для каждого элемента коллекции, результатом которого становится накопление нового результата. Используется, как правило, для получения единого результата из коллекции.

```swift
let arr = [1, 2, 3, 4]
let resut = arr.reduce(0) { partialResult, value in
    if partialResult == 0 {
        return value
    }
    
    return partialResult * 10 + value
} // result = 1234
```

<br/>

### 24. 🟡 Что такое `weak` и `unowned`? Чем они отличаются?

`weak` и `unowned` - это два ключевых слова для создания слабой ссылки. Применимо только к экземплярам `reference type` типов. Используются для предотвращения `reference cycle`. `weak` и `unowned` отличаются между собой так же, как и операторы `?` и `!` соответственно. `weak` не гарантирует наличия значения, в результате чего может использоваться только с `optional`. `unowned` предполагает, что значение всегда будет и, по сути, является `force unwrapped optional`. Если в процессе выполнения значение `unowned` будет `nil`, при попытке обратиться к данному значению будет краш.

<br/>

### 25. 🟡 Как реализован `Optional`?

Здесь можно много говорить, но лучше один раз показать, чем сто раз рассказать, так что просто воспроизводим `enum` из стандартной библиотеки. Благо он небольшой.

```swift
enum Optional<Wrapped> {
    case some(Wrapped)
    case none
}
```

> Да, все так просто

<br/>

### 26. 🟡 Что такое `lazy var`? Для чего она используется?

`lazy var` - это переменная, инициализация которой не происходит во время инициализации экземпляра. Вместо этого инициализация `lazy var` происходит при первом обращении к этой переменной. Используется для оптимизации ресурсов, когда тяжелые или длительные операции, которые не всегда нужны, можно отложить до реальной необходимости.  
У `lazy var` есть интересный побочный эффект: так как инициализация данной переменной происходит после инициализации экземпляра, при инициализации `lazy var` `self` уже существует и может быть использован.

<br/>

### 27. 🟡 Что такое `escaping` и `nonescaping`? Для чего они используются?

`escaping` и `nonescaping` - ключевые слова, применимые только к параметрам функции, типом которых является функция. Являются механизмом оптимизации выполнения кода.  
`escaping` - сигнализирует компилятору, что функция-параметр может быть вызвана после того, как выполнение тела вызывающей ее функции закончится.  
`nonescaping`, соотвественно, гарантирует, что функция-параметр не будет вызвана после того, как тело вызывающей ее функции завершится.  
По умолчанию все параметры-функции - `nonescaping`, за исключением, если они не являются `optional`.

<br/>

### 38. 🟡 Что такое `generics`? Для чего они используются?

`genrics` - аналог шаблонов из C++, механизм парметризации типов, способ уйти от конкретного типа к передачи его как параметра и обобщения функционала для разных типов. Идеальный пример - `Array`. Мы может сделать массив любых данных, но каждый такой массив будет работать одинаково, вне зависимости от типов данных, которые он хранит. 

<br/>

### 29. 🟡 Что такое `associated type`? Для чего он используется?

`associated type` - механизм параметризации протокола. Используется для обеспечения большей гибкости работы с протоколом в силу ухода от конкретного типа к параметру. По своей сути `generics` для протокола. 

<br/>

### 30. 🟡 Какие ограничения есть для протоколов, у которых есть `associated type`?

Так как протоколы с `assotiated type` не являются достаточно конкретными, объявить переменную данного типа или передать напрямик подобный тип как параметр функции невозможно. Решений данной проблемы есть несколько, но все они, по сути своей, практически костыли.

**Почитать про any/some**

<br/>

### 31. 🟡 Сравните по скорости чтение/запись/поиск в разных коллекциях в Swift

Чтение:
* `Array` - O(1)
* `Set` - O(log n)
* `Dictionary` - O(1)

Запись:
* `Array` - O(1), в худшем случае - O(n)
* `Set` - ???
* `Dictionary` - O(1), в худшем случае - ???

Поиск:
* `Array` - O(n)
* `Set` - O(1)
* `Dictionary` - 0(log n) ???

<br/>

### 32. 🟡 Чем отличается `compactMap` от `flatMap`?

`compactMap` - функция, которая формирует новую коллекцию из текущей, исключая все элементы, значением которых является `nil`.  
`flatMap` - функция, которая не формирует новую коллекцию, но вместо этого "схлопывает" накопление `optional` до одного `optional`.

<br/>

### 33. 🟡 Чем отличается цикл `for` от `forEach`?

Цикл `for` имеет все преимущества контроля выполнения и может быть прерван раньше, чем весь цикл будет пройден.  
`forEach` не может быть прерван и гарантированно пройдет по всем элементам коллекции.

<br/>

### 34. 🔴 Можно ли объеденить код на ObjC и Swift в одном проекте? Если да, то как?

<br/>

### 35. 🔴 Можно ли объеденить код на C/C++ и Swift в одном проекте? Если да, то как?

<br/>

### 36. 🔴 Чем отличается вызов функции в Swift и отправка сообщения в ObjC?

<br/>

### 37. 🔴 Что такое `conditional conformance`? Как его реализовать и для чего используют?

<br/>

### 38. 🔴 Что такое `async/await`? Что такое `Task`? Что такое `actor`?

<br/>

### 39. 🔴 Что такое `swizzling`? В чем его преимущества/недостатки?

<br/>

### 40. 🔴 Что такое условная компиляция? Для чего она используется?

<br/>

## Паттерны

### 1. 🟢 Как расшифровывается `SOLID`?

S - single responsibility. Каждый элемент программы должен выполнять только одну роль.  
O - open-closed. Элементы программы должны быть открыты к расширению, но закрыты к модификации.  
L - Liskov substitution. Элементы программы, работающие с базовыми классами или протоколами, должны так же работать и с наследниками или реализаторами протокола.  
I - Interface segregation. Множество специализированных интерфейсов лучше, чем один большой на все сразу.
D - Dependency inversion. Строить зависимости необходимо на интерфейсах, нежеле на конкретных типах.

> Это еще один очень любимый и никому не нужный вопрос, ответ на который, по сути, гуглится ровно за 5 минут до собеседования.
> Вы должны знать принципы SOLID и использовать их там, где это необходимо, но знать наизусть слово в слово определние каждого термина - это маразм.

<br/>

### 2. 🟢 Какие паттерны используются в `iOS`?

В iOS три самых распространенных паттерна - это `singleton`, `delegate` и `observer`. С недавних пор к ним присоединились `publisher` и `actor`.

<br/>

### 3. 🟢 Что такое `Singleton`? Что с ним не так?

`Singleton` - пораждающий паттерн, который гарантирует единственность экземпляра конкретного типа. Основная проблема `Singleton` - практически полная невозможность контролировать доступ и модификацию его состояния, так как он доступен всегда из всего кода.

<br/>

### 4. 🟢 Как реализовать `Singleton` в Swift?

Еще один вопрос, когда лучше просто написать сразу код.

```swift
final class Singleton {
    static let shared = Singleton()
    
    private init() {}
} 
```

> Я видел синглтоны, которые реализовывали через `struct`. В целом это допустимо, но накладывает целый ряд дополнительных трудностей в использовании такого синглтона.

<br/>

### 5. 🟢 Что такое `Delegate`? Как его использовать?

`Delegate` - поведенческий паттерн, который перекладывает часть реализации на другой объект. Делегаты используются в iOS сплошь и рядом в основном для того, чтобы уточнить часть информации, которая зависит от вашего кода и встроить в уже готовую реализацию используемых компонентов.

> Примеры: `UITableViewDataSource` и `UITableViewDelegate`

<br/>

### 6. 🟢 Что такое `Observer`? Как его использовать?

`Observer` - поведенческий паттерн, который позволяет наладить механизм подписки на события нескольких объектам и реагировать на эти события.

> Пример: `NotificationCenter`.

<br/>

### 7. 🟢 Назовите все парттерны, которые вы знаете. Перечислите те, которые вы использовали на практике.

В принципе сейчас, наконец-то, народ начал по-немного отходить от того, что знание всех паттернов в мире показывает хоть что-то, кроме того, что у вас хорошая память. Основные паттерны, приведенные выше, знать надо, потому что они используются абсолютно везде в iOS, но что до остальных - все весьма по желанию и опционально.

> И да, все вопросы про паттерны как начинаются, так и заканчиваются на джунах, дальше это уже никому не интересно.

<br/>

## UI

### 1. 🟢 Назовите все состояния, в которых может находиться iOS приложение (Application lifecycle). Назовите примеры, когда может наступить каждое из состояний.

<br/>

### 2. 🟢 Какие из этих состояний вы используете чаще всего в работе?

<br/>

### 3. 🟢 Что такое Storyboard? Что такое Xib? Чем отличаются Xib и Nib? Для чего их используют?

<br/>

### 4. 🟢 Какие UI фреймворки доступны в iOS? Чем они отличаются?

<br/>

### 5. 🟢 Что такое UIKit?

<br/>

### 6. 🟢 Что такое AutoLayout? Для чего его используют?

<br/>

### 7. 🟢 Какое минимальное количество constraints надо задать, чтобы определить положение UIView на экране?

<br/>

### 8. 🟢 Назовите основные аттрибуты constraint и что каждый из них означает

<br/>

### 9. 🟢 Что такое contentHuggingPriority и contentCompressionResistancePriority? Как их использовать и для чего?

<br/>

### 10. 🟢 Как связаны между собой contentHuggingPriority/contentCompressionResistancePriority и constraint priority?

<br/>

### 11. 🟢 Что такое UIStackView? В чем его преимущества/недостатки?

<br/>

### 12. 🟢 Жизненный цикл UIViewController. Назовите все методы-обработчики жизненного цикла и когда каждый из них вызывается.

<br/>

### 13. 🟢 Чем отличаются frame и bounds?

<br/>

### 14. 🟢 Что такое UISegue? Как они обрабатываются? Какие есть альтернативы и в чем преимущества/недостатки каждого из них?

<br/>

### 15. 🟢 UINavigationController - что это, для чего используется и как реализован?

<br/>

### 16. 🟢 UITabController - что это, для чего используется и как реализован?

<br/>

### 17. 🟢 Что такое UITableView? Для чего его использовать и что необходимо сделать, чтобы его реализовать?

<br/>

### 18. 🟢 Что такое UICollectionView? Для чего его использовать и что необходимо сделать, чтобы его реализовать?

<br/>

### 19. 🟢 В чем отличие UICollectionView и UITableView?

<br/>

### 20. 🟢 Что такое GestureRecognizer? Какие они бывают?

<br/>

### 21. 🟢 Что такое LaunchScreen.storyboard? Можно ли динамически менять его элементы или поставить ему класс-обработчик? Почему?

<br/>

### 22. 🟡 Что такое size class? Какие они бывают? Для чего их используют?

<br/>

### 23. 🟡 Как построить UI в коде? Какие преимущества/недостатки у данного подхода?

<br/>

### 24. 🟡 В чем разница между CALayer и UIView? Для чего нужен CALayer?

<br/>

### 25. 🟡 Как можно реализовать кастомную анимацию перехода между двумя экранами?

<br/>

### 26. 🟡 UISplitViewController - что это, для чего используется и как реализован? Какие недавние изменения в нем появились?

<br/>

### 27. 🟡 В чем разница между layoutIfNeeded(), setNeedsLayout() и layoutSubviews()?

<br/>

### 28. 🟡 Что такое UIResponder? Для чего он используется? Как происходит обработка событий UIResponder?

<br/>

### 29. 🟡 Какие UI операции можно делать не на главном потоке?

<br/>

### 30. 🟡 Что такое UIScene? Для чего их используют?

<br/>

### 31. 🟡 Сколько LaunchScreen сторибордов может быть в приложении? Если более одного, то как система определяет, какой использовать сейчас?

<br/>

### 32. 🔴 Что такое CADisplayLink? Для чего его используют?

<br/>

### 33. 🔴 Что такое SwiftUI?

<br/>

### 34. 🔴 Что такое View? Для чего он используется?

<br/>

### 35. 🔴 Что такое ViewModifier? Для чего он используется?

<br/>

## Хранение данных

### 1. 🟢 Какие виды persistency вы знаете в iOS?

<br/>

### 2. 🟢 Что такое plist файл? Для чего он использутеся? Какие типы данных можно хранить в plist файле?

<br/>

### 3. 🟢 Что такое UserDefaults? Для чего они используются?

<br/>

### 4. 🟡 Что такое CoreData? Когда и для чего ее используют?

<br/>

### 5. 🟡 Какие альтернативы CoreData вы знаете и в чем их преимущества/недостатки?

<br/>

### 6. 🟡 Назовите основные элементы CoreData.

<br/>

### 7. 🟡 Где могут храниться данные из CoreData?

<br/>

### 8. 🟡 Что такое NSStoreCoordinator? Для чего его используют?

<br/>

### 9. 🟡 Что такое NSManagedObjectContext? Для чего его используют?

<br/>

### 10. 🟡 Что такое NSFetchRequest? Для чего его используют?

<br/>

### 11. 🟡 Что такое NSFetchResultsController? Для чего его используют?

<br/>

### 12. 🟡 Как работать с CoreData в многопоточной среде?

<br/>

### 13. 🟡 Как реализовать чтение/запись файла в iOS?

<br/>

### 14. 🟡 Что такое KeyChain? Для чего он используется?

<br/>

### 15. 🟡 Какой persistance вы выберете для разных типов данных?

<br/>

## Работа с сетью

### 1. 🟢 Что такое REST? Что такое RESTful API?

<br/>

### 2. 🟢 Какие виды HHTP запросов вы знаете? Какими пользуетесь чаще всего?

<br/>

### 3. 🟢 Что такое JSON? Для чего он используется?

<br/>

### 4. 🟢 Как реализовать парсинг JSON в iOS? Что такое Encodable/Decodable?

<br/>

### 5. 🟢 Что такое URLSession? Для чего его используют?

<br/>

### 6. 🟢 Что такое URL и URLRequest? В чем их отличие? Когда нужно использовать какой?

<br/>

### 7. 🟡 Какие альтернативы есть URLSession? Назовите их преимущества/недостатки

<br/>

### 8. 🟡 Что такое WebSocket? Для чего он используется? В чем отличие от обычнх HTTP запросов?

<br/>

## Управление памятью

### 1. 🟡 Какая модель работы с памятью в iOS?

<br/>

### 2. 🟡 Что такое stack и heap? Для чего используюется каждая из них?

<br/>

### 3. 🟡 Что такое счетчик ссылок? Для чего он нужен?

<br/>

### 4. 🟡 Что такое reference cycle? Когда он может произойти? Что необходимо сделать, чтобы избежать таких ситуаций?

<br/>

### 5. 🟡 Что такое memory leak? Как вычеслить memory leak? Как его избежать?

<br/>

### 6. 🔴 Что такое ObjC Runtime? Что такое диспетчиризация методов, dispatch table? Назовите преимущества и недостатки.

<br/>

## Асинхронность и многопоточность

### 1. 🟡 Что такое многопоточность? Что такое concurrency?

<br/>

### 2. 🟡 Что такое асинхронное и синхронное исполнение?

<br/>

### 3. 🟡 Что такое последовательное и параллельное исполнение? Как можно реализовать каждый из типов?

<br/>

### 4. 🟡 Какие задачи могут потребовать асинхронного выполнения?

<br/>

### 5. 🟡 Какие способы выполнения асинхронной работы в iOS вы знаете?

<br/>

### 6. 🟡 Что такое GCD? Для чего он используется?

<br/>

### 7. 🟡 Что такое Operation и OperationQueue? Для чего они используется?

<br/>

### 8. 🟡 Что такое DispatchGroup? Для чего он используется?

<br/>

### 9. 🟡 Что такое Qos (Quality of Service)? Где использутеся? Для чего? Какие есть уровни?

<br/>

### 10. 🟡 Что такое race codition? Когда может произойти такая ситуация? Как предотвратить?

<br/>

### 11. 🟡 Что такое deadlock? Когда может произойти такая ситуация? Как предотвратить?

<br/>

### 12. 🟡 Можно ли реализовать многопоточность на одноядерном процессоре?

<br/>

### 13. 🟡 Что такое globalActor и @MainActor? Для чего используются?

<br/>

### 14. 🔴 Что такое NSTread? Для чего он используется?

<br/>

### 15. 🔴 Чем отличаются GCD, OperationQueue, DispatchGroup и NSThread?

<br/>

### 16. 🔴 Что такое mutex? Для чего он используется?

<br/>

### 17. 🔴 Что такое semaphore? Для чего он использутеся? Чем отличается от mutex?

<br/>

### 18. 🔴 Как обеспечить безопасный доступ к переменной в многопоточной среде?

<br/>

## Архитектурные подходы

### 1. 🟢 Что такое клиент-серверная архитектура? В роли кого как правило выступает iOS приложение?

<br/>

### 2. 🟢 Что такое MVC? Из чего он состоит? Что не так с Apple MVC?

<br/>

### 3. 🟡 Что такое MVP? Из чего он состоит?

<br/>

### 4. 🟡 Что такое MVVM? Из чего он состоит?

<br/>

### 5. 🟡 Что такое VIPER? Из чего он состоит?

<br/>

### 6. 🔴 Что не так с VIPER? Какие минусы разных архитектурных подходов вы находили и как их решали?

<br/>

### 7. 🔴 В чем разница между MVC, MVP, MVVM и VIPER? Какие еще архитектурные подходы вы ззнаете?

<br/>

### 8. 🔴 Какие критерии выбора архитектуры при разработки приложения/фичи?

<br/>

## Debug

### 1. 🟢 Какие инструменты отладки в Xcode вы знаете? Какими пользовались?

<br/>

### 2. 🟢 Для чего используется логгирование? Какие уровни логгирования бывают?

<br/>

### 3. 🟢 Что такое llvm?

<br/>

### 4. 🟢 Что такое view hierarchy debugger?

<br/>

### 5. 🟡 Что такое thread sanitiser?

<br/>

### 6. 🟡 Что такое memory graph?

<br/>

### 7. 🟡 Какие инструменты вы используете для дебага UI приложения?

<br/>

## Git

### 1. 🟢 Что такое система контроля версий? Какие вам известны и какие вы использовали?

<br/>

### 2. 🟢 Что такое push? Pull? Fetch? Merge?

<br/>

### 3. 🟢 Что такое GitFlow? Опишите основные принципы данного подхода

<br/>

### 4. 🟢 Что такое Pull/Merge Request? Зачем их используют?

<br/>

### 5. 🟢 Что такое Code Review?

<br/>

### 6. 🟡 Для чего нужен .gitignore файл?

<br/>

### 7. 🟡 Чем отличается merge от rebase? Как решаются конфликты при использовании git?

<br/>

### 8. 🟡 Что такое Git hook? Для чего они используются? Использовали ли вы на практике?

<br/>

### 9. 🔴 Как перенести репозиторий с одного сервиса на другой? Как при этом сохранить историю коммитов?

<br/>

## Тестирование

### 1. 🟢 Что такое unit тесты? Для чего они нужны?

<br/>

### 2. 🟡 Какие преимущества и недостатки предоставляют unit тесты?

<br/>

### 3. 🟡 Назовите три основных блока unit теста

<br/>

### 4. 🟡 Чем отличается Stub от Mock?

<br/>

### 5. 🟡 Что такое TDD? Какие у него преимущества/недостатки перед другими подходами?

<br/>

### 6. 🔴 Что такое интеграционные тесты? Для чего они используются?

<br/>

### 7. 🔴 Что такое UI тесты? Для чего они нужны?

<br/>

### 8. 🔴 Что такое Snapshot тесты? Для чего они нужны?

<br/>

### 9. 🔴 Если в приложении нет ни одного теста, как вы будете расставлять приоритеты для написания unit тестов? Будете ли вы писать тесты в принципе?

<br/>

## Зависимости и сторонние библиотеки

### 1. 🟢 Что такое dependency manager? Для чего они используются? Какие приходилось использовать?

<br/>

### 2. 🟢 Что такое CocoaPods? Как их использовать?

<br/>

### 3. 🟢 Что такое Carthage? Как его использовать?

<br/>

### 4. 🟢 Что такое Swift Package Manager (SPM)? Как его использовать?

<br/>

### 5. 🟡 В чем отличие CocoaPods, Carthage и SPM? Какие у них преимущества/недостатки?

<br/>

## CI/CD и дистрибуция

### 1. 🟡 Что такое CI (continuous integration)?

<br/>

### 2. 🟡 Что такое CD (continuous delivery)?

<br/>

### 3. 🟡 Что такое AppStore Connect? Для чего его используют?

<br/>

### 4. 🟡 Что такое Testflight? Для чего его используют?

<br/>

### 5. 🟡 Как распространить билд в AppStore Connect и Testflight?

<br/>

### 6. 🟡 Что такое bundle identifier?

<br/>

### 7. 🟡 Что такое provisioning profile?

<br/>

### 8. 🟡 Что такое development certificate?

<br/>

### 9. 🟡 Что такое entitlements файл? Что в нем находится?

<br/>
