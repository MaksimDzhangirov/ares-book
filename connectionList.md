# Управление списком соединений

<div style="text-align:justify;">
	<p>Список соединений, созданный используя ISIS или другой программой создания принципиальных схем, содержит как минимум, список компонентов, используемых при проектировании и описание того, как их выводы связаны между собой. В отличие от других программ проектирования печатных плат, ARES может использовать эту информацию.</p>
	<p>Родной формат списка соединений Proteus называется SDF, что является сокращением от Schematic Description Format (Формат описания принципиальной схемы). Кроме информации о названии компонента и его связях, SDF файл также содержит подробную информацию о корпусе, используемом для каждого компонента и классе цепи, используемой каждой цепью. В результате можно полностью охарактеризовать печатную плату с помощью SDF файла (т. е., из программы ISIS), сохраняя физическое размещение компонентов и подробную разводку соединений.</p>
	<center><strong>Команда Load Netlist (Загрузить список соединений)</strong></center>
	<p>Загрузчик списка соединений – это средство, позволяющее импортировать данные, хранимые в файле SDF в текущую разводку печатной платы.</p>
	<p>Список соединений может быть загружен:</p>
	<ul>
		<li>в полностью пустую рабочую область проекта;</li>
		<li>с набором размещенных и обозначенных компонентов на рабочей области;</li>
		<li>или (при модификации существующего проекта) в полностью разведенную печатную плату.</li>
	</ul>
	<center><strong>Использование загрузчика списка соединений в пустом проекте</strong></center>
	<p>Когда в проекте нет компонентов, все элементы, приведенные в списке соединений, просто загружаются и обозначаются в селекторе объектов, готовые к размещению как описано в команде <strong>Component Mode</strong> из левой панели инструментов.</p>
	<center><strong>Загрузчик списка соединений и существующие компоненты</strong></center>
	<p>Когда компоненты или корпуса, имеющие обозначения, уже находятся на плате, каждый из них, который имеет такое же обозначение, как в загруженном списке соединений, связывается с базой данных списка соединений. Затем они используются при выполнении действий, связанных со списком соединений, например, составлении линий связи между компонентами. Компоненты или корпуса, имеющие обозначение, которые не указаны в списке соединений, выделяются. После этого разработчик может либо проигнорировать их или удалить, нажав клавишу <strong>Delete</strong>.</p>
	<p>ARES проверяет совпадает ли библиотека, указанная для компонента в списке соединений, с библиотекой, из которой компонент был помещен на плату. Если они отличаются, то возможен один из следующих вариантов:</p>
	<ul>
		<li>Если новый корпус имеет такое же число выводов, что и существующий, то происходит замена, причем новый корпус накладывается на старый таким образом, что первый вывод нового находится над первым выводом старого. Компонент выделяется, чтобы указать, что он был изменен.</li>
		<li>Если новый корпус имеет другое число выводов, компонент удаляется с печатной платы и добавляется в селектор объектов для ручного размещения.</li>
	</ul>
	<p>Загрузчик списка соединений игнорирует корпуса без обозначений. Это позволяет размещать посадочные места для элементов, которые по какой-то причине, не должны содержаться в списке соединений. Это также дает возможность соединять их выводы к чему угодно (поскольку они не указаны в списке соединений) без возникновения нарушений правил соединений.</p>
	<center><strong>Загрузчик списка соединений и существующая разводка печатной платы</strong></center>
	<p>В случае, когда на плате находятся и компоненты, и дорожки, ARES проверяет какие выводы соединены дорожками, чтобы проверить согласуются ли они со списком соединений. При большом увеличении масштаба текущее название цепи отображается на дорожке, если она разведена. Цепям, которые не имеют названий в ISIS, даются автоматические генерируемые численные названия.</p>
	<p>Если обнаруживается, что произошло соединение двух цепей (вероятно в результате изменения принципиальной схемы), дорожкам и переходным отверстиям, связанным с ними, присваиваются к цепи VOID.</p>
	<p>Программа проверки соединений игнорирует дорожки и переходные отверстия цепи VOID, мигающие желтым цветом, и они не выводятся на печать. Их можно удалить одним из двух способов:</p>
	<ul>
		<li>Вызвав команду <strong>Tidy</strong> из меню <strong>Edit</strong>. Эта команда выполняет также некоторые другие действия, поэтому удаление может занять некоторое время.</li>
		<li>Выбирая иконку <strong>Connectivity Highlight Mode</strong> в левой панели инструментов и два раза щелкнуть по цепи VOID в селекторе объектов, чтобы выделить её. Нажмите на клавишу <strong>Delete</strong>, чтобы удалить её.</li>
	</ul>
	<p>Дорожки цепи VOID также показывают какие участки цепи необходимо удалить после изменения проекта. Если, увидев их, пользователь решит не изменять проект, то необходимо закрыть ARES без сохранения проекта и затем восстановить принципиальную схему в первоначальное состояние.</p>
	<p>Новые соединения, указанные в списке соединений, автоматически появляются в виде дополнительных линий связи.</p>
	<center><strong>Проблемы с номерами выводов</strong></center>
	<p>Когда загружается список соединений, ARES выбирает указанный корпус для каждой компоненты и затем пытается согласовать число выводов, используемое для этой компоненты с числом выводов в библиотечном корпусе. Если в списке соединений указан номер вывода, которого нет в библиотечном корпусе, то выдается сообщение об ошибке. Проблемы могут возникать в одном из следующих случаев:</p>
	<ul>
		<li>указан неправильный корпус, например, биполярного транзистора вместо реостата.</li>
		<li>вручную не пронумерованы выводы, которые требуют не числовых значений. Например, DIN разъем имеет номера выводов, которые называются A1, A2 и т. д. Необходимо помнить, что по умолчанию ARES всегда нумерует выводы в том порядке, в котором они помещаются на плату.</li>
		<li>существуют пробелы в конце названий/номеров выводов компонента в ISIS или в номерах выводов ARES. Это можно проверить, редактируя соответствующий объект и проверяя поле <strong>Data Entry Field</strong> или <strong>Number</strong>, в котором вводится текст.</li>
	</ul>
	<p>При создании новых библиотечных корпусов, используя <strong>Packaging Tool</strong> в ISIS, необходимо избегать вышеперечисленных проблем.</p>
	<center><strong>Перестановка эквивалентных выводов и/или элементов</strong></center>
	<p>При использовании вместе с ISIS, ARES поддерживает изменение линий связи путем перестановки эквивалентных выводов и элементов при разводке. Это означает, что пользователь может поменять местами соединения подходящие к эквивалентным выводам и/или поменять местами эквивалентные элементы для компонента, содержащего несколько элементов в одном корпусе. В ARES для этого можно использовать ручную или автоматическую перестановку.</p>
	<center><strong>Ручная перестановка эквивалентных выводов и/или элементов</strong></center>
	<p>Чтобы осуществить ручную перестановку эквивалентных выводов или элементов:</p>
	<ol>
		<li>Выберите иконку <strong>Ratsnest Mode</strong> из левой панели инструментов.</li>
		<li>Нажмите правую кнопку мыши на исходной контактной площадке. Для перестановки элементов это может быть любой элемент компонента. Линии связи, подсоединенные к этому выводу, выделятся. Кроме того, также подсветятся доступные конечные контактные площадки.</li>
		<li>Зажмите левую кнопку мыши и перетащите линии связи к требуемой конечной контактной площадке.</li>
		<li>Отпустите левую кнопку мыши. ARES осуществит изменения, обновляя линии связи и направляющие вектора соответствующим образом. В случае замены элементов, ARES переместит другие линии связи автоматически.</li>
	</ol>
	<p>Перестановка эквивалентных выводов и элементов приводит к изменениям связей в проекте. ARES использует данные о возможности перестановки выводов и элементов, указанные в библиотеках ISIS, чтобы определить является ли допустимой перестановка. Если в этих данных существуют ошибки, то ARES может разрешить недопустимые перестановки. Таким образом, необходимо тщательно проверять правильность осуществляемых перестановок и возможно создать макет печатной платы для проверки правильности работы перед массовым производством.</p>
	<center><strong>Автоматическая перестановка эквивалентных выводов и/или элементов</strong></center>
	<p>В случае, когда плата содержит большое число возможных перестановок элементов очень сложно найти наилучшее расположение для элемента. Для этих случаев существует автоматический оптимизатор для перестановки элементов.</p>
	<p>Чтобы осуществить автоматическую оптимизацию для перестановки элементов, необходимо:</p>
	<ol>
		<li>Вызвать команду <strong>Gateswap Optimizer</strong> из меню <strong>Tools</strong>.</li>
		<li>ARES осуществит повторные проходки, пробуя очередной набор возможных перестановок. Процесс повторяется, пока не будет достигнуто уменьшение длины линий связи.</li>
	</ol>
	<p><strong>Gateswap Optimizer</strong> основывается исключительно на данных о возможности перестановки элементов, указанных в библиотеках ISIS, чтобы определить является ли допустимой перестановка. Если в этих данных существуют ошибки, то могут возникнуть ошибки в проекте. Таким образом, необходимо тщательно проверять правильность осуществляемых перестановок и возможно создать макет печатной платы для проверки правильности работы перед массовым производством.</p>	
	<center><strong>Синхронизация с принципиальной схемой</strong></center>
	<p>Когда осуществляется ручная или автоматическая перестановка, необходимо, чтобы изменения отражались или импортировались обратно в принципиальную схему. Для успешного выполнения этой операции, принципиальная схема не должна изменяться.</p>
	<p>PROTEUS управляет этим процессом, используя файл списка соединений как признак изменения. Если ARES не может найти обновленный список соединений, он не допустит изменений, а если в ISIS осуществляются изменения, он удаляет список соединений.</p>
	<p>Когда в ARES производятся изменения, он сохраняет файл импортирования изменений (с расширением «BAF»), как только сохраняется печатная плата. ISIS импортирует их, как только его окно станет активным. Если изменения в ARES не были сохранены, то в ISIS также не произойдет никаких изменений.</p>
	<p>Такой алгоритм работы обычно предотвращает одновременные изменения в принципиальной схеме и печатной плате. Конечно, можно обойти этот алгоритм, переименовывая файлы, редактируя их и затем, меняя названия на старые; редактируя файлы на другом компьютере и т. д. В таких случаях необходимо тщательно проверять, что принципиальная схема и печатная плата совпадают и затем перезагрузить список соединений в ARES.</p>
	<p>Дальнейшие подробности о перестановке эквивалентных выводов и/или элементов даются в разделе «ISIS и ARES».</p>
	<center><strong>Классы цепей</strong></center>
	<p>В ARES класс цепи определяет как цепь, связанная с ним будет разводиться. Эта информация включает:</p>
	<ul>
		<li>используемый стиль дорожки и переходных отверстий;</li>
		<li>тип используемого переходного отверстия – обычное, между внутренними слоями, глухое.</li>
		<li>соответствующие настройки для авторазводчика.</li>
	</ul>
	<p>Преимущество включения всех свойств в один параметр и затем назначения его цепи в отличие от назначения свойств отдельно каждой цепи заключается в значительном уменьшении количества информации, которую необходимо вводить в принципиальной схеме.</p>
	<center><strong>Классы цепей и список соединений</strong></center>
	<p>ISIS может назначить свойство цепи (в этом случае название класса цепи), присваивая ей метку цепи, например, CLASS=POWER. Эта информация затем обрабатывается компилятором списка соединений ISIS и появляется как свойство цепи после её названия.</p>
	<p>Например:</p>
	<p>VDD,2,CLASS=POWER </p>
	<p>U1,14 </p>
	<p>U2,14</p>
	<p>Если используется другая программа для создания принципиальной схемы, многое зависит от её возможности обрабатывать свойства цепи подобным образом. Если такая возможность не поддерживается, то возможны три варианта:</p>
	<ul>
		<li>Использовать названия цепи вида VDD=POWER. ARES воспримет это как цепь с названием VDD, с которой связан класс цепи POWER.</li>
		<li>Отредактировать файл списка соединений с помощью текстового редактора и добавить информацию о классе цепи вручную. Используя макросы текстового редактора, это может быть очень удобный и гибкий способ.</li>
		<li>Проигнорировать возможность добавления информации о классе цепи. Учитывая возможность автоматического назначения класса цепи, которое описано ниже, это может быть приемлемым и вероятно простейшим решением.</li>
	</ul>
	<center><strong>Классы цепей и правила проектирования</strong></center>
	<p>Классы цепей очень важны при определении правил проектирования печатной платы. Как только пользователь определил класс цепи в ISIS и передал список соединений в ARES, этот класс цепи становится доступен в <strong>Design Rule Manager</strong>, что позволяет управлять зазорами между контактными площадками и дорожками для этого класса цепи, создавая, если необходимо дополнительные правила.</p>
	<center><strong>Особые названия классов цепей</strong></center>
	<p>Основная причина необходимости различных классов цепей заключается в том, чтобы отличать цепи питания от сигнальных цепей, чтобы питающие дорожки можно было сделать толще. Также, особенно при использовании авторазводчика, часто соединения шины памяти обрабатываются особо, поскольку они должны разводиться особым образом.</p>
	<p>Названия классов цепей POWER, BUS и SIGNAL имеют особое значение и цепям с определенным названием будут назначаться эти классы цепей:</p>
	<ul>
		<li>цепям с названиями GND и VCC по умолчанию назначается класс цепи POWER, пока им явно не назначается другой класс цепи в списке соединений.</li>
		<li>цепям с названиями вида D[0] по умолчанию назначается класс цепи BUS. Такое название шин может использоваться в тех программах создания принципиальных схем, которые не имеют свойств цепи.</li>
		<li>все другие цепи по умолчанию относятся к классу цепей SIGNAL.</li>
	</ul>
	<p>Такой способ позволяет разводить большинство плат, не указывая явно классы цепей на принципиальной схеме или в списке соединений.</p>
	<center><strong>Редактирование класса цепи</strong></center>
	<p>Классы цепи создаются автоматически загрузчиком списка соединений, если они встречаются в списке соединений. Чтобы назначить определенные свойства различным полям, классы цепей необходимо отредактировать, используя команду <strong>Design Rule Manager</strong> из меню <strong>Tools</strong>.</p>
	<p>Дальнейшие подробности о классах цепей даются в разделе «ISIS и ARES».</p>

</div>