# Фильтр для выбора объектов

<div style="text-align:justify;"> 
	<p>ARES использует фильтр для выбора объектов в нижней левой части окна программы для определения какие объекты доступны для выбора в любой заданный момент времени (Рис. 90).</p>
	<center><img src="/images/filter/filter.png" alt=""></center>
	<center>Рис. 90</center>
	<p>Самая левая иконка – <strong>Layer Filter Mode</strong> (Режим фильтрации слоев) – определяет независимо от слоя, выбранного в селекторе слоев:</p>
	<ul>
		<li>в положении <img src="/images/filter/layer1.png" alt=""> команда выбора объектов применяется ко всем слоям на печатной плате.</li>
		<li>в положении <img src="/images/filter/layer2.png" alt=""> команда выбора объектов применяется только к слою, определенному в селекторе слоев.</li>
	</ul>
	<p>Другие иконки представляют различные типы объектов (компоненты  <img src="/images/filter/comp.png" alt="">, двумерную графику <img src="/images/filter/gra.png" alt="">, контактные площадки <img src="/images/filter/pad.png" alt="">, дорожки  <img src="/images/filter/track.png" alt="">, переходные отверстия <img src="/images/filter/via.png" alt="">, области металлизации <img src="/images/filter/zones.png" alt="">, линии связи <img src="/images/filter/rat.png" alt="">) и определяют когда эти объекты можно выбрать (иконка утоплена – объект можно выбрать, иконка не утоплена – объект нельзя выбрать).</p>
	<p>Если пользователь переключается между различными режимами работы (например, от режима выбора элемента (<strong>Selection Mode</strong>) в режим выбора дорожек <strong>Track mode</strong> или компонентов <strong>Сomponent mode</strong>), то увидит как переключаются объекты, которые можно выбрать, в соответствии с режимом, в котором он находится (Рис. 91). Разработчик может изменить настройки выбора объектов в любой момент, включив или выключив выбор объектов определенного типа. Также можно изменить настройки по умолчанию через меню System команду <strong>Set Selection Filter</strong>.</p>
	<div>
		<table>
			<tbody>
				<tr>
					<td style="text-align:center;"><img src="/images/filter/trackmode.png" alt=""></td> <td style="text-align:center;"><img src="/images/filter/componentmode.png" alt=""></td>
				</tr>
				<tr>
					<td style="text-align:center;">Режим <strong>Track Mode</strong> – иконки <img src="/images/filter/comp1.png" alt="">, <img src="/images/filter/gra1.png" alt="">, <img src="/images/filter/zone1.png" alt=""> выбрать нельзя</td> <td style="text-align:center;">Режим <strong>Сomponent mode</strong> – иконки  <img src="/images/filter/track1.png" alt="">, <img src="/images/filter/via1.png" alt="">, <img src="/images/filter/zone2.png" alt=""> выбрать нельзя</td>
				</tr>
			</tbody>
		</table> 
	</div>
	<center>Рис. 91</center>
	<p>Иконка <strong>Track Selection Mode</strong> снимает (<img src="/images/filter/tr1.png" alt="">) или устанавливает (<img src="/images/filter/tr2.png" alt="">) выделение с дорожек, которые только частично входят в область выделения.</p>
	<p>Учтите, что фильтр для выбора объектов контролирует какие объекты доступны для выбора в любой заданный момент времени. Если нельзя выбрать какой-либо элемент, проверьте доступен ли выбор данного объекта для того режима, в котором сейчас находится программа или просто переключитесь в Selection Mode, в котором можно выбрать все объекты.</p>
	<p>В качестве примера удалим все дорожки на верхнем медном слое платы. Перейдите в режим выбора элементов (<strong>Selection Mode</strong>) и выделите всю плату.</p>
	<p>Затем с помощью фильтра для выбора объектов снимите выбор с тех объектов, которые не хотите удалять (сделайте их иконки не утопленными), а именно со всего кроме дорожек и переходных отверстий. Выделенные объекты будут автоматически обновляться, таким образом, становится сразу понятно, что выбрано в данный момент.</p>
	<p>Теперь измените слой на <code style="color: #FFF; background-color: rgb(0,0,204);">Top Copper</code> в селекторе объектов, а <strong>Layer Filter Mode</strong> – в режим, чтобы фильтр для выбора объектов применялся только к текущему слою.</p>
	<p>Теперь можно просто нажать клавишу <strong>Delete</strong> на клавиатуре или правой кнопкой мыши внутри выделения и выбрать команду <strong>Block Delete</strong> (Удаление блока), чтобы удалить все дорожки на верхнем медном слое.</p>

</div>