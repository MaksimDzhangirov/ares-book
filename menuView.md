# Меню View

<div style="text-align:justify;">
<p><strong>Redraw (R)</strong> – перерисовывает содержимое основного окна редактирования и окна предварительного просмотра. Использование команды Redraw также снимет выделение со всех выделенных объектов.</p>
<p><strong>Flip (F)</strong> – Переворачивает плату, позволяя увидеть её нижний медный слой или слой пайки.</p>
<p><strong>Grid (G)</strong> – включает/выключает изображение сетки. Размер сетки обычно равен текущим настройкам шага сетки, но при масштабировании он может умножаться на коэффициент равный двум, четырем, восьми и т. д. Пороговое значение шага сетки, при котором производится умножение на коэффициент, настраивается через команду Set Grid в меню System. Размер сетки в окне предварительного просмотра равен 0,5 дюйма.</p>
<p><strong>Layers… (CTRL+L)</strong> – вызывает диалоговое окно, позволяющее настроить цвет, видимость слоев и отображение информации на экране (Рис. 22). Пользователь также может вызвать его, щелкнув левой кнопкой мыши по панели задач.</p>
<center><img src="/images/chapter3/display.png"></center>
<center>Рис. 22</center>
<p>Во вкладке <strong>Displayed Layers</strong> (Отображаемые слои) можно изменить цвет и видимость слоев с помощью флажка слева от названия слоя:</p>
<p><code style="color: #FFF; background-color: rgb(204,0,0);">Top Copper</code> – верхний медный слой печатной платы.</p>
<p><code style="color: #FFF; background-color: rgb(0,0,204);">Bottom Copper</code> – нижний медный слой печатной платы.</p>
<p><code style="color: #000; background-color: rgb(0,255,255);">Top Silk</code> – слой для нанесения шелкографии на верхней стороне платы.</p>
<p><code style="color: #000; background-color: rgb(255,0,255);">Bottom Silk</code> – слой для нанесения шелкографии на нижней стороне платы.</p>
<p><code style="color: #000; background-color: rgb(0,204,0);">Top Resist</code> – слой паяльной маски на верхней стороне платы.</p>
<p><code style="color: #000; background-color: rgb(0,204,0);">Bottom Resist</code> – слой паяльной маски на нижней стороне платы.</p>
<p><code style="color: #000; background-color: rgb(204,204,0);">Top Mask</code> – слой паяльной пасты на верхней стороне платы.</p>
<p><code style="color: #000; background-color: rgb(204,204,0);">Bottom Mask</code> – слой паяльной пасты на нижней стороне платы.</p>
<p><code style="color: #000; background-color: rgb(0,255,0);">Ratsnest</code> – слой линии связи между элементами.</p>
<p><code style="color: #000; background-color: rgb(255,255,0);">Force Vectors</code> – слой направляющих векторов; используется для оптимального размещения элементов на плате.</p>
<p><code style="color: #FFF; background-color: rgb(192,192,192);">Mech. 1 … Mech. 4</code> – механические слои для создания пазов и других нестандартных рисунков на печатной плате. Смотри также раздел «Механические операции, производимые с платой. Вырезание пазов».
</p>
<p><code style="color: #FFF; background-color: rgb(255,0,0);">Illegal</code> – слой, хранящий метки, обозначающие нарушение правил проектирования, а также проводники, принадлежащие к цепи VOID.</p>
<p><code style="color: #FFF; background-color: rgb(255,0,0);">Keepout</code> – слой, состоящий из запретных зон, на которых не могут располагаться дорожки печатной платы.</p>
<p><code style="color: #FFF; background-color: rgb(57,57,57);">Occupancy</code> – слой, определяющий область, которую занимает компонент на печатной плате.</p>
<p><code style="color: #000; background-color: rgb(255,255,0);">Edge</code> – слой, определяющий границы (длину и ширину) печатной платы.</p>
<p><code style="color: #FFF; background-color: rgb(134,134,134);">Drill Holes</code> – слой, хранящий метки, обозначающие центр и диаметр высверливаемых отверстий.</p>
<p><code style="color: #FFF; background-color: rgb(192,192,192);">Grid Lines</code> – цвет линий сетки.</p>
<p><code style="color: #FFF; background-color: rgb(204,102,51);">Inner 1 … Inner 14</code> – внутренние слои печатной платы, которые могут использоваться для прокладки электрических соединений.</p>
<p><code style="color: #FFF; background-color: rgb(204,0,204);">Thru Pads</code> – цвет сквозных контактных площадок.</p>
<p><code style="color: #FFF; background-color: rgb(128,128,0);">Thru Vias</code> – цвет сквозных переходных отверстий.</p>
<p><code style="color: #FFF; background-color: rgb(51,153,153);">Buried Vias</code> – цвет переходных отверстий во внутренних слоях платы.</p>
<p><code style="color: #000; background-color: rgb(153,255,255);">Pin Numbers</code> – цвет номеров контактных площадок.</p>
<p><code style="color: #FFF; background-color: rgb(34,34,34);">Empty Zones</code> – цвет не залитых областей металлизации.</p>
<p><code style="color: #FFF; background-color: rgb(0,204,0);">Drag Cursor</code> – цвет объектов во время перетаскивания.</p>
<p>Все изменения происходят в реальном времени. Кнопка All делает все слои видимыми, а кнопка None делает невидимыми все слои, кроме Force Vectors и Drill Holes. Раздел Resist/Solder Paste Display (Отображение паяльной маски/пасты) изображает все паяльную массу/пасту на плате при установленном флажке. Эти флажки доступны только в режиме аппаратного ускорения OpenGL.</p>
<p>Вкладка Thru-View Settings аналогична диалоговому окну Set Display Options в меню System.</p>
<p>Metric (M) – осуществляет выбор единицы измерения. ARES может работать с дюймовыми (th – мил, 1/1000 дюйма) и метрическими единицами (мм) измерения длин. Выбранная в данный момент единица измерения отображается в окне координат курсора мыши (Рис. 23).</p>
<center><table style="border-width: 0px; text-align:center;">
<tbody>
<tr style="border-width: 0px; text-align:center;">
<td style="border-width: 0px; text-align:center;"><img src="/images/chapter3/inch.png"></td>
<td style="border-width: 0px; text-align:center;"><img src="/images/chapter3/meter.png"></td>
</tr>
<tr style="border-width: 0px; text-align:center;">
<td style="border-width: 0px; background-color:#FFF;">Дюймовые единицы измерения</td>
<td style="border-width: 0px; background-color:#FFF;">Метрические единицы измерения</td>
</tr>
</tbody>
</table></center>
<center>Рис. 23</center>
<p>Origin (O) – включает/выключает локальное начало координат. Задача команды заключается в присвоении текущим координатам курсора мыши локального начала координат.</p>
<p>Когда выбрано локальное начало координат, координаты курсора мыши изменяют цвет с черного на розовый (Рис. 24).</p>
<center><table style="border-width: 0px; text-align:center;">
<tbody>
<tr style="border-width: 0px; text-align:center;">
<td style="border-width: 0px; text-align:center;"><img src="/images/chapter3/global.png"></td>
<td style="border-width: 0px; text-align:center;"><img src="/images/chapter3/local.png"></td>
</tr>
<tr style="border-width: 0px; text-align:center;">
<td style="border-width: 0px; background-color:#FFF;">Координаты отображаются в глобальной системе</td>
<td style="border-width: 0px; background-color:#FFF;">Координаты отображаются в локальной системе</td>
</tr>
</tbody>
</table></center>
<center>Рис. 24</center>
<p>Отметить использование локального начала координат можно повторным вызовом команды <strong>Origin</strong>.</p>
<p><strong>Z-Theta (Z)</strong> – включает/выключает отображение координат в полярной системе. При этом радиус от центра координат отображается красным цветом, а угол, отсчитываемый от положительного направления оси X (параллельна горизонтали и направлена вправо) – синим. Отметить использование полярной системы координат можно повторным вызовом команды <strong>Z-Theta</strong>.</p>
<p><strong>X cursor (X)</strong> – включает маленький или большой крест, кроме курсора мыши, показывающий в какой точке в данный момент установлен курсор. Эту функцию полезно использовать, когда необходимо точно знать текущее положение курсора.</p>
<p><strong>Goto-XY… (CTRL+G)</strong> – перемещает курсор мыши в нужное положение на экране (Рис. 25).</p>
<center><img src="/images/chapter3/gotoxy.png"></center>
<center>Рис. 25</center>
<p>Поле <strong>X Coordinate</strong> используется для ввода координаты X, куда необходимо переместить курсор. Поле <strong>Y Coordinate</strong> используется для ввода координаты Y, куда необходимо переместить курсор. В выпадающем списке <strong>Relative to</strong> можно выбрать относительно чего будут вычисляться координаты X и Y:</p>
<ul>
  <li><strong>Current Origin</strong> (выбрано по умолчанию) – относительно текущего начала координат. Им может быть локальное, измененное глобальное или первоначальное (используемое по умолчанию) начало координат.</li>
  <li><strong>Output Origin</strong> – относительно глобального начала координат. Им может быть измененное глобальное или первоначальное (используемое по умолчанию) начало координат.</li>
  <li><strong>Database Origin</strong> – относительно первоначального глобального начала координат.</li>
</ul>
<p>Диапазон вводимых значений изменяется от –9999999 до 99999999, причем при вводе значения выходящего за пределы рабочей области (синий прямоугольник в основном окне редактирования или окне предварительного просмотра) на панели задач выводится предупреждающее сообщение о выходе координат за допустимые пределы и перемещения курсора не происходит.</p>
<p><strong>Goto Component… (CTRL+C)</strong> – используется для выделения компонента и масштабирования изображения так, чтобы выделенный компонент был по центру (Рис. 26). В единственном поле <strong>Component</strong> необходимо ввести название компонента.</p>
<center><img src="/images/chapter3/gotocomp.png"></center>
<center>Рис. 26</center>
<p>Если компонента с введенным названием нет на печатной плате, то на панели задач выводится предупреждающее сообщение <strong>Component ‘&lt;название компонента&gt;’ not found!</strong> (Компонент «название компонента» не найден).</p>
<p><strong>Goto Pin… (CTRL+P)</strong> – используется для выделения вывода компонента и масштабирования изображения так, чтобы выделенный вывод был по центру (Рис. 27). В единственном поле Component ID-Pin необходимо ввести название компонента и через дефис требуемый вывод компонента, например, U1-1.</p>
<center><img src="/images/chapter3/gotopin.png"></center>
<center>Рис. 27</center>
<p>Если вывода компонента с введенным названием нет на печатной плате, то на панели задач выводится предупреждающее сообщение <strong>Pin ‘&lt;название компонента и вывода&gt;’ not found!</strong> (Вывод «название компонента и вывода» не найден).</p>
<p><strong>Snap XX</strong> (F2…F4 и Ctrl+F1) – переключает шаг сетки и привязку к ней, где XX – значения в милах (th) или миллиметрах (мм) (Рис. 28). Самый мелкий шаг 1th (0,001 дюйма) или 0,1 мм вызывается через Ctrl+F1. Шаг сетки и привязки можно настроить через команду <strong>Set Grids</strong> в меню <strong>System</strong>.</p>
<p>Обычно печатные платы разводятся с шагом сетки 50 или 25 мил.</p>
<p>Шаги сетки вычисляются от текущего начала координат, которое устанавливается командой <strong>Origin</strong>. Это позволяет измерить расстояние между контактными площадками при создании нового компонента, поскольку можно установить начало координат в центре первой контактной площадки, выставить шаг сетки равный расстоянию между площадками, и затем перемещать курсор в точки новых положений контактных площадок.</p>
<center><table style="border-width: 0px; text-align:center;">
<tbody>
<tr style="border-width: 0px; text-align:center;">
<td style="border-width: 0px; text-align:center;"><img src="/images/chapter3/stepi.png"></td>
<td style="border-width: 0px; text-align:center;"><img src="/images/chapter3/stepm.png"></td>
</tr>
<tr style="border-width: 0px; text-align:center;">
<td style="border-width: 0px; background-color:#FFF;">Шаг сетки в дюймовых единицах измерения</td>
<td style="border-width: 0px; background-color:#FFF;">Шаг сетки в метрических единицах измерения</td>
</tr>
</tbody>
</table></center>
<center>Рис. 28</center>
<p><strong>Pan (F5)</strong> – центрирует изображение на экране по указателю курсора (по щелчку левой кнопкой мыши).</p>
<p><strong>Zoom In (F6)</strong> – увеличить масштаб.</p>
<p><strong>Zoom Out (F7)</strong> – уменьшить масштаб.</p>
<p><strong>Zoom All (F8)</strong> – разместить на экране рабочую область (синий прямоугольник) целиком.</p>
<p><strong>Zoom to Area</strong> – позволяет четко разместить в пределах основного окна редактирования выделенный перед этим участок экрана.</p>
<p>Команда <strong>Toolbars…</strong> позволяет включить/выключить отображение верхних панелей инструментов <strong>File</strong>, <strong>View</strong>, <strong>Edit</strong>, <strong>Layout</strong>. Смотри также раздел «Верхние (подключаемые) панели инструментов». Изменить отображаемый в них набор кнопок-инструментов невозможно.</p>
</p>
</div>
