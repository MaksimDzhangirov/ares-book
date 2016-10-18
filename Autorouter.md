# Режимы работы авторазводчика

<div style="text-align:justify;">
	<p>Хотя авторазводчик ARES одновременно сложен и гибок в настройке, его очень легко использовать. Кратко рассмотрим некоторые базовые примеры того как запускать авторазводчик в разных режимах работы.</p>
	<p>Чтобы вызвать разводчик в полностью автоматическом режиме, необходимо:</p>
	<ol>
		<li>Запустить его командой Auto Router… из меню Tools в ARES.</li>
		<li>Выбрать переключатель Run Basic Schedule Automatically в разделе Execution Mode.</li>
		<li>Если необходимо, настроить число проходов, изменив значения в полях Fanout Passes, Routing Passes, Cleaning Passes, Repeat Phases, Filter Passes, поменяв значения по умолчанию.</li>
		<li>Использовать кнопку Begin Routing для автоматической разводки платы.</li>
	</ol>
	<p>Чтобы вызвать авторазводчик в скриптовом режиме, необходимо:</p>
	<ul>
		<li>Запустить его командой Auto Router… из меню Tools в ARES.</li>>
		<li>Выбрать переключатель Run Specified DO file Automatically в разделе Execution Mode.</li>
		<li>Открыть скрипт для авторазводчика (файл DO) с помощью кнопки Browse или ввести непосредственно путь к нему в поле для редактирования.</li>
		<li>Использовать кнопку Begin Routing для авторазводки платы.</li>
	</ul>
	<p>Чтобы вызвать авторазводчик в интерактивном режиме, необходимо:</p>
	<ol>
		<li>Запустить его командой Auto Router… из меню Tools в ARES.</li>
		<li>Выбрать переключатель Enter Router Commands Interactively в разделе Execution Mode.</li>
		<li>Использовать кнопку Begin Routing для авторазводки платы.</li>
		<li>внизу ARES появится командное окно, позволяющее пользователю вводить команды разводки всей платы или её выбранных областей (Рис. 103).</li>
	</ol>
	<center><img src="/images/autoroute/route.png" alt=""></center>
	<center>Рис. 103</center>
	<center><strong>Создание скриптов для авторазводки</strong></center>
	<p>ARES может запускать заранее созданные скрипты и осуществлять операции разводки, используя команды в скрипте. Эту возможность можно использовать, если известно, что определенная последовательность команд может помочь развести всю плату или приведет к лучшим результатам, чем автоматическая разводка, и пользователь хочет использовать эту последовательность для различных проектов. Наконец, для очень сложных плат этот режим работы идеален, когда, пользователь хочет, чтобы авторазводчик нашел наилучшее решение в течение несколько часов.</p>
	<center><strong>Создание и редактирование скриптов</strong></center>
	<p>ARES создает скриптовый файл после запуска авторазводчика в автоматическом режиме с выбранными дополнительными параметрами, который в общем случае успешно разводит большинство стандартных печатных плат. Его можно скопировать, отредактировать или расширить, чтобы он подходил для пользовательских проектов.</p>
	<p>Содержимое созданного скрипта показано ниже:</p>
	<code style="font-family:Courier New">
		set pad_wire_necking on <br>
		bus diagonal <br>
		fanout 5 <br>
		route 50 <br>
		clean 2 <br>
		route 50 16 <br>
		clean 2 <br>
		filter 5 <br>
		recorner diagonal <br>
		status_file <br>
	</code>
	<p>Чтобы ввести комментарии необходимо поставить перед строкой символ решетки «#».</p>
	<p>Информация по каждой команде дается в разделе «Список команд авторазводчика».</p>
	<p>Как только пользователь настроил скрипт как необходимо и сохранил его на компьютере, укажите режим работы Run Specified DO file Automatically и местоположение скрипта через команду Auto Router… в меню Tools и запустите авторазводчик.</p>
	<center><strong>Работа в интерактивном режиме</strong></center>
	<p>Работа с авторазводчиком в интерактивном режиме дает максимальную гибкость, которую можно получить при использовании авторазводчика. Он позволяет легко разводить части платы, разрешая пользователю полностью контролировать порядком и приоритетом операций разводки. Однако необходимо понимать основной список команд и различные стадии авторазводки, чтобы по максимуму использовать этот режим работы. Таким образом, этот режим используется для очень сложных проектов или когда пользователь хочет управлять последовательностью команд авторазводчика.</p>
	<p>Как только авторазводчик запущен в интерактивном режиме, пользователь увидит командное окно в нижней части основного окна редактирования ARES (Рис. 103). Важно понимать, что программа находится в режиме автоматической разводки и любая попытка изменить плату приведет к выходу из режима. Подобным образом, если пользователь переключится в другой режим (например, в режим размещения компонентов или дорожек), то произойдет выход из режима авторазводки и ARES закроет командное окно.</p>
	<p>В общем случае, после входа в интерактивный режим разводки, пользователь может:</p>
	<ul>
		<li>Вводить команды для управления авторазводчиком;</li>
		<li>Использовать мышь для выбора области, которую необходимо развести.</li>
		<li>Использовать селектор объектов для выбора цепи.</li>
		<li>Использовать мышь или клавиатуру для перемещения по плате.</li>
	</ul>
	<p>Другие операции приведут к выходу из режима авторазводки.</p>
	<center><strong>Определение цепей для авторазводки</strong></center>
	<p>По умолчанию, любые команды, которые пользователь вводит в командной строке, будут влиять на всю плату. Например, если ввести «route 20», то осуществиться двадцать проходов для разводок дорожек на всей плате. Однако, достаточно часто требуется развести определенную область платы (например, небольшую область с посадочными местами для поверхностного монтажа) до разводки всей платы. Это можно сделать в ARES, просто растягивая прямоугольное выделение вокруг области платы, которую необходимо развести (Рис. 104).</p>
	<p>Создав прямоугольную область для выделения, пользователь может:</p>
	<ol>
		<li>ограничить область выделения только цепями, полностью входящими в область выделения;</li>
		<li>расширить выделение всеми цепями, которые частично входят в выделение.</li>
	</ol>
	<p>Пользователь может переключаться между этими двумя возможностями через иконку выбора дорожек Track Selection Mode в фильтре для выбора объектов.</p>
	<p>В противном случае, можно ограничить начальную разводку только определенной цепью. Для этого просто нажмите левой кнопкою мыши на контактной площадке этой цепи – при этом подсветятся все линии связи этой цепи и любые последующие команды будут применяться только к выбранным объектам.</p>
	<p>Если существует какое-либо выделение, то команды разводки будут ограничены только этими выделениями. Чтобы вернуться к глобальной разводке, необходимо нажать левую кнопку мыши на пустой области печатной платы, чтобы снять выделение со всех выделенных в текущий момент объектов.</p>
	<center><img src="/images/autoroute/pl.png" alt=""></center>
	<center>Рис. 104</center>
	<center><strong>Стадии разводки</strong></center>
	<p>В интерактивном режиме пользователь может управлять авторазводчиком, определяя что необходимо развести (с помощью выделения) и затем вводя команды для непосредственного управления процессом разводки. Для успешного управления процессом разводки нужно иметь представление о трех стадиях стандартной процедуры разводки.</p>
	<center><strong>Подготовка</strong></center>
	<p>Это первая стадия, в которой используются команды для обработки сложно разводимых объектов. Примером может быть команда ‘fanout’, которая используется до разводки, чтобы упростить доступ к посадочным местам для поверхностного монтажа.</p>
	<center><strong>Разводка</strong></center>
	<p>Это основная стадия и в ней обычно используются две команды: ‘route’ и ‘clear’. Необходимо помнить, что авторазводчик – адаптивный, т. е. если плата не развелась полностью можно повторить процесс разводки.</p>
	<center><strong>Очистка</strong></center>
	<p>После завершения стадии разводки вводятся команды для очистки платы. Здесь можно использовать команду ‘filter’, если плата разведена не полностью и команду ‘recorner’, чтобы минимизировать длину дорожек и скопление припоя в уголках дорожек.</p>
	<p>Хороший пример последовательности набора команд, который можно использовать для стандартных плат, дан в стандартном скрипте, создаваемом ARES, в разделе «Создание и редактирование скриптов».</p>
	<p>Синтаксис команд и примеры использования приведены в следующем разделе.</p>
	<center><strong>Список команд авторазводчика</strong></center>
	<p>Ниже дается описание набора команд, доступных пользователю, которые выполняют операции разводки в ARES. Эти команды можно ввести непосредственно при разводке в интерактивном режиме или использовать для создания пользовательских скриптов для разводки при работе в скриптовом режиме. В общем случае используются только первые шесть из этих команд для интерактивного режима, тогда как некоторые дополнительные команды применяются для скриптов. Для каждой команды дано описание, синтаксис команды и пример.</p>
	<center><strong><em>Команда BUS</em></strong></center>
	<p>Эта команда вызывает проход для разводки шины для группы выводов, имеющих одинаковые координаты X или Y, у которых дорожки должны быть параллельны друг другу, например, при разводке шин памяти. По умолчанию дорожки разводятся ортогонально, если не выбрана опция диагональной разводки. Обычно эта команда должна вызываться первой в скрипте для разводки.</p>
	<p>Основной синтаксис:	<code style="font-family:Courier New">bus [diagonal]</code></p>
	<p>Пример:	<code style="font-family:Courier New">bus diagonal</code></p>
	<center><strong><em>Команда FANOUT</em></strong></center>
	<p>Эта команда разводит небольшие дорожки с переходным отверстием на конце от контактных площадок для поверхностного монтажа. Её рекомендуется использовать в начале авторазводки, когда существует более двух сигнальных слоев. Не рекомендуется использовать её для двухсторонних плат, поскольку она уменьшает область для разводки дорожек.</p>
	<p>Обычно эта команда должна вызываться сразу после команды BUS и до любых команд разводки.</p>
	<p>Основной синтаксис:	<code style="font-family:Courier New">fanout &lt;number of passes&gt;</code>,</p>
	<p>где <code style="font-family:Courier New">&lt;number of passes&gt;</code> – число проходов.</p>
	<p>Пример:	<code style="font-family:Courier New">fanout 5</code></p>
	<p>	Направление дорожек может быть настроено так, что переходные отверстия будут формироваться внутри компонентов для поверхностного монтажа и/или снаружи. Разводка таких дорожек может быть ограничена типом вывода, например, только для выводов, соединенных с цепями питания.</p>
	<p>Полный синтаксис: <code style="font-family:Courier New">fanout [&lt;passes&gt;]</code> </p>
	<p><code style="font-family:Courier New">[(direction[in_out|in|out])]</code> </p>
	<p><code style="font-family:Courier New">[(pin_share [on|off])] [(via_share [on|off])]</code> </p>
	<p><code style="font-family:Courier New">{[(pin_type [active|signal|power|unused|all|single])]}</code> </p>
	<p><code style="font-family:Courier New">[(max_len &lt;positive_dimension&gt;)]</code>,</p>
	<p>где <code style="font-family:Courier New">&lt;passes&gt;</code> – число проходов;</p>
	<p><code style="font-family:Courier New">direction</code> – направление дорожек: <code style="font-family:Courier New">in</code> – внутри компонентов, <code style="font-family:Courier New">out</code> – снаружи компонентов, <code style="font-family:Courier New">in_out</code> – внутри и снаружи компонентов.</p>
	<p><code style="font-family:Courier New">pin_share</code> – использование контактных площадок, для подсоединения к ним нескольких дорожек: <code style="font-family:Courier New">on</code> – разрешено, <code style="font-family:Courier New">off</code> – запрещено.</p>
	<p><code style="font-family:Courier New">via_share</code> – использование переходных отверстий, для подсоединения к ним нескольких дорожек: <code style="font-family:Courier New">on</code> – разрешено, <code style="font-family:Courier New">off</code> – запрещено.</p>
	<p><code style="font-family:Courier New">pin_type</code> – тип вывода: <code style="font-family:Courier New">active</code> – активный, <code style="font-family:Courier New">signal</code> – сигнальный, <code style="font-family:Courier New">power</code> – питающий, <code style="font-family:Courier New">unused</code> – не используемый, <code style="font-family:Courier New">all</code> – все выводы; <code style="font-family:Courier New">single</code> – определенный, указанный.</p>
	<p><code style="font-family:Courier New">max_len</code> – максимальная длина разводимых дорожек: <code style="font-family:Courier New">&lt;positive_dimension&gt;</code> – положительное число, определяющее длину дорожки.</p>
	<p>Примеры:</p>
	<p>Задание глубины для глухих и внутренних переходных отверстий:</p>
	<p><code style="font-family:Courier New">fanout (depth opposite 2) (share_len 500)</code></p>
	<p>Задание типа вывода сигнал и разрешение использования переходных отверстий, для подсоединения к ним нескольких дорожек</p>
	<p><code style="font-family:Courier New">fanout 5 (pin_type signal) (via_share on)</code></p>
	<p>Разводка дорожек, используя сетку для переходных отверстий 25 мил</p>
	<p><code style="font-family:Courier New">fanout [via_grid 25]</code></p>
	<center><strong><em>Команда ROUTE</em></strong></center>
	<p>Эта команда указывает авторазводчику осуществлять определенное число проходов по разводке дорожек и является основной командой, используемой при авторазводке. Обычно эта команда используется вместе с командой CLEAR для осуществления разводки всей платы. Параметр &lt;start_pass&gt; используется только для второй или последующих стадий разводки и определяет начальный весовой коэффициент первой проходки разводки для этого набора разводок.</p>
	<p>Основной синтаксис: <code style="font-family:Courier New">route &lt;number of passes&gt;, &lt;start_pass&gt;</code>,</p>
	<p>где <code style="font-family:Courier New">&lt;number of passes&gt;</code> – число проходов.</p>
	<p>Пример:</p>
	<p><code style="font-family:Courier New">route 20</code> (первая стадия разводки)</p>
	<p><code style="font-family:Courier New">route 20, 16</code> (последующие стадии разводки)</p>
	<center><strong><em>Команда CLEAN</em></strong></center>
	<p>Команда CLEAR в основном удаляет и повторно разводит каждую цепь с высоким весовым коэффициентом для переходных отверстий и с самым высоким весовым коэффициентом, связанным с нарушениями по зазорам и пересечениям дорожек. Эта команда обычно используется вместе с командой ROUTE для осуществления нескольких проходов по разводке:</p>
	<p><code style="font-family:Courier New">route 20</code></p>
	<p><code style="font-family:Courier New">clear 2</code></p>
	<p><code style="font-family:Courier New">route 30</code></p>
	<p><code style="font-family:Courier New">clear 5</code></p>
	<p>и т. д.</p>
	<p>Однако после завершения разводки платы команда CLEAR может использоваться, чтобы минимизировать число переходных отверстий.</p>
	<p>Основной синтаксис:	<code style="font-family:Courier New">clean &lt;number of passes&gt;</code>,</p>
	<p>где <code style="font-family:Courier New">&lt;number of passes&gt;</code> – число проходов.</p>
	<p>Пример:	<code style="font-family:Courier New">clear 2</code></p>
	<center><strong><em>Команда FILTER</em></strong></center>
	<p>В конце разводки пользователь может захотеть удалить дорожки/переходные отверстия с конфликтами (с пересечениями или расположенные слишком близко друг к другу). Команда FILTER удалит эти конфликты, убрав минимальное число конфликтующих дорожек.</p>
	<p>Основной синтаксис:	<code style="font-family:Courier New">filter &lt;number of passes&gt;</code>,</p>
	<p>где <code style="font-family:Courier New">&lt;number of passes&gt;</code> – число проходов.</p>
	<p>Пример: <code style="font-family:Courier New">filter 5</code></p>
	<center><strong><em>Команда RECORNER</em></strong></center>
	<p>Команда RECORNER изменяет угол разводки дорожек с 90 градусов на 135 градусов. Она выполняется для углов выходных выводов и переходных отверстий. Эта команда используется после завершения разводки, чтобы уменьшить длину дорожек и обычно выполняется последней.</p>
	<p>Основной синтаксис: <code style="font-family:Courier New">recorner [diagonal]</code></p>
	<p>Пример: <code style="font-family:Courier New">recorner diagonal</code></p>
	<center><strong><em>Команда CHECK</em></strong></center>
	<p>Это команда может использоваться для запуска проверки правил проектирования и визуального выделения нарушений. Она используется в частности, когда изменяется правило проектирования. Проверка автоматически вызывается после каждого прохода разводки. Общее число нарушений показывается на панели задач и на печатной плате, чтобы показать конфликты.</p>
	<p>Основной синтаксис: <code style="font-family:Courier New">check</code></p>
	<p>Пример: <code style="font-family:Courier New">check</code></p>
	<center><strong><em>Команда CIRCUIT</em></strong></center>
	<p>Команда используется для планирования приоритетов операций разводки, использования специальных переходных отверстий и допустимых слоев для цепей и классов цепей.</p>
	<p>Основной синтаксис:</p>
	<p><code style="font-family:Courier New">class &lt;class_id&gt; | net &lt;net_id&gt; circuit {&lt;circuit_descriptor&gt;}</code></p>
	<p><code style="font-family:Courier New">&lt;circuit_descriptor&gt;:=</code> </p>
	<p><code style="font-family:Courier New">[(priority &lt;positive_integer&gt; |</code> </p>
	<p><code style="font-family:Courier New">(use_via {&lt;padstack_id&gt;}) |</code> </p>
	<p><code style="font-family:Courier New">(use_layer {&lt;layer_name&gt;})]</code> </p>
	<p>Значение приоритетов меняются от 0 до 255, значение по умолчанию равно 10.</p>
	<p>Правило use_via назначает один или несколько стеков переходных отверстий классу или цепи. Если определен более чем один стек контактных площадок, авторазводчик будет использовать наименьший по размеру.</p>
	<p>Правило use_layer назначает слои для разводки, на которых должны быть разведены цепи классы цепей. Заметьте, что правило use_layer имеет преимущество над правилом общей разводки.</p>
	<p>Примеры:</p>
	<p>Разводка цепи/класса цепей на определенных слоях:</p>
	<p>Разводка цепи sig1, используя слои L1 и L2</p>
	<p><code style="font-family:Courier New">net sig1 (circuit (use_layer L1 L2))</code></p>
	<p>Разводка класса цепи fast, используя слои M1 и M2</p>
	<p><code style="font-family:Courier New">class fast (circuit (use_layer M1 M2))</code></p>
	<p>Назначение приоритета разводки:</p>
	<p>Разводка цепи sig1 c приоритетом 200</p>
	<p><code style="font-family:Courier New">net sig1 (circuit(priority 200))</code></p>
	<p>Разводка определенного класса на указанных слоях и используя указанные переходные отверстия:</p>
	<p>Разводка классов цепей special, net1, net2, net3, net4, net5 на слоях SIGNAL_1 SIGNAL_3 SIGNAL_4 SIGNAL_5 SIGNAL_6 SIGNAL_2, используя переходные отверстия via.VIA1__1_10.bv1_10 via.VIA3__4_5.bv4_5 via.VIA3__6_7.bv6_7 с правилом rule:</p>
	<code style="font-family:Courier New">(class special net1 net2 net3 net4 net5 <br>
		(circuit <br>
		(use_via via.VIA1__1_10.bv1_10 via.VIA3__4_5.bv4_5 via.VIA3__6_7.bv6_7) <br>
		(use_layer SIGNAL_1 SIGNAL_3 SIGNAL_4 SIGNAL_5 SIGNAL_6 SIGNAL_2) <br>
		) <br>
		(rule <br>
		(width 0.007) <br>
		(clearance 0.007) <br>
		(clearance 0.001 (type via_via_same_net)) <br>
		(clearance 0.001 (type smd_via_same_net)) <br>
		) <br>
		) <br>
	</code>
	<center><strong><em>Команда COST</em></strong></center>
	<p>Эта команда присваивает определенные значения весовым коэффициентам, определенным внутри алгоритма разводки. По умолчанию, некоторые из весовых значений изменяются во время авторазводки. Не рекомендуется изменять весовые коэффициенты <code style="font-family:Courier New">cross</code> и <code style="font-family:Courier New">squeeze</code>.</p>
	<p>Значения весов могут меняться в пределах от 0 до 100. Значение –1 сбросит значение весового коэффициента. Можно использовать заранее определенные значения весов, приведенные в таблице 9.</p>
	<p>Таблица 9 - Заранее определенные значения весов</p>
	<div>
		<table>
			<tbody>
				<tr>
					<td style="text-align:center; font-weight: bold;">Название веса</td>
					<td style="text-align:center; font-weight: bold;">Значение</td>
				</tr>
				<tr>
					<td style="text-align:center;">Forbidden</td>
					<td style="text-align:center;">100</td>
				</tr>
				<tr>
					<td style="text-align:center;">High</td>
					<td style="text-align:center;">50</td>
				</tr>
				<tr>
					<td style="text-align:center;">Medium</td>
					<td style="text-align:center;">25</td>
				</tr>				
				<tr>
					<td style="text-align:center;">Low</td>
					<td style="text-align:center;">8</td>
				</tr>				
				<tr>
					<td style="text-align:center;">Free</td>
					<td style="text-align:center;">0</td>
				</tr>
			</tbody>
		</table>
	</div>
	<p>Можно изменить следующие весовые коэффициенты:</p>
	<p><code style="font-family:Courier New">cross</code> – весовой коэффициент конфликтов при пересечении дорожек;</p>
	<p><code style="font-family:Courier New">squeeze</code> – весовой коэффициент конфликтов зазоров между дорожками;</p>
	<p><code style="font-family:Courier New">via</code> – весовой коэффициент конфликтов зазоров между дорожками и переходными отверстиями;</p>
	<p><code style="font-family:Courier New">way</code> – весовой коэффициент разводки дорожек в направлении не предпочитаемом для данного слоя;</p>
	<p><code style="font-family:Courier New">off-grid</code> – весовой коэффициент разводки дорожек вне сетки, если определена сетка;</p>
	<p><code style="font-family:Courier New">off-center</code> – весовой коэффициент разводки дорожки от контактной площадки для поверхностного монтажа не от её центра;</p>
	<p><code style="font-family:Courier New">side exit</code> – весовой коэффициент разводки дорожки от контактной площадки для поверхностного монтажа поперек её большей стороны.</p>
	<p><code style="font-family:Courier New">layer</code> – если типом является <code style="font-family:Courier New">length</code> – это весовой коэффициент использования данного слоя; если типом является <code style="font-family:Courier New">way</code> – это весовой коэффициент разводки дорожек в направлении не предпочтительном для данного слоя.</p>
	<p>Основной синтаксис:</p>
	<p><code style="font-family:Courier New">cost &lt;cost_type&gt; &lt;cost_descriptors&gt;|[(type[length|way])] |-1]]</code></p>
	<p>Примеры:</p>
	<p>Присвоение весового коэффициента forbidden слою S1:</p>
	<p><code style="font-family:Courier New">cost layer S1 forbidden</code></p>
	<p>Присвоение весового коэффициента <code style="font-family:Courier New">high</code> коэффициенту разводки дорожек в направлении не предпочтительном для данного слоя для слоя S2:</p>
	<p><code style="font-family:Courier New">cost layer S2 high (type way)</code></p>
	<p>Присвоение весового коэффициента <code style="font-family:Courier New">high</code> коэффициенту конфликтов зазоров между дорожками и переходными отверстиями:</p>
	<p><code style="font-family:Courier New">cost via high</code></p>

	<center><strong><em>Команда DIRECTION</em></strong></center>
	<p>Изменяет предпочтительное направление проведения дорожек для слоя.</p>
	<p>Основной синтаксис:</p>
	<p><code style="font-family:Courier New">direction &lt;layer name&gt; [horizontal|vertical|orthogonal|off]</code>,</p>
	<p>где <code style="font-family:Courier New">&lt;layer name&gt;</code> – название слоя:</p>
	<p><code style="font-family:Courier New">horizontal</code> – предпочтительное направление горизонтальное;</p>
	<p><code style="font-family:Courier New">vertical</code> – предпочтительное направление горизонтальное;</p>
	<p><code style="font-family:Courier New">orthogonal</code> – предпочтительное направление горизонтальное и вертикальное;</p>
	<p><code style="font-family:Courier New">off</code> – для этого слоя предпочтительное направление отключено.</p>
	<center><strong><em>Команда GRID</em></strong></center>
	<p>Определяет размер сетки для дорожек и переходных отверстий</p>
	<p>Основной синтаксис: </p>
	<p><code style="font-family:Courier New">grid [via&lt;positive_value&gt;[&lt;via_id&gt;] | wire&lt;positive_value&gt;[&lt;layer_name&gt;]</code>,</p>
	<p>где </p>
	<p><code style="font-family:Courier New">via</code> – размер сетки для переходного отверстия, определяемый значением <code style="font-family:Courier New">&lt;positive_value&gt;</code></p>
	<p><code style="font-family:Courier New">&lt;via_id&gt;</code> – идентификатор переходного отверстия</p>
	<p><code style="font-family:Courier New">wire</code> – размер сетки для дорожек, определяемый значением &lt;positive_value&gt;.</p>
	<p><code style="font-family:Courier New">&lt;layer_name&gt;</code> – название слоя, на котором будут находится дорожки.</p>
	<p>Примеры:</p>
	<p>Определяем размер сетки 8.333 для дорожек</p>
	<p><code style="font-family:Courier New">grid wire 8.333</code></p>
	<p>Определяем размер сетки 5 для дорожек на слое layer 1</p>
	<p><code style="font-family:Courier New">grid wire 5 layer 1</code></p>
	<center><strong><em>Команда LIMIT</em></strong></center>
	<p>Команда LIMIT устанавливает абсолютные предельные значения, применяемые для каждого соединения. Определяет максимально допустимое число пересекающихся дорожек, число переходных отверстий для каждого соединения, число изгибов дорожек и максимальное расстояние для разводки дорожек в направлении, не предпочтительном для слоя. Диапазон значений для команды может меняться от 0 до 255. Пользователь может установить предельные значения, осуществить некоторые проходы по разводке и вернуться к значениям по умолчанию, выполняя команду LIMIT со значением –1. Если предельные значения не определены, авторазводчик использует значения по умолчанию.</p>
	<p>Основной синтаксис:</p>
	<p><code style="font-family:Courier New">limit [cross [&lt;positive_integer&gt; | -1] |</code></p>
	<p><code style="font-family:Courier New">via [&lt;positive_integer&gt; | -1] |</code> </p>
	<p><code style="font-family:Courier New">bend [&lt;positive_integer&gt; | -1] |</code> </p>
	<p><code style="font-family:Courier New">way [&lt;positive_dimension&gt; | -1]]</code>,</p>
	<p>где <code style="font-family:Courier New">cross</code> – максимально допустимое число пересекающихся дорожек, определяемое целым числом <code style="font-family:Courier New">&lt;positive_integer&gt;</code>;</p>
	<p><code style="font-family:Courier New">via</code> – максимально допустимое число переходных отверстий для каждого соединения, определяемое положительным целым числом <code style="font-family:Courier New">&lt;positive_integer&gt;</code>;</p>
	<p><code style="font-family:Courier New">bend</code> – максимально допустимое число изгибов дорожек, определяемое положительным целым числом <code style="font-family:Courier New">&lt;positive_integer&gt;</code>;</p>
	<p><code style="font-family:Courier New">way</code> – максимальное расстояние для разводки дорожек в направлении, не предпочтительном для слоя, определяемое положительным размером <code style="font-family:Courier New">&lt;positive_dimension&gt;</code>.</p>
	<p>Пример:</p>
	<p>Установить число переходных отверстий для каждого соединения равное 2:</p>
	<p><code style="font-family:Courier New">limit via 2</code></p>
	<p>Установить значение максимального расстояния для разводки дорожек в направлении, не предпочтительном для слоя, равное 200:</p>
	<p><code style="font-family:Courier New">limit way 200</code></p>
	<p>Установить значение максимального расстояния для разводки дорожек в направлении, не предпочтительном для слоя, принятое по умолчанию:</p>
	<p><code style="font-family:Courier New">limit way –1</code></p>
	<center><strong><em>Команда LOCK</em></strong></center>
	<p>Запрещает авторазводчику изменять или удалять указанные дорожки. Учтите также, что авторазводчик не может также подсоединять дорожки к указанным дорожкам.</p>
	<p>Основной синтаксис:</p>
	<p><code style="font-family:Courier New">lock net &lt;name&gt;</code>,</p>
	<p>где <code style="font-family:Courier New">&lt;name&gt;</code> – название цепи.</p>
	<center><strong><em>Команда PROTECT</em></strong></center>
	<p>Запрещает авторазводчику изменять или удалять указанные защищенные дорожки. Эту команду можно использовать для защиты заранее разведенных цепей питания и земли. Заметьте, что авторазводчик также может присоединять дорожки к указанным дорожкам.</p>
	<p>Основной синтаксис: <code style="font-family:Courier New">protect all wires</code></p>
	<center><strong><em>Команда RULE</em></strong></center>
	<p>Используется для создания нового правила проектирования. Правила могут быть назначены глобальной (для всей печатной платы) или конкретно для слоев, классов цепей или цепи. Заметьте, что в общем случае они задаются системой правил проектирования в ARES, поэтому эту команду стоит использовать только при работе в скриптовом режиме.</p>
	<p>Существует два вида правил: правила для зазоров и правила для дорожек, как видно из описания правила, указанного ниже.</p>
	<p>Основной синтаксис:</p>
	<p><code style="font-family:Courier New">rule [pcb|layer&lt;layer_name&gt;|class &lt;class_id&gt;| net<net_id>|]{&lt;rule_descriptors&gt;}</code>, где</p>
	<p><code style="font-family:Courier New">pcb</code> – правило для всей печатной платы;</p>
	<p><code style="font-family:Courier New">layer &lt;layer_name&gt;</code> – правило для слоя с названием <code style="font-family:Courier New">&lt;layer_name&gt;</code>;</p>
	<p><code style="font-family:Courier New">class &lt;class_id&gt;</code> – правило для класса цепи с названием <code style="font-family:Courier New">&lt;class_id&gt;</code>;</p>
	<p><code style="font-family:Courier New">net&lt;net_id&gt;</code> – правило для цепи с названием <code style="font-family:Courier New">&lt;net_id&gt;</code>;</p>
	<p><code style="font-family:Courier New">&lt;rule_descriptors&gt;</code> – описание правила.</p>
	<p>&lt;rule_descriptor&gt;:= </p>
	<p><code style="font-family:Courier New">[(clearance &lt;positive_dimension&gt;</code> </p>
	<p><code style="font-family:Courier New">[(type {&lt;clearance_type&gt;})])] |</code> </p>
	<p><code style="font-family:Courier New">[(junction_type [term_only | all])] |</code> </p>
	<p><code style="font-family:Courier New">[(limit_bends [&lt;positive_integer&gt; | -1])] |</code> </p>
	<p><code style="font-family:Courier New">[(limit_crossing [&lt;positive_integer&gt; | -1])] |</code> </p>
	<p><code style="font-family:Courier New">[(limit_vias [&lt;positive_integer&gt; | -1])] | </code></p>
	<p><code style="font-family:Courier New">[(limit_way [&lt;positive_integer&gt; | -1])] |</code> </p>
	<p><code style="font-family:Courier New">[(max_total_vias [&lt;positive_integer&gt; | -1])] |</code> </p>
	<p><code style="font-family:Courier New">[(reorder &lt;positive_integer&gt;)] | [(tjunction [on | off])] |</code> </p>
	<p><code style="font-family:Courier New">[(via_at_smd [off | on [(grid [on | off])] [(fit [on | off])]] |</code> </p>
	<p><code style="font-family:Courier New">[(width &lt;positive_dimension&gt;)]</code>,</p>
	<p>где <code style="font-family:Courier New">clearance &lt;positive_dimension&gt;</code> – задание зазора, определяемого положительным размером <code style="font-family:Courier New">&lt;positive_dimension&gt;</code>;</p>
	<p><code style="font-family:Courier New">type {<clearance_type>}</code> – задание типа зазора;</p>
	<p><code style="font-family:Courier New">junction_type</code> – задание типа контактной площадки: <code style="font-family:Courier New">term_only</code> – только выводы компонентов; <code style="font-family:Courier New">all</code> – все;</p>
	<p><code style="font-family:Courier New">limit_bends</code> – максимальное число изгибов дорожек, определяемое положительным целым числом <code style="font-family:Courier New">&lt;positive_integer&gt;</code>;</p>
	<p><code style="font-family:Courier New">limit_crossing</code> – максимально допустимое число пересекающихся дорожек, определяемое целым числом <positive_integer>;</p>
	<p><code style="font-family:Courier New">limit_vias</code> – максимально допустимое число переходных отверстий для каждого соединения, определяемое положительным целым числом <code style="font-family:Courier New">&lt;positive_integer&gt;</code>;</p>
	<p><code style="font-family:Courier New">limit_way</code> – максимальное расстояние для разводки дорожек в направлении, не предпочтительном для слоя, определяемое положительным целым числом <code style="font-family:Courier New">&lt;positive_integer&gt;</code>;</p>
	<p><code style="font-family:Courier New">max_total_vias</code> – максимальное общее число переходных отверстий, определяемое положительным целым числом <code style="font-family:Courier New">&lt;positive_integer&gt;</code>;</p>
	<p><code style="font-family:Courier New">width</code> – длина дорожки для данного правила.</p>
	<center><strong><em>Команда SELECT</em></strong></center>
	<p>Команда позволяет авроразводчику использовать конкретные слои и переходные отверстия для разводки дорожек. Она также позволяет выбрать цепь для разводки. Учтите, что названия чувствительны к регистру символов.</p>
	<p>Основной синтаксис:</p>
	<p><code style="font-family:Courier New">select[layer|via]{&lt;id&gt;}|[all[layers|vias]|comp{&lt;comp_name&gt;}|[net]{&lt;net_name&gt;}</code>,</p>
	<p>где</p>
	<p><code style="font-family:Courier New">layer</code> – выбор слоя для разводки дорожек;</p>
	<p><code style="font-family:Courier New">via</code> – выбор переходных отверстий для разводки дорожек;</p>
	<p><code style="font-family:Courier New">&lt;id&gt;</code> – идентификатор слоя/переходного отверстия: <code style="font-family:Courier New">all</code> – все слои/переходные отверстия; <code style="font-family:Courier New">layers</code> – перечисление слоев; <code style="font-family:Courier New">vias</code> – перечисление переходных отверстий.</p>
	<p><code style="font-family:Courier New">net</code> – выбор цепи для разводки дорожек: <code style="font-family:Courier New">&lt;net_name&gt;</code> – название дорожки.</p>
	<center><strong><em>Команда UNLOCK</em></strong></center>
	<p>Снимает запреты со всех существующих дорожек, устанавливаемые командой LOCK.</p>
	<p>Основной синтаксис:</p>
	<p><code style="font-family:Courier New">unlock net &lt;name&gt; | [all {layers|vias}]</code>,</p>
	<p>где <code style="font-family:Courier New">&lt;name&gt;</code> – название цепи: <code style="font-family:Courier New">all</code> – все цепи; <code style="font-family:Courier New">layers</code> – перечисление слоев, на которых расположена цепь; <code style="font-family:Courier New">vias</code> – перечисление переходных отверстий, с которыми связана цепь.</p>
	<center><strong><em>Команда UNPROTECT</em></strong></center>
	<p>Снимает защиту со всех существующих дорожек, устанавливаемую командой PROTECT, позволяя авторазводчику изменять и удалять их.</p>
	<p>Основной синтаксис: <code style="font-family:Courier New">unprotect</code></p>
	<center><strong><em>Команда UNSELECT</em></strong></center>
	<p>Запрещает авторазводчику использовать конкретные слои и переходные отверстия для разводки дорожек. Эта команда может использоваться, чтобы уменьшить число слоев для разводки по сравнению с количеством, используемым по умолчанию. Учтите, что названия чувствительны к регистру символов.</p>
	<p>Основной синтаксис:</p>
	<p><code style="font-family:Courier New">unselect [layer|net|via]{&lt;id&gt;} | [all {layers|vias}]</code></p>
	<p>где</p>
	<p><code style="font-family:Courier New">layer</code> – выбор слоя для запрета разводки дорожек;</p>
	<p><code style="font-family:Courier New">net</code> – выбор цепи для запрета разводки дорожек</p>
	<p><code style="font-family:Courier New">via</code> – выбор переходных отверстий для запрета разводки дорожек;</p>
	<p><code style="font-family:Courier New">&lt;id&gt;</code> – идентификатор слоя/переходного отверстия: <code style="font-family:Courier New">all</code> – все слои/переходные отверстия; <code style="font-family:Courier New">layers</code> – перечисление слоев; <code style="font-family:Courier New">vias</code> – перечисление переходных отверстий.</p>
	<p>Пример:</p>
	<p>Запрет разводки дорожек на слоях s1 s2</p>
	<p><code style="font-family:Courier New">unselect layer s1 s2</code></p>
	<center><strong>Советы при использовании авторазводчика</strong></center>
	<p>В общем случае авторазводка происходит, используя следующую последовательность действий:</p>
	<ul>
		<li>загружается список соединений, проводятся границы печатной платы и внутри неё помещаются все или некоторые компоненты;</li>
		<li>определяются правила проектирования и настраиваются классы цепей для определения стилей дорожек и переходных отверстий при разводке.</li>
		<li>запускается авторазводчик и полностью автоматическом (или скриптовом) режиме.</li>
		<li>пока не будет разведена вся плата, исследуются области с большим числом переходных отверстий или неразведенные участки схемы и меняется местами расположение компонентов. Чтобы удалить дорожки, размещенные авторазводчиком, можно использовать иконку <strong>Block Delete</strong>, выделив дорожки в режиме <strong><strong>Track Mode</strong></strong>.</li>
		<li>после повторного расположения компонентов, переключитесь в интерактивный режим разводки для управления режимом или повторите полностью автоматическую разводку с увеличенным числом проходов.</li>
	</ul>
	<p>Если разведены почти все дорожки (95–99%) и нужно исследовать проблемные соединения можно вызвать <strong>Connectivity Checker…</strong> из меню <strong>Tools</strong>. Двойной щелчок по нужному соединению в списке отцентрирует его и позволит исследовать проблемную область платы.</p>
	<center><strong>Односторонние платы</strong></center>
	<p>Чтобы развести одностороннюю плату необходимо настроить классы цепей, указав для всех них один слой, на котором нужно разводить плату. Это заставит ARES разводить вертикальные и горизонтальные дорожки на одной стороне платы.</p>
	<p>Число проходов авторазводчика, которое требуется при разводке односторонних плат намного больше, чем для многослойных, но при хорошем расположении компонентов, большинство плат все равно разводятся полностью.</p>
	<p>Не полностью разведенные дорожки отображаются в виде линий связей; их можно попытаться развести вручную.</p>
	<center><strong>Компоненты для поверхностного монтажа</strong></center>
	<p>Компоненты для поверхностного монтажа, особенно интегральные микросхемы, иногда представляют проблему для традиционных сеточных алгоритмов авторазводки, поскольку расстояние между выводами редко равно 25 или 50 мил. Таким образом, дорожки не могут соединяться с выводами точно по центру, поскольку точки сетки не совпадают с центрами контактных площадок.</p>
	<p>Чтобы избежать этого, необходимо всегда осуществлять одну или более проходов fanout, чтобы авторазводчику было проще осуществлять соединения во время фазы разводки.</p>
	<p>Необходимо также быть осторожным при размещении фильтрующих конденсаторов слишком близко к контактным площадкам, поскольку эти может заблокировать доступ к ним.</p>
	<center><strong>Подключение к областям металлизации</strong></center>
	<p>Важно, чтобы все области металлизации, к которым необходимо присоединить дорожки имели установленный флажок <strong>Route to this zone</strong>. Его можно установить из диалогового окна редактирования зоны (Рис. 105).</p>
	<center><img src="/images/autoroute/zone.png" alt=""></center>
	<center>Рис. 105</center>
	<p>Хотя весовой коэффициент разбиения зоны на части высокой, иногда зона разделяется во время разводки дорожкой другой цепи. Этого можно избежать, настраивая пары слоев для класса цепей или разводя плату в интерактивном режиме. Если избежать разделения не удается, области металлизации можно скорректировать после разводки или просто поместить их после разводки на требуемом участке.</p>

</div>