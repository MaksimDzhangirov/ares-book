# Верхние (подключаемые) панели инструментов

<div style="text-align: justify;">
	<p>Под главным верхним меню находится полоса <strong>Toolbars (Панели инструментов)</strong>. Она условно разделена на четыре секции (Рис. 76), которые можно включать и выключать через команду <strong>Toolbars…</strong> из главного меню <strong>View</strong>. По умолчанию все они включены (в диалоговом окне Show/Hide Toolbars… отмечены галочками). Термин «верхние» относителен, поскольку их можно перетаскивать размещать у любой из четырех сторон приложения ARES. Если в случае уменьшения размера окна программы панели инструментов не помещаются в одной строке, они автоматически выстраиваются в две строки. Так же ведут себя и меню расположенные вертикально слева. Если необходимо скрыть один из верхних панелей инструментов, можно снять для него соответствующую галочку в <strong>Show/Hide Toolbars…</strong>. Все иконки панели инструментов при наведении на них курсора мышки имеют всплывающие текстовые подсказки, однако они не всегда совпадают с аналогичным в основном меню. Панели инструментов предоставляют альтернативный доступ к командам меню и сгруппированы по назначению следующим образом:</p>
	<div>
		<table style="text-align: center;">
			<tbody>
				<tr>
					<th style="text-align: center;">Назначение</th> <th style="text-align: center;">Панель инструментов</th>
				</tr>
				<tr>
					<td>Команды файл/печать (<strong>File</strong>)</td> <td><img src="/images/topmenu/file.png" alt=""></td>
				</tr>
				<tr>
					<td>Команды вид/масштаб (<strong>View</strong>)</td> <td><img src="/images/topmenu/view.png" alt=""></td>
				</tr>				
				<tr>
					<td>Команды редактирования (<strong>Edit</strong>)</td> <td><img src="/images/topmenu/edit.png" alt=""></td>
				</tr>
				<tr>
					<td>Команды разводки печатной платы (<strong>Layout</strong>)</td> <td><img src="/images/topmenu/layout.png" alt=""></td>
				</tr>
			</tbody>
		</table>		
	</div>
	<center>Рис. 76</center>
	<center>Панель инструментов <strong>File</strong> (смотри также меню <strong>File</strong> и <strong>Output</strong>):</center>
	<div>
		<table>
			<tbody>
				<tr>
					<td style="text-align: center;"><img src="/images/topmenu/newfile.png" alt=""></td> <td><strong>New Layout</strong> – создает новый проект. Если проект был изменен, но не сохранен, перед созданием нового проекта открывается диалоговое окно позволяющее сохранить текущий проект (<em>пустой белый лист</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/file.png'); background-position: -28px -4px;"></div></td> <td><strong>Open Layout</strong> – открывает файлы программы ARES. Если проект был изменен, но не сохранен, перед открытием другого проекта открывается диалоговое окно позволяющее сохранить текущий проект (<em>раскрывающаяся папка</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/file.png'); background-position: -50px -4px;"></div> </td> <td><strong>Save Layout</strong> – записывает текущий редактируемый проект на диск (<em>дискета</em>)</td>					
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/file.png'); background-position: -78px -4px;"></div> и <div style="width: 23px; height: 23px; background-image:url('images/topmenu/file.png'); background-position: -100px -4px;"></div></td> <td><strong>Import ARES Region File</strong> и <strong>Export ARES Region File</strong> – вставляет файл участка печатной платы с расширением <strong>*.RGN</strong> в текущий проект и сохраняет выделенный участок печатной платы в файл с расширением <strong>*.RGN</strong> (<em>дискета, указывающая на файл и файл, указывающий на дискету</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/file.png'); background-position: -128px -4px;"></div></td> <td><strong>Print Layout</strong> – осуществляет печать разводки проекта печатной платы с множеством предварительных настроек (<em>принтер</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('images/topmenu/file.png'); background-position: -148px -4px;"></div></td> <td><strong>Set Output Area</strong> – позволяет выбрать область для печати (<em>лист с выбранной частью</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/file.png'); background-position: -178px -4px;"></div></td> <td><strong>Generate Gerber/Excellon Files</strong> – открывает диалоговое окно, позволяющее сохранить печатную плату в формате <strong>Gerber</strong> и <strong>Excellon</strong> аналогично команде <strong>Gerber/Excellon Output...</strong> (<em>участок платы с дорожками</em>)</td>
				</tr>					
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/file.png'); background-position: 26px -4px;"></div></td> <td><strong>Gerber Viewer</strong> – запускает просмотрщик, позволяющий загрузить и отобразить файлы, созданные командой <strong>Gerber/Excellon Output...</strong> (<em>участок платы с дорожками под лупой</em>)</td>
				</tr>	
			</tbody>
		</table>
	</div>
	<center>Панель инструментов <strong>View</strong> (слева – направо) (смотри также меню <strong>View</strong>):</center>
	<div>
		<table>
			<tbody>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: -10px -2px;"></div></td> <td><strong>Redraw Display</strong> – обновляет окно программы (<em>круговые зеленые стрелки</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: -31px -2px;"></div></td> <td><strong>Toggle Board Flip</strong> – переворачивает плату, позволяя увидеть её нижний медный слой (<em>два прямоугольных треугольника с буквой F посередине</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: -52px -2px;"></div></td> <td><strong>Toggle Grid (G)</strong> – включает/выключает отображение сетки (<em>точечная сетка</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: -73px -2px;"></div> </td> <td><strong>Edit Layer Colours/Visibility</strong> – вызывает диалоговое окно, позволяющее настроить цвет, видимость слоев и отображение информации на экране (<em>три прямоугольника, расположенные по убыванию</em>)</td>					
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: -103px -2px;"></div></td> <td><strong>Toggle Metric/Imperial</strong> – позволяет выбрать дюймовую или метрическую систему единиц для системы координат (<em>маленькая английская буква M</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: -124px -2px;"></div></td> <td><strong>Toggle False Origin</strong> – включает/выключает локальное начало координат. Используется при создании корпусов (<em>прицел</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: -145px -2px;"></div></td> <td><strong>Toggle Polar Coordinates</strong> – включает/выключает отображение координат в полярной системе (<em>система координат с буквой Z</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: -173px -2px;"></div></td> <td><strong>Center At Cursor</strong> – центрирует изображение на экране по указателю курсора (щелчок левой кнопкой мышки) (<em>четыре голубые растягивающиеся стрелки</em>)</td>
				</tr>					
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: 90px -2px;"></div></td> <td><strong>Zoom In (F6)</strong> – увеличить масштаб (<em>лупа с плюсом</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: 68px -2px;"></div></td> <td><strong>Zoom Out (F7)</strong> – уменьшить масштаб (<em>лупа с минусом</em>)</td>
				</tr>					
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: 48px -2px;"></div></td> <td><strong>Zoom To View Entire Board (F8)</strong> – изменить масштаб так, чтобы было видно всю печатную плату (<em>лупа с мелким квадратом</em>)</td>
				</tr>				
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/view.png'); background-position: 28px -2px;"></div></td> <td><strong>Zoom To Area</strong> – разместить в основном окне редактирования выделенную область (щелчок левой кнопки мыши первая точка, повторный вторая по диагонали выделяемой области)  (<em>лупа с белым прямоугольником</em>)</td>
				</tr>				
			</tbody>
		</table>
	</div>
		<center><strong>Панель инструментов Edit</strong> (слева – направо) (смотри также меню <strong>Edit</strong>):</center>
	<div>
		<table>
			<tbody>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/edit.png'); background-position: -7px -2px;"></div></td> <td><strong>Undo Changes</strong> – отмена последнего действия (<em>голубая стрелка против часовой</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/edit.png'); background-position: -29px -2px;"></div></td> <td><strong>Redo Changes</strong> – возврат последнего отмененного действия. Активна только после <strong>Undo</strong> (<em>голубая стрелка по часовой</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/edit.png'); background-position: -58px -2px;"></div></td> <td><strong>Block Copy</strong> – копировать блок (<em>два зеленых прямоугольника с вертикальной красной стрелкой вниз</em>). Смотри раздел «Команды группового редактирования».</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/edit.png'); background-position: -79px -2px;"></div> </td> <td><strong>Block Move</strong> – переместить блок (<em>кнопка аналогична предыдущей, только верхний прямоугольник прозрачный</em>). Смотри раздел «Команды группового редактирования».</td>					
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/edit.png'); background-position: -101px -2px;"></div></td> <td><strong>Block Rotate</strong> – позволяет через появившееся диалоговое окно повернуть выделенный блок (элементы 2D графики, дорожки и/или корпуса) на заданный угол или отразить его (флажок <strong>Mirror</strong>) по оси <strong>Х</strong> или <strong>Y</strong> (<em>зеленый прямоугольник с круговой стрелкой против часовой</em>). Смотри раздел «Команды группового редактирования».</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/edit.png'); background-position: -122px -2px;"></div></td> <td><strong>Block Delete</strong> – удаляет выделенный блок/элемент (<em>зеленый прямоугольник с крестиком</em>). Смотри раздел «Команды группового редактирования».</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/edit.png'); background-position: -150px -2px;"></div></td> <td><strong>Pick Parts From libraries</strong> – выбрать объект из библиотеки ARES (<em>лупа с мнемоникой ОУ – треугольник внутри</em>). В отличие от аналогичной по действию кнопки вверху селектора объектов – <strong>P</strong>, всегда переносит в библиотеку корпусов. Кнопка <strong>P</strong> – изменяет свое действие в зависимости от выбранной иконки в левом меню.</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/edit.png'); background-position: -171px -2px;"></div></td> <td><strong>Make Package</strong> – создание нового корпуса из выделенных элементов (<em>мнемоника корпуса с символом плюс</em>)</td>
				</tr>					
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/edit.png'); background-position: 26px -2px;"></div></td> <td><strong>Decompose</strong> – разбить компонент на составляющие (<em>молоток</em>). Противоположен по действию <strong>Make Package</strong>.</td>
				</tr>				
			</tbody>
		</table>
	</div>
	<center><strong>Панель инструментов Layout</strong> (слева – направо) (смотри также меню <strong>Tools</strong>):</center>
	<div>
		<table>
			<tbody>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/layout.png'); background-position: -11px -2px;"></div></td> <td><strong>Toggle Trace Angle Lock</strong> – включить/выключить запрет изменения угла разводки дорожки (<em>две перпендикулярные прямые с дугой между ними внутри которой находится замок</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/layout.png'); background-position: -32px -2px;"></div></td> <td><strong>Toggle Auto Trace Style/Selection</strong> – включить/выключить автоматический выбор соответствующих стилей дорожек и переходных отверстий (<em>выделенная штрихованным прямоугольником дорожка с курсором</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/layout.png'); background-position: -53px -2px;"></div></td> <td><strong>Toggle Auto Track Necking</strong> – включить/выключить автоматическое уменьшение размера дорожки (<em>дорожка, суженная с обеих сторон</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/layout.png'); background-position: -82px -2px;"></div> </td> <td><strong>Search Tag Components (New)</strong> – поиск и выделение компонентов (<em>бинокль</em>)</td>					
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/layout.png'); background-position: -101px -2px;"></div></td> <td><strong>Automatic Name Generator</strong> – автоматическое изменение названия и нумеровка компонентов или контактных площадок на плате (<em>вертикальное перечисление компонентов U1, U2, U3</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/layout.png'); background-position: -132px -2px;"></div></td> <td><strong>Auto-router</strong> – запускает авторазводчик (<em>пересекающиеся разноцветные дорожки</em>)</td>
				</tr>
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/layout.png'); background-position: -162px -2px;"></div></td> <td><strong>Connectivity Rules Checker</strong> – запускает проверку правил соединений и выдает диалоговое окно <strong>Connectivity Errors</strong>, если существуют ошибки соединений (<em>линии, показывающие расстояние между элементами</em>)</td>
				</tr>			
				<tr>
					<td style="text-align: center;"><div style="width: 23px; height: 23px; background-image:url('/images/topmenu/layout.png'); background-position: 33px -2px;"></div></td> <td><strong>Design Rule Manager</strong> – настройка встроенной системы проверки правил проектирования (<em>прямоугольная, треугольная линейка и карандаш</em>)</td>
				</tr>				
			</tbody>
		</table>
	</div>
</div>