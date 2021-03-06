# Окно координат курсора мыши

<div style="text-align:justify;">
<p>Текущие координаты курсора мыши отображаются в правом нижнем углу экрана по умолчанию. При этом отображается не точное положение конца курсора, а положение ближайшей точки координатной сетки, к которой он привязан. Они могут выдаваться в дюймовых или метрических единицах (команда <strong>Metric</strong> из меню <strong>View</strong>) и можно настроить локальное начало координат (команда <strong>Origin</strong> из меню <strong>View</strong>). Команда <strong>X-Cursor</strong> из меню <strong>View</strong> отображает маленькое или большое перекрестие в точном положении текущих координат.</p>
<p>Основной линейной единицей измерения в ARES является 10 нм. Это позволяет создавать платы размером около 10 м с некоторым запасом. 10 нм помещаются целое число раз как в 1 мкм (микрон), так и в 0,1 мил (одна десятитысячная дюйма), поэтому их можно использовать как при дюймовом, так и метрическом представлении системы координат.</p>
<p>Углы вращения задаются с точностью 0,1 градус.</p>
<center><strong>Поля с вводом размерностей</strong></center>
<p>Множество диалоговых окон содержат поля, где нужно вводить размерности, например, при выборе размеров контактных площадок, толщин дорожек, зазоров для правил проектирования и т. д. Все эти поля обрабатываются таким образом, что в них можно использовать как дюймовые, так и метрические единицы измерения. Работа с такими полями осуществляется согласно следующим правилам:</p>
<ul>
<li>значения отображаются в единицах измерения, выбираемых с помощью эвристического алгоритма, который определяет, является ли число целой единицей в дюймовых или метрических единицах измерения. Например, 25,4 мм (введенные вручную) будут всегда отображаться как 1 дюйм при следующем вызове диалогового окна.</li>
<li>отображаемые значения всегда содержат единицу измерения. При удалении текущего значения, для следующего введенного будет использоваться та же единица измерения.</li>
<li>можно вводить новое значение, явно указывая единицы измерения для него. Поддерживаемыми единицами измерения являются:
<div style="margin-left: 100px;text-align:center;">
<table style="text-align:center; width:80%;">
<tbody>
<tr style="border: none;">
<td style="border: none;">th</td><td style="border: none;">Одна тысячная дюйма</td>
</tr>
<tr style="border: none;">
<td style="border: none;">in</td><td style="border: none;">Дюйм</td>
</tr>
<tr style="border: none;">
<td style="border: none;">um</td><td style="border: none;">Микрометр</td>
</tr>
<tr style="border: none;">
<td style="border: none;">mm</td><td style="border: none;">Миллиметр</td>
</tr>
<tr style="border: none;">
<td style="border: none;">cm</td><td style="border: none;">Сантиметр</td>
</tr>
<tr style="border: none;">
<td style="border: none;">m</td><td style="border: none;">Метр</td>
</tr>
</tbody>
</table>
</div>
</li>
<li>независимо от выбранной единицы измерения, значения всегда должны быть меньше 10 м и они сохраняются с разрешающей способностью в 10 нм.</li>
</ul>
</div>