# Краткое описание книги "Effective Java" от Джошуа Блох

-----



## Создание и уничтожение объектов 

### 1. Рассмотрите возможность замены конструкторов статическими фабричными методами 

+ Преимущество статического фабричного метода состоит в том, что, в отличие от конструкторов, он имеет название

+ Преимущество статических фабричных методов заключается в том, что, в отличие от конструкторов, они не обязаны при каждом вызове создавать новый объект

+ Преимущество статического фабричного метода заключается в том, что, в
отличие от конструктора, он может возвратить объект, который соответствует не только
заявленному типу возвращаемого значения, но и любому его подтипу. 

+ Преимущество статических фабричных методов заключается в том, что
они уменьшают многословие при создании экземпляров параметризованных типов.

- Основной недостаток использования только статических фабричных методов
заключается в том, что классы, не имеющие открытых или защищённых конструкторов,
не могут иметь подклассов. 

- Недостаток статических фабричных методов состоит в том, что их трудно
отличить от других статических методов.

### 2. Используйте шаблон Builder, когда приходится иметь дело с большим количеством параметров конструктора. 

### 3. Обеспечивайте уникальность синглтонов с помощью закрытого конструктора или перечислимого типа 

### 4. Используйте закрытый конструктор для предотвращения создания экземпляров класса 

### 5. Избегайте создания ненужных объектов

### 6. Уничтожайте устаревшие ссылки на объекты

### 7. Остерегайтесь методов ﬁnalize

## Методы, общие для всех объектов 

### 8. Переопределяя метод equals, соблюдайте его общий контракт 

### 9. Переопределяя метод equals, всегда переопределяйте hashCode

### 10. Всегда переопределяйте метод toString85 

### 11. Соблюдайте осторожность при переопределении метода clone

### 12. Подумайте о том, чтобы реализовать интерфейс Comparable 

## Классы и интерфейсы

### 13. Сводите к минимуму доступность классов и их членов

### 14. В открытых классах используйте методы доступа, а не открытые поля

### 15. Предпочитайте неизменяемые классы

### 16. Предпочитайте композицию наследованию

### 17. Проектируйте и документируйте классы для наследования либо запрещайте его

### 18. Предпочитайте интерфейсы абстрактным классам

### 19. Используйте интерфейсы только для определения типов

### 20. Предпочитайте иерархии классов классам с метками

### 21. Используйте объекты-функции для представления стратегий

### 22. Предпочитайте статические классы-члены нестатическим

## Средства обобщённого программирования(generics)

### 23. Не используйте сырые типы в новом коде 

### 24. Избавляйтесь от предупреждений о непроверенных операциях с типами

### 25. Предпочитайте списки массивам

### 26. Предпочитайте обобщённые типы 

### 27. Предпочитайте обобщённые методы 

### 28. Используйте ограниченные подстановочные типы для увеличения гибкости API 

### 29. Рассмотрите возможность использования типобезопасных неоднородных контейнеров

## Перечислимые типы и аннотации 

### 30. Используйте перечислимые типы вместо констант int 

### 31. Используйте поля экземпляра вместо числовых значений. 

### 32. Используйте EnumSet вместо битовых полей

### 33. Используйте ЕnumМар вместо индексирования по порядковому номеру 

### 34. Имитируйте расширяемые перечислимые типы с помощью интерфейсов

### 35. Предпочитайте аннотации шаблонам именования

### 36. Используйте аннотацию Override последовательно

### 37. Используйте маркерные интерфейсы для определения типов 

## Методы 

### 38. Проверяйте правильность параметров

### 39. При необходимости создавайте защитные копии 

### 40. Тщательно проектируйте сигнатуру метода 

### 41. Соблюдайте осторожность, перегружая методы

### 42. Соблюдайте осторожность при использовании методов с переменным числом параметров 

### 43. Возвращайте массивы и коллекции нулевой длины, а не null 

### 44. Пишите комментарии Javadoc для всех открытых элементов API

## Общие вопросы программирования 

### 45. Сводите к минимуму область видимости локальных переменных

### 46. Предпочитайте циклы for-each традиционным циклам for

### 47. Изучите библиотеки и пользуйтесь ими

### 48. Если требуются точные ответы, избегайте использования типов ﬂoat и double 

### 49. Предпочитайте примитивные типы упакованным примитивным типам

### 50. Не используйте строку там, где более уместен другой тип

### 51. При конкатенации строк опасайтесь потери производительности

### 52. Используйте интерфейсы для ссылок на объекты 

### 53. Предпочитайте интерфейсы рефлексии

### 54. Соблюдайте осторожность при использовании машинозависимых методов 

### 55. Соблюдайте осторожность при оптимизации

### 56. При выборе имён придерживайтесь общепринятых соглашений

## Исключения

### 57. Используйте исключения лишь в исключительных ситуациях

### 58. Применяйте проверяемые исключения для восстановления, для программных ошибок используйте исключения времени выполнения

### 59. Избегайте ненужного использования проверяемых исключений

### 60. Предпочитайте стандартные исключения 

### 61. Выбрасывайте исключения, соответствующие абстракции

### 62. Для каждого метода документируйте все выбрасываемые им исключения

### 63. В описание исключения добавляйте информацию о сбое

### 64. Добивайтесь атомарности методов по отношению к сбоям

### 65. Не игнорируйте исключения

## Многопоточность

### 66. Синхронизируйте доступ потоков к совместно используемым изменяемым данным 

### 67. Избегайте избыточной синхронизации

### 68. Предпочитайте Executor Framework непосредственному использованию потоков

### 69. Предпочитайте утилиты параллельности методам wait и notify 

### 70. Документируйте уровень потокобезопасности

### 71. Соблюдайте осторожность при использовании ленивой инициализации 

### 72. Не полагайтесь на планировщик потоков

### 73. Не используйте класс ThreadGrou

## Сериализация

### 74. Соблюдайте осторожность при реализации интерфейса Serializable

### 75. Рассмотрите возможность использования специализированной сериализованной формы

### 76. Включайте защитные проверки в метод readObject

### 77. Для контроля экземпляров предпочитайте перечислимые типы методу readResolve

### 78. Рассмотрите возможность использования прокси-классов сериализации вместо сериализованных экземпляров
