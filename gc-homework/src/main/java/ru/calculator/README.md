<style>
   .text {
    text-align:  center;
   }
  </style>
<h1 class="code-line" data-line-start=0 data-line-end=1 ><a id="__0"></a>Домашняя работа:</h1>
<h2 class="code-line" data-line-start=1 data-line-end=2 ><a id="____1"></a>Определение нужного размера хипа</h2>
<br>
<nav class="toc">
  <h2>Содержание:</h2>
  <ul>
    <li><a href="#Определение оптимального размера хипа">Определение оптимального размера хипа</a>
    <li><a href="#Ответ1">Ответ</a>
    <li><a href="#Оптимизация работы приложения">Оптимизация работы приложения</a>
    <li><a href="#Ответ2">Ответ</a>
  </ul>
</nav>
<hr>
<p class="has-line-data" data-line-start="3" data-line-end="4">Стандартные настройки | spend msec:15174, sec:15</p>
<hr>
<br>
<h3 class="has-line-data" data-line-start="8" data-line-end="11" id="Определение оптимального размера хипа">Задача1:</h3>
<p> <b>Определите оптимальный размер хипа</b>, т.е. размер, превышение которого,<br>
не приводит к сокращению времени выполнения приложения.</p>
<h3 class = "text">            G1
</h3>
<hr>
<p class="has-line-data" data-line-start="15" data-line-end="18">-Xms256m     |<br>
-Xmx256m     |<br>
-XX:+UseG1GC | java.lang.OutOfMemoryError</p>
<hr>
<p class="has-line-data" data-line-start="19" data-line-end="21">-Xms512m     |<br>
-Xmx512m     | spend msec:15616, sec:15</p>
<hr>
<p class="has-line-data" data-line-start="22" data-line-end="24">-Xms1024m    |<br>
-Xmx1024m    | spend msec:14006, sec:14</p>
<hr>
<p class="has-line-data" data-line-start="25" data-line-end="27">-Xms2048m    |<br>
-Xmx2048m    | spend msec:14266, sec:14</p>
<hr>
<pre><code>Разный размер хипа на старте и на финише
</code></pre>
<hr>
<p class="has-line-data" data-line-start="30" data-line-end="32">-Xms256m     |<br>
-Xmx512m     | spend msec:16792, sec:16</p>
<hr>
<p class="has-line-data" data-line-start="33" data-line-end="35">-Xms256m     |<br>
-Xmx1024m    | spend msec:15782, sec:15</p>
<hr>
<p class="has-line-data" data-line-start="36" data-line-end="38">-Xms256m     |<br>
-Xmx2048m    | spend msec:15454, sec:15</p>
<hr>
<h3 class = "text">     Shenandoah
</h3>
<hr>
<p class="has-line-data" data-line-start="44" data-line-end="47">-Xms256m             |<br>
-Xmx256m             |<br>
-XX:+UseShenandoahGC | java.lang.OutOfMemoryError</p>
<hr>
<p class="has-line-data" data-line-start="48" data-line-end="50">-Xms512m     |<br>
-Xmx512m     | spend msec:42245, sec:42</p>
<hr>
<p class="has-line-data" data-line-start="51" data-line-end="53">-Xms1024m    |<br>
-Xmx1024m    | spend msec:12803, sec:12</p>
<hr>
<p class="has-line-data" data-line-start="54" data-line-end="56">-Xms2048m    |<br>
-Xmx2048m    | spend msec:11599, sec:11</p>
<hr>
<pre><code>Разный размер хипа на старте и на финише
</code></pre>
<hr>
<p class="has-line-data" data-line-start="59" data-line-end="61">-Xms256m     |<br>
-Xmx512m     | spend msec:40166, sec:40</p>
<hr>
<p class="has-line-data" data-line-start="62" data-line-end="64">-Xms256m     |<br>
-Xmx1024m    | spend msec:11819, sec:11</p>
<hr>
<p class="has-line-data" data-line-start="65" data-line-end="67">-Xms256m     |<br>
-Xmx2048m    | spend msec:9368, sec:9</p>
<hr>
<h3 class = "text">    Serial Collector
</h3>
<hr>
<p class="has-line-data" data-line-start="73" data-line-end="76">-Xms256m         |<br>
-Xmx256m         |<br>
-XX:+UseSerialGC | java.lang.OutOfMemoryError</p>
<hr>
<p class="has-line-data" data-line-start="77" data-line-end="79">-Xms512m     |<br>
-Xmx512m     | spend msec:18491, sec:18</p>
<hr>
<p class="has-line-data" data-line-start="80" data-line-end="82">-Xms1024m    |<br>
-Xmx1024m    | spend msec:13964, sec:13</p>
<hr>
<p class="has-line-data" data-line-start="83" data-line-end="85">-Xms2048m    |<br>
-Xmx2048m    | spend msec:11252, sec:11</p>
<hr>
<pre><code>Разный размер хипа на старте и на финише
</code></pre>
<hr>
<p class="has-line-data" data-line-start="88" data-line-end="90">-Xms256m     |<br>
-Xmx512m     | spend msec:18446, sec:18</p>
<hr>
<p class="has-line-data" data-line-start="91" data-line-end="93">-Xms256m     |<br>
-Xmx1024m    | spend msec:18695, sec:18</p>
<hr>
<p class="has-line-data" data-line-start="94" data-line-end="96">-Xms256m     |<br>
-Xmx2048m    | spend msec:17930, sec:17</p>
<hr>
<h3 class = "text">    Parallel Collector
</h3>
<hr>
<p class="has-line-data" data-line-start="102" data-line-end="105">-Xms256m           |<br>
-Xmx256m           |<br>
-XX:+UseParallelGC | java.lang.OutOfMemoryError</p>
<hr>
<p class="has-line-data" data-line-start="106" data-line-end="108">-Xms512m     |<br>
-Xmx512m     | spend msec:40448, sec:40</p>
<hr>
<p class="has-line-data" data-line-start="109" data-line-end="111">-Xms1024m    |<br>
-Xmx1024m    | spend msec:30299, sec:30</p>
<hr>
<p class="has-line-data" data-line-start="112" data-line-end="114">-Xms2048m    |<br>
-Xmx2048m    | spend msec:21789, sec:21</p>
<hr>
<pre><code>Разный размер хипа на старте и на финише
</code></pre>
<hr>
<p class="has-line-data" data-line-start="117" data-line-end="119">-Xms256m     |<br>
-Xmx512m     | spend msec:41651, sec:41</p>
<hr>
<p class="has-line-data" data-line-start="120" data-line-end="122">-Xms256m     |<br>
-Xmx1024m    | spend msec:30926, sec:30</p>
<hr>
<p class="has-line-data" data-line-start="123" data-line-end="125">-Xms256m     |<br>
-Xmx2048m    | spend msec:26707, sec:26</p>
<hr>
<h3 class = "text">       CMS
</h3>
<hr>
<p class="has-line-data" data-line-start="130" data-line-end="133">Unrecognized VM option ‘UseConcMarkSweepGC’<br>
Error: Could not create the Java Virtual Machine.<br>
Error: A fatal exception has occurred. Program will exit.</p>
<hr>
<h3 class = "text">       Z
</h3>
<hr>
<p class="has-line-data" data-line-start="139" data-line-end="142">-Xms256m    |<br>
-Xmx256m    |<br>
-XX:+UseZGC | java.lang.OutOfMemoryError</p>
<hr>
<p class="has-line-data" data-line-start="143" data-line-end="145">-Xms512m     |<br>
-Xmx512m     | spend msec:24157, sec:24</p>
<hr>
<p class="has-line-data" data-line-start="146" data-line-end="148">-Xms1024m    |<br>
-Xmx1024m    | spend msec:10111, sec:10</p>
<hr>
<p class="has-line-data" data-line-start="149" data-line-end="151">-Xms2048m    |<br>
-Xmx2048m    | spend msec:8354, sec:8</p>
<hr>
<pre><code>Разный размер хипа на старте и на финише
</code></pre>
<hr>
<p class="has-line-data" data-line-start="154" data-line-end="156">-Xms256m     |<br>
-Xmx512m     | spend msec:25886, sec:25</p>
<hr>
<p class="has-line-data" data-line-start="157" data-line-end="159">-Xms256m     |<br>
-Xmx1024m    | spend msec:9095, sec:9</p>
<hr>
<p class="has-line-data" data-line-start="160" data-line-end="162">-Xms256m     |<br>
-Xmx2048m    | spend msec:8250, sec:8</p>
<hr>
<h4 class="has-line-data" data-line-start="165" data-line-end="168" id="Ответ1">Ответ:</h4>
<p>Исходя из произведенных измерений можно сделать вывод, что оптимальный размер хипа, для исходного кода,
превышение которого, не приводит к сокращению времени выполнения приложения, это 1024 Мб</p>
<hr>
<br><br>
<h3 class="has-line-data" data-line-start="172" data-line-end="177" id="Оптимизация работы приложения">Задача2:</h3>
<p><b>Оптимизируйте работу приложения.</b><br>
Т.е. не меняя логики работы (но изменяя код), сделайте так, чтобы приложение работало
быстро с минимальным хипом. Повторите измерения времени выполнения программы<br>
для тех же значений размера хипа.</p>
<h3 class = "text">       G1
</h3>
<hr>
<p class="has-line-data" data-line-start="180" data-line-end="183">-Xms256m     |<br>
-Xmx256m     |<br>
-XX:+UseG1GC | spend msec:3401, sec:3</p>
<hr>
<p class="has-line-data" data-line-start="184" data-line-end="186">-Xms512m     |<br>
-Xmx512m     | spend msec:2864, sec:2</p>
<hr>
<p class="has-line-data" data-line-start="187" data-line-end="189">-Xms1024m    |<br>
-Xmx1024m    | spend msec:2508, sec:2</p>
<hr>
<p class="has-line-data" data-line-start="190" data-line-end="192">-Xms2048m    |<br>
-Xmx2048m    | spend msec:2412, sec:2</p>
<hr>
<h3 class = "text">   Shenandoah
</h3>
<hr>
<p class="has-line-data" data-line-start="197" data-line-end="200">-Xms256m             |<br>
-Xmx256m             |<br>
-XX:+UseShenandoahGC | spend msec:2774, sec:2</p>
<hr>
<p class="has-line-data" data-line-start="201" data-line-end="203">-Xms512m     |<br>
-Xmx512m     | spend msec:2185, sec:2</p>
<hr>
<p class="has-line-data" data-line-start="204" data-line-end="206">-Xms1024m    |<br>
-Xmx1024m    | spend msec:2003, sec:2</p>
<hr>
<p class="has-line-data" data-line-start="207" data-line-end="209">-Xms2048m    |<br>
-Xmx2048m    | spend msec:1954, sec:1</p>
<hr>
<h3 class = "text">    Serial Collector
</h3>
<hr>
<p class="has-line-data" data-line-start="214" data-line-end="217">-Xms256m         |<br>
-Xmx256m         |<br>
-XX:+UseSerialGC | spend msec:4856, sec:4</p>
<hr>
<p class="has-line-data" data-line-start="218" data-line-end="220">-Xms512m     |<br>
-Xmx512m     | spend msec:3198, sec:3</p>
<hr>
<p class="has-line-data" data-line-start="221" data-line-end="223">-Xms1024m    |<br>
-Xmx1024m    | spend msec:2255, sec:2</p>
<hr>
<p class="has-line-data" data-line-start="224" data-line-end="226">-Xms2048m    |<br>
-Xmx2048m    | spend msec:2291, sec:2</p>
<hr>
<h3 class = "text">    Parallel Collector
</h3>
<hr>
<p class="has-line-data" data-line-start="231" data-line-end="234">-Xms256m           |<br>
-Xmx256m           |<br>
-XX:+UseParallelGC | spend msec:16300, sec:16</p>
<hr>
<p class="has-line-data" data-line-start="235" data-line-end="237">-Xms512m     |<br>
-Xmx512m     | spend msec:7806, sec:7</p>
<hr>
<p class="has-line-data" data-line-start="238" data-line-end="240">-Xms1024m    |<br>
-Xmx1024m    | spend msec:2374, sec:2</p>
<hr>
<p class="has-line-data" data-line-start="241" data-line-end="243">-Xms2048m    |<br>
-Xmx2048m    | spend msec:2138, sec:2</p>
<hr>
<h3 class = "text">       Z
</h3>
<hr>
<p class="has-line-data" data-line-start="248" data-line-end="251">-Xms256m    |<br>
-Xmx256m    |<br>
-XX:+UseZGC | spend msec:3266, sec:3</p>
<hr>
<p class="has-line-data" data-line-start="252" data-line-end="254">-Xms512m     |<br>
-Xmx512m     | spend msec:2519, sec:2</p>
<hr>
<p class="has-line-data" data-line-start="255" data-line-end="257">-Xms1024m    |<br>
-Xmx1024m    | spend msec:2326, sec:2</p>
<hr>
<p class="has-line-data" data-line-start="258" data-line-end="260">-Xms2048m    |<br>
-Xmx2048m    | spend msec:2350, sec:2</p>
<hr>
<h4 class="has-line-data" data-line-start="263" data-line-end="266" id="Ответ2">Ответ:</h4>
<p>После проведенных измерений можно сделать вывод, что использование примитивных типов, значительно<br>
увеличивают скорость работы кода.</p>