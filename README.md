<h1 align="center">Описание кода</h1>
<h2>ClassLoader:</h2>
<p>Прогружаются: JvmComprehension, String, Object, Integer, System.
String, Object, Integer, System - прогружаются в первую очередь.</p>
<h2>Связавыние Linking:</h2>
<p>• Verify проверка валидности и синтаксической консистентности</p>
<p>• Prepare подготовка примитивов в статических классах (в данном случае проходит без реальной проверки)</p>
<p>• Resolve разрешение символьных ссылок (в данном случае также опускается). Следующим этапом является Inititalization -
выполняются инициализаторы static полей и методов - т.е. printAll и main.</p>
<h2>Данные, попадают в Metaspace, Stack Memory и Heap.</h2>
<p>При выполения метода main создается новая область фрейм в Stack Memory (SM).</p>
<p>В 1 пункте. В стэк загружается фрейм метода main(), 
где создается переменная int со значением 1.</p>
<p>В 2 пункте. Создается переменная и хранит в себе ссылку на объект new Object 
- новый объект создается для в heap.И записывается в кучу Heap, а ссылка o - в SM.</p>
<p>В 3 пункте.  Integer является ссылочной переменной. Переменная ii само значение объекта 
создается и храненится в heap, а ссылка сохраняется в SM.</p>
<p>В 4 пункте.  Происходит создание фрейма в SM для функции printAll и далее начинается его заполнение.</p>
<p>В 5 пункте. Происходит создание объекта Integer в Heap и сохраняется ссылка uselessVar в SM.</p>
<p>В 6 пункте. Создается новый фрейм в SM под вызов println. Перед этим будет создана строчка в String Pool - части
области памяти Heap, ссылка на которую будет передана в созданный фрейм.</p>
<p>В 7 пункте.  Создается новый фрейм в SM под вызов println. Будет создана строчка в String Pool и ссылка 
на нее будет передана в созданный фрейм.</p>