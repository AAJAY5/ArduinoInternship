---


---

<h1 id="introduction-to-embedded-system">Introduction to Embedded System</h1>
<h2 id="system-vs-embedded-system">System vs Embedded System</h2>

<table>
<thead>
<tr>
<th>System</th>
<th>Embedded System</th>
</tr>
</thead>
<tbody>
<tr>
<td>A system is a general purpose electronic device used to perform different types of tasks</td>
<td>An embedded system is a specialized system that used to perform one or a few specific tasks</td>
</tr>
<tr>
<td>A computer typically consists of a CPU, storage unit, and I/O units</td>
<td>Embedded system are designed with a microcontroller which consists of a CPU, memory unit, and I/O interface on a single IC chip</td>
</tr>
<tr>
<td>high processing power</td>
<td>relatively low processing power</td>
</tr>
<tr>
<td>Computers</td>
<td>Music Player</td>
</tr>
</tbody>
</table><h2 id="microprocessor-vs-microcontroller">Microprocessor vs Microcontroller</h2>

<table>
<thead>
<tr>
<th>uProc</th>
<th>uCont</th>
</tr>
</thead>
<tbody>
<tr>
<td>It is a processor in which memory and I/O output component is connected externally</td>
<td>It is a controlling device in which memory and I/O output component is present internally</td>
</tr>
<tr>
<td><img src="https://www.javatpoint.com/embeddedsystem/images/es-processors.png" alt="img"></td>
<td><img src="https://www.javatpoint.com/embeddedsystem/images/es-8051-microcontroller2.png" alt="img"></td>
</tr>
</tbody>
</table><h2 id="basic-embedded-system-block-diag.">Basic Embedded System Block Diag.</h2>
<p><img src="https://imgur.com/OJEkL5N.png" alt="img"></p>
<h2 id="arduino-uno-overview">Arduino UNO Overview</h2>
<h3 id="specs">Specs</h3>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>Board</td>
<td>Arduino UNO/ Arduino Nano</td>
</tr>
<tr>
<td>uCont</td>
<td>ATmega328P(8-Bit)</td>
</tr>
<tr>
<td>Digital I/O</td>
<td>14</td>
</tr>
<tr>
<td>Analog Input</td>
<td>6-8</td>
</tr>
<tr>
<td>PWM Output</td>
<td>6</td>
</tr>
<tr>
<td>Built-in LED</td>
<td>13</td>
</tr>
<tr>
<td>I/O Voltage</td>
<td>5V</td>
</tr>
<tr>
<td>I/O Current</td>
<td>20mA</td>
</tr>
<tr>
<td>Comm.</td>
<td>UART,I2C,SPI</td>
</tr>
<tr>
<td>Clock</td>
<td>16MHz</td>
</tr>
<tr>
<td>Flash Memory</td>
<td>32KB</td>
</tr>
<tr>
<td>SRAM</td>
<td>2KB</td>
</tr>
<tr>
<td>EEPROM</td>
<td>1KB</td>
</tr>
</tbody>
</table><h3 id="arduino-uno-pinout">Arduino Uno Pinout</h3>
<p><img src="https://www.electronicshub.org/wp-content/uploads/2021/01/High-Res-Arduino-UNO-Pinout.jpg" alt="img"></p>
<h3 id="arduino-nano">Arduino Nano</h3>
<p><img src="https://www.electronicshub.org/wp-content/uploads/2021/01/Arduino-Nano-Pinout.jpg" alt="img"></p>
<h2 id="programming-structure">Programming Structure</h2>
<h3 id="sketch">Sketch</h3>
<h4 id="setup">setup()</h4>
<ul>
<li>The <code>setup()</code> function is called when a sketch starts. Use it to initialize variables, pin modes, start using libraries, etc. The <code>setup()</code> function will only run once, after each powerup or reset of the Arduino board.</li>
</ul>
<h4 id="loop">loop()</h4>
<ul>
<li>After creating a <code>setup()</code> function, which initializes and sets the initial values, the <code>loop()</code> function does precisely what its name suggests, and loops consecutively, allowing your program to change and respond.</li>
</ul>
<pre class=" language-arduino"><code class="prism  language-arduino"><span class="token keyword">int</span> buttonPin <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">;</span>

<span class="token keyword">void</span> <span class="token keyword">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token builtin">Serial</span><span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token number">9600</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token function">pinMode</span><span class="token punctuation">(</span>buttonPin<span class="token punctuation">,</span> <span class="token constant">INPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token keyword">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token comment">// ...</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="control-structure">Control Structure</h3>

<table>
<thead>
<tr>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>break</td>
<td><code>break</code> is used to exit from a <code>for(), while() or do{}while()</code> loop. It is also used to exit from a <code>switch case</code> statement</td>
<td>-</td>
</tr>
<tr>
<td>continue</td>
<td>The <code>continue</code> statement <strong>skips</strong> the rest of the current iteration of a loop</td>
<td>-</td>
</tr>
<tr>
<td>do…while</td>
<td>The <code>do…​while</code> loop works in the same manner as the <code>while</code> loop, with the exception that the condition is tested at the end of the loop, so the do loop will always run at least once</td>
<td><pre>do{<br>	/* block of code */<br>}while(condition)</pre></td>
</tr>
<tr>
<td>while</td>
<td>A <code>while</code> loop will loop continuously, and infinitely, until the expression inside the parenthesis, () becomes false</td>
<td><pre>while(condition){<br>	/* block of code */<br>}</pre></td>
</tr>
<tr>
<td>for</td>
<td>The <code>for</code> statement is used to repeat a block of statements enclosed in curly braces. An increment counter is usually used to increment and terminate the loop. The <code>for</code> statement is useful for any repetitive operation, and is often used in combination with arrays to operate on collections of data/pins</td>
<td><pre>for(initialization; condition; increment) {<br>	/* statements */ <br>}<pre></pre></pre></td>
</tr>
<tr>
<td>if</td>
<td>The <code>if</code> statement checks for a condition and executes the following statement or set of statements if the condition is ‘true’</td>
<td><pre>if(condition){<br>	/* execute if true */<br>} </pre></td>
</tr>
<tr>
<td>if…else</td>
<td>The <code>if…​else</code> allows greater control over the flow of code than the basic <code>if</code> statement, by allowing multiple tests to be grouped. An <code>else</code> clause (if at all exists) will be executed if the condition in the <code>if</code> statement results in <code>false</code>. The <code>else</code> can proceed another <code>if</code> test, so that multiple, mutually exclusive tests can be run at the same time</td>
<td><pre>if(condition){<br>	// statements <br>}else if(condition){<br>	//statements <br>} else{<br>	//statements <br>}</pre></td>
</tr>
<tr>
<td>switch…case</td>
<td>Like  if statements, switch case  controls the flow of programs by allowing programmers to specify different code that should be executed in various conditions. In particular, a switch statement compares the value of a variable to the values specified in case statements. When a case statement is found whose value matches that of the variable, the code in that case statement is run.The  break  keyword exits the switch statement, and is typically used at the end of each case. Without a break statement, the switch statement will continue executing the following expressions (“falling-through”) until a break, or the end of the switch statement is reached</td>
<td><pre>switch (var) {<br>	case label1:<br>		// statements<br>		break;<br>	case label2:<br>		// statements<br>		break;<br>	default:<br>		// statements<br>		break;<br>}</pre></td>
</tr>
<tr>
<td>goto</td>
<td>Transfers program flow to a labeled point in the program</td>
<td><pre>goto label; // sends program flow to the label <br>label:<br>	// do some task</pre></td>
</tr>
<tr>
<td>return</td>
<td>Terminate a function and return a value from a function to the calling function, if desired</td>
<td><pre>int add(int a, int b){<br>	return a+b;<br>}</pre></td>
</tr>
</tbody>
</table><h3 id="arithmatic-operators">Arithmatic Operators</h3>

<table>
<thead>
<tr>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>Remainder</td>
<td>%</td>
<td>(11 % 2) = 1</td>
</tr>
<tr>
<td>Multiplication</td>
<td>*</td>
<td>(5 * 2) = 10</td>
</tr>
<tr>
<td>Addition</td>
<td>+</td>
<td>(5 + 2) = 7</td>
</tr>
<tr>
<td>Subtraction</td>
<td>-</td>
<td>(5 - 2) = 3</td>
</tr>
<tr>
<td>Division</td>
<td>/</td>
<td>(5/2) = 2</td>
</tr>
<tr>
<td>Assignment</td>
<td>=</td>
<td>int a = 10</td>
</tr>
</tbody>
</table><h3 id="comparison-operators">Comparison Operators</h3>
<ul>
<li>It return true/false.</li>
</ul>

<table>
<thead>
<tr>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>Not Equal to</td>
<td>!=</td>
<td>a != b</td>
</tr>
<tr>
<td>Equal to</td>
<td>==</td>
<td>a == b</td>
</tr>
<tr>
<td>Less than</td>
<td>&lt;</td>
<td>a &lt; b</td>
</tr>
<tr>
<td>Less than or equal to</td>
<td>&lt;=</td>
<td>a &lt;= b</td>
</tr>
<tr>
<td>Greater than</td>
<td>&gt;</td>
<td>a &gt; b</td>
</tr>
<tr>
<td>Greater than or equal to</td>
<td>&gt;=</td>
<td>a &gt;= b</td>
</tr>
</tbody>
</table><h3 id="boolean-operators">Boolean Operators</h3>

<table>
<thead>
<tr>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>Logical not</td>
<td>!</td>
<td>a = !a</td>
</tr>
<tr>
<td>Logical and</td>
<td>&amp;&amp;</td>
<td>a &amp;&amp; b</td>
</tr>
<tr>
<td>Logical or</td>
<td>||</td>
<td>a || b</td>
</tr>
</tbody>
</table><h3 id="bitwise-operators">Bitwise Operators</h3>

<table>
<thead>
<tr>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>bitwise and</td>
<td>&amp;</td>
<td>5(0b00000101) &amp; 4(0b00000100) = 1</td>
</tr>
<tr>
<td>bitwise or</td>
<td>|</td>
<td>5(0b00000101) | 8(0b00001000) = 13(0b00001101)</td>
</tr>
<tr>
<td>bitwise xor</td>
<td>^</td>
<td>5(0b00000101) ^ 7(0b00000111) = 2(0b00000010)</td>
</tr>
<tr>
<td>bitwise not</td>
<td>~</td>
<td>~ 5(0b00000101) = 250(0b11111010)</td>
</tr>
<tr>
<td>bitshift left</td>
<td>&lt;&lt;</td>
<td>1(0b00000001) &lt;&lt; 2 = 4(0b00000100)</td>
</tr>
<tr>
<td>bitshift right</td>
<td>&gt;&gt;</td>
<td>8(0b00001000)&gt;&gt;2 = 2(0b00000010)</td>
</tr>
</tbody>
</table><h3 id="compound-operators">Compound Operators</h3>
<ul>
<li>shorthand notation</li>
</ul>

<table>
<thead>
<tr>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>compound reminder</td>
<td>%=</td>
<td>x %= 2 (x = x % 2)</td>
</tr>
<tr>
<td>compound multiplication</td>
<td>*=</td>
<td>x *= 2 (x = x * 2)</td>
</tr>
<tr>
<td>compound addition</td>
<td>+=</td>
<td>x += 2 (x = x + 2)</td>
</tr>
<tr>
<td>compound subtraction</td>
<td>-=</td>
<td>x -= 2 (x = x - 2)</td>
</tr>
<tr>
<td>compound division</td>
<td>/=</td>
<td>x /= 2 (x = x / 2)</td>
</tr>
<tr>
<td>compound bitwise and</td>
<td>&amp;=</td>
<td>x &amp;= 2 (x = x &amp; 2)</td>
</tr>
<tr>
<td>compound bitwise and</td>
<td>^=</td>
<td>x ^= 2 (x = x ^ 2)</td>
</tr>
<tr>
<td>compound bitwise and</td>
<td>|=</td>
<td>x |= 2 (x = x | 2)</td>
</tr>
<tr>
<td>increment</td>
<td>++</td>
<td>x++</td>
</tr>
<tr>
<td>decrement</td>
<td>–</td>
<td>x–</td>
</tr>
</tbody>
</table><h2 id="variables">Variables</h2>
<h3 id="constants">Constants</h3>
<ul>
<li>
<p>Use <code>const or #define</code> to use declare const variables.</p>
<pre class=" language-arduino"><code class="prism  language-arduino">const <span class="token keyword">int</span> retry <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span>
<span class="token macro property">#<span class="token directive keyword">define</span> MAX_RETRY_COUNT 3</span>
</code></pre>
</li>
<li>
<p>Some const used in Arduino is listed in below table.</p>
</li>
</ul>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>HIGH</td>
<td>1</td>
</tr>
<tr>
<td>LOW</td>
<td>0</td>
</tr>
<tr>
<td>INPUT</td>
<td>input mode</td>
</tr>
<tr>
<td>INPUT_PULLUP</td>
<td>input pullup mode</td>
</tr>
<tr>
<td>OUTPUT</td>
<td>output mode</td>
</tr>
<tr>
<td>LED_BUILTIN</td>
<td>13</td>
</tr>
</tbody>
</table><h3 id="data-types">Data Types</h3>

<table>
<thead>
<tr>
<th>Type</th>
<th>Bits</th>
<th>Range</th>
</tr>
</thead>
<tbody>
<tr>
<td>bool/boolean</td>
<td>1</td>
<td>0 or 1</td>
</tr>
<tr>
<td>byte</td>
<td>8</td>
<td>0 - 255</td>
</tr>
<tr>
<td>char</td>
<td>8</td>
<td>-128 to 127</td>
</tr>
<tr>
<td>int</td>
<td>16</td>
<td>-32768 to 32767</td>
</tr>
<tr>
<td>float</td>
<td>32</td>
<td>3.4028235E+38 and as low as -3.4028235E+38</td>
</tr>
<tr>
<td>size_t</td>
<td>32</td>
<td>-2147483648 to 2147483647</td>
</tr>
<tr>
<td>void</td>
<td>-</td>
<td>-</td>
</tr>
<tr>
<td>uint8_t</td>
<td>8</td>
<td>0 to 255</td>
</tr>
<tr>
<td>uint16_t</td>
<td>16</td>
<td>0 to 65535</td>
</tr>
<tr>
<td>uint32_t</td>
<td>32</td>
<td>0 to 4294967295</td>
</tr>
<tr>
<td>int8_t</td>
<td>8</td>
<td>-128 to 127</td>
</tr>
<tr>
<td>int16_t</td>
<td>16</td>
<td>-32768 to 32767</td>
</tr>
<tr>
<td>int32_t</td>
<td>32</td>
<td>-2147483648 to 2147483647</td>
</tr>
</tbody>
</table><h3 id="utilities">Utilities</h3>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>sizeof</td>
<td>return size of variable</td>
</tr>
<tr>
<td>PROGMEM</td>
<td>Store data in flash (program) memory instead of SRAM</td>
</tr>
</tbody>
</table><h3 id="variable-scope--qualifiers">Variable Scope &amp; Qualifiers</h3>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>const</td>
<td>The <code>const</code> keyword stands for constant. It is a variable <em>qualifier</em> that modifies the behavior of the variable, making a variable “<em>read-only</em>”</td>
</tr>
<tr>
<td>static</td>
<td>The <code>static</code> keyword is used to create variables that are visible to only one function. However unlike local variables that get created and destroyed every time a function is called, static variables persist beyond the function call, preserving their data between function calls</td>
</tr>
<tr>
<td>volatile</td>
<td><code>volatile</code> is a keyword known as a variable <em>qualifier</em>, it is usually used before the datatype of a variable, to modify the way in which the compiler and subsequent program treat the variable</td>
</tr>
</tbody>
</table><h2 id="gpio-general-purpose-input-or-output">GPIO (General Purpose Input or Output)</h2>
<h3 id="push-button">Push Button</h3>
<p><img src="https://imgur.com/iTYlIkO.png" alt="push_button"></p>
<ul>
<li>As shown in above image the terminals which falls inside the oval are internally connected.</li>
</ul>
<h3 id="pull-down-configuration-with-push-button">Pull-down configuration with push button</h3>
<ul>
<li>In such a configuration the input pin or the pin which we are monitoring remains <strong><code>LOW</code></strong>  when circuit is kept open (push button is not pressed) and  <strong><code>HIGH</code></strong> when circuit is closed (push button is pressed).</li>
</ul>
<p><img src="https://imgur.com/wLweJlj.png" alt="pull_down"></p>
<h3 id="pull-up-configuration-with-push-button">Pull-up configuration with push button</h3>
<ul>
<li>In such a configuration the input pin or the pin which we are monitoring remains <strong><code>HIGH</code></strong>  when circuit is kept open (push button is not pressed) and  <strong><code>LOW</code></strong> when circuit is closed (push button is pressed).</li>
</ul>
<p><img src="https://cdn.sparkfun.com/assets/6/f/b/c/7/511568b6ce395f1b40000000.jpg" alt=""></p>
<ul>
<li>API</li>
</ul>

<table>
<thead>
<tr>
<th>API</th>
<th>Info</th>
<th>Arg</th>
<th>Return</th>
</tr>
</thead>
<tbody>
<tr>
<td>pinMode(pin,mode)</td>
<td>Configures the specified pin to behave either as an input or an output</td>
<td><pre>pin: The Arduino pin number which you want to set as an input or output<br>mode: INPUT, OUTPUT, INPUT_PULLUP</pre></td>
<td>void</td>
</tr>
<tr>
<td>digitalRead(pin)</td>
<td>Reads the value from a specified digital pin, either <code>HIGH</code> or <code>LOW</code></td>
<td><pre>pin: the Arduino pin number you want to read</pre></td>
<td>HIGH or LOW</td>
</tr>
<tr>
<td>digitalWrite(pin, value)</td>
<td>Write a <code>HIGH</code> or a <code>LOW</code> value to a digital pin</td>
<td><pre>pin: The Arduino pin number which you want write <br>value:HIGH or a LOW</pre></td>
<td>void</td>
</tr>
</tbody>
</table><ul>
<li>Example LED Blink</li>
</ul>
<pre class=" language-arduino"><code class="prism  language-arduino"><span class="token keyword">void</span> <span class="token keyword">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token punctuation">{</span>
	<span class="token function">pinMode</span><span class="token punctuation">(</span>BUILTIN_LED<span class="token punctuation">,</span><span class="token constant">OUTPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token keyword">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token punctuation">{</span>
	<span class="token comment">/* Will blink builtin led every one second*/</span>
	<span class="token function">digitalWrite</span><span class="token punctuation">(</span>BUILTIN_LED<span class="token punctuation">,</span><span class="token constant">HIGH</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token function">delay</span><span class="token punctuation">(</span><span class="token number">1000</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// delay is in millisecond</span>
	<span class="token function">digitalWrite</span><span class="token punctuation">(</span>BUILTIN_LED<span class="token punctuation">,</span><span class="token constant">LOW</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token function">delay</span><span class="token punctuation">(</span><span class="token number">1000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>Example Read &amp; Write GPIO</li>
</ul>
<pre class=" language-arduino"><code class="prism  language-arduino"><span class="token macro property">#<span class="token directive keyword">define</span> PUSH_BTN	7		</span><span class="token comment">// pin on which push button is connected</span>
<span class="token keyword">void</span> <span class="token keyword">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token punctuation">{</span>
	<span class="token function">pinMode</span><span class="token punctuation">(</span>PUSH_BTN<span class="token punctuation">,</span><span class="token constant">INPUT_PULLUP</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Set pin as input because your are reading the state </span>
	<span class="token function">pinMode</span><span class="token punctuation">(</span>BUILTIN_LED<span class="token punctuation">,</span><span class="token constant">OUTPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token keyword">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token punctuation">{</span>
	<span class="token keyword">int</span> state <span class="token operator">=</span> <span class="token function">digitalRead</span><span class="token punctuation">(</span>PUSH_BTN<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token keyword">if</span><span class="token punctuation">(</span>state <span class="token operator">==</span><span class="token constant">LOW</span><span class="token punctuation">)</span> <span class="token comment">// Button pressed </span>
	<span class="token punctuation">{</span>
		<span class="token function">digitalWrite</span><span class="token punctuation">(</span>BUILTIN_LED<span class="token punctuation">,</span><span class="token constant">HIGH</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// LED on </span>
	<span class="token punctuation">}</span>
	<span class="token keyword">else</span><span class="token punctuation">{</span> 
		<span class="token function">digitalWrite</span><span class="token punctuation">(</span>BUILTIN_LED<span class="token punctuation">,</span><span class="token constant">LOW</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// LED off</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="serial-vs.-parallel-communication">SERIAL VS. PARALLEL COMMUNICATION</h2>
<ul>
<li>
<p>The bits of data can be transmitted either in parallel or serial form. In parallel communication, the bits of data are sent all at the same time, each through a separate wire. The following diagram shows the parallel transmission of the letter “C” in binary (01000011)<br>
<img src="https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Parallel-Transmission-of-One-Byte-3-768x489.png" alt=""></p>
</li>
<li>
<p>In serial communication, the bits are sent one by one through a single wire. The following diagram shows the serial transmission of the letter “C” in binary (01000011)<br>
<img src="https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Serial-Transmission-of-the-Letter-C-768x235.png" alt=""></p>
</li>
</ul>
<h2 id="serial-uart--universal-asynchronous-receiver-transmitter">Serial (UART- Universal asynchronous receiver transmitter)</h2>
<ul>
<li>
<p>UARTs transmit data  <em>asynchronously</em>, which means there is no clock signal to synchronize the output of bits from the transmitting UART to the sampling of bits by the receiving UART. Instead of a clock signal, the transmitting UART adds start and stop bits to the data packet being transferred. These bits define the beginning and end of the data packet so the receiving UART knows when to start reading the bits.</p>
</li>
<li>
<p>When the receiving UART detects a start bit, it starts to read the incoming bits at a specific frequency known as the  <em>baud rate.</em> Baud rate is a measure of the speed of data transfer, expressed in bits per second (bps).  Both UARTs must operate at about the same baud rate. The baud rate between the transmitting and receiving UARTs can only differ by about 10% before the timing of bits gets too far off.</p>
</li>
<li>
<p>Basic connections<br>
<img src="https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-UART-Basic-Connection-Diagram-300x147.png" alt=""></p>
</li>
<li>
<p>Info<br>
<img src="https://www.circuitbasics.com/wp-content/uploads/2016/02/Basics-of-UART-Communication-Specifications-Table-768x243.png" alt=""></p>
</li>
</ul>
<h3 id="uart-packet-format">UART Packet Format</h3>
<ul>
<li>
<p>UART transmitted data is organized into <em>packets</em>. Each packet contains 1 start bit, 5 to 9 data bits (depending on the UART), an optional <em>parity</em> bit, and 1 or 2 stop bits<br>
<img src="https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-UART-Packet-Frame-and-Bits-2.png" alt=""></p>
</li>
<li>
<p><code>START BIT</code>: The UART data transmission line is normally held at a high voltage level when it’s not transmitting data. To start the transfer of data, the transmitting UART pulls the transmission line from high to low for one clock cycle</p>
</li>
<li>
<p><code>STOP BITS</code>: To signal the end of the data packet, the sending UART drives the data transmission line from a low voltage to a high voltage for at least two bit durations</p>
</li>
<li>
<p><code>DATA FRAME</code>: The data frame contains the actual data being transferred. It can be 5 bits up to 8 bits long if a parity bit is used. If no parity bit is used, the data frame can be 9 bits long. In most cases, the data is sent with the least significant bit first</p>
</li>
<li>
<p><code>PARITY</code>: Parity describes the evenness or oddness of a number. The parity bit is a way for the receiving UART to tell if any data has changed during transmission. Bits can be changed by electromagnetic radiation, mismatched baud rates, or long distance data transfers. After the receiving UART reads the data frame, it counts the number of bits with a value of 1 and checks if the total is an even or odd number. If the parity bit is a 0 (even parity), the 1 bits in the data frame should total to an even number. If the parity bit is a 1 (odd parity), the 1 bits in the data frame should total to an odd number. When the parity bit matches the data, the UART knows that the transmission was free of errors. But if the parity bit is a 0, and the total is odd; or the parity bit is a 1, and the total is even, the UART knows that bits in the data frame have changed.</p>
</li>
<li>
<p>API</p>
<ul>
<li><a href="https://www.arduino.cc/reference/en/language/functions/communication/serial/">See all API here</a></li>
</ul>
</li>
</ul>

<table>
<thead>
<tr>
<th>API</th>
<th>Info</th>
<th>Arg</th>
<th>Return</th>
</tr>
</thead>
<tbody>
<tr>
<td>begin()</td>
<td>Initialize Serial</td>
<td>Serial.begin(speed, config=SERIAL_8N1)</td>
<td>void</td>
</tr>
<tr>
<td>print()</td>
<td>Prints data to the serial port as human-readable ASCII text</td>
<td><a href="https://www.arduino.cc/reference/en/language/functions/communication/serial/print/">Link</a></td>
<td>void</td>
</tr>
</tbody>
</table><h3 id="bonus">Bonus</h3>

<table>
<thead>
<tr>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>Mode: 8N1</td>
<td>Baudrate: 9600</td>
<td>Stop: 1 bit, Start: 1 bit, Data: 8 bit</td>
<td>1 bit time (clock): 1.041ms</td>
</tr>
</tbody>
</table><h2 id="adc--analog-to-digital-converter-">ADC ( Analog to Digital Converter )</h2>

<table>
<thead>
<tr>
<th>Board</th>
<th>OPERATING VOLTAGE</th>
<th>Pins</th>
<th>Resolution(n)</th>
<th>sample time</th>
<th>Value (2^n)</th>
<th>Step Size (Vref/(2^n))</th>
</tr>
</thead>
<tbody>
<tr>
<td>Uno</td>
<td>5 Volts</td>
<td>A0 to A5</td>
<td>10 bits</td>
<td>0.1ms</td>
<td>0 - 1023</td>
<td>4.9mv/step</td>
</tr>
<tr>
<td>Nano</td>
<td>5 Volts</td>
<td>A0 to A7</td>
<td>10 bits</td>
<td>0.1ms</td>
<td>0 - 1023</td>
<td>4.9mv/step</td>
</tr>
</tbody>
</table><ul>
<li>
<p>API</p>
<pre class=" language-arduino"><code class="prism  language-arduino">	<span class="token comment">// Read adc</span>
	<span class="token function">analogRead</span><span class="token punctuation">(</span>pin<span class="token punctuation">)</span>	
	
	<span class="token comment">// Configures the reference voltage used for analog input</span>
	<span class="token function">analogReference</span><span class="token punctuation">(</span>type<span class="token punctuation">)</span>
</code></pre>
</li>
<li>
<p>analogReference()</p>
<ul>
<li>
<p>Configures the reference voltage used for analog input (i.e. the value used as the top of the input range). The options are:</p>
</li>
<li>
<p>Arduino AVR Boards (Uno, Mega, Leonardo, etc.)</p>
<ul>
<li>
<p>DEFAULT: the default analog reference of 5 volts (on 5V Arduino boards) or 3.3 volts (on 3.3V Arduino boards)</p>
</li>
<li>
<p>INTERNAL: a built-in reference, equal to 1.1 volts on the ATmega168 or ATmega328P and 2.56 volts on the ATmega32U4 and ATmega8 (not available on the Arduino Mega)</p>
</li>
<li>
<p>EXTERNAL: the voltage applied to the AREF pin (0 to 5V only) is used as the reference.</p>
</li>
</ul>
</li>
</ul>
</li>
<li>
<p>The code reads the voltage on analogPin and displays it.</p>
<pre class=" language-arduino"><code class="prism  language-arduino"><span class="token keyword">int</span> analogPin <span class="token operator">=</span> A3<span class="token punctuation">;</span> <span class="token comment">// potentiometer wiper (middle terminal) connected to analog pin 3</span>
                    <span class="token comment">// outside leads to ground and +5V</span>
<span class="token keyword">int</span> val <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>  <span class="token comment">// variable to store the value read</span>

<span class="token keyword">void</span> <span class="token keyword">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token builtin">Serial</span><span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token number">9600</span><span class="token punctuation">)</span><span class="token punctuation">;</span>           <span class="token comment">//  setup serial</span>
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token keyword">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  val <span class="token operator">=</span> <span class="token function">analogRead</span><span class="token punctuation">(</span>analogPin<span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">// read the input pin</span>
  <span class="token builtin">Serial</span><span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span>val<span class="token punctuation">)</span><span class="token punctuation">;</span>          <span class="token comment">// debug value</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
</ul>
<h2 id="pwm--pulse-width-modulation-">PWM ( Pulse Width Modulation )</h2>
<ul>
<li>Writes an analog value to a pin. Can be used to light a LED at varying brightnesses or drive a motor at various speeds. After a call to <code>analogWrite()</code>, the pin will generate a steady rectangular wave of the specified duty cycle until the next call to <code>analogWrite()</code> (or a call to <code>digitalRead()</code> or <code>digitalWrite()</code>) on the same pin</li>
<li>You do not need to call <code>pinMode()</code> to set the pin as an output before calling <code>analogWrite()</code></li>
</ul>

<table>
<thead>
<tr>
<th>Board</th>
<th>PWM Pins</th>
<th>PWM Freq</th>
<th>Resolution</th>
<th>Duty (2^n)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Uno/Nano</td>
<td>3,5,6,9,10,11</td>
<td>490Hz (5,6: 980 Hz)</td>
<td>8 bits</td>
<td>0-100% (0 - 255)</td>
</tr>
</tbody>
</table><ul>
<li>
<p>API</p>
<pre class=" language-arduino"><code class="prism  language-arduino">	<span class="token comment">// Write pwm duty value to pin</span>
	<span class="token function">analogWrite</span><span class="token punctuation">(</span>pin<span class="token punctuation">,</span>value<span class="token punctuation">)</span>
</code></pre>
</li>
<li>
<p>Example</p>
<pre class=" language-arduino"><code class="prism  language-arduino"><span class="token keyword">int</span> ledPin <span class="token operator">=</span> <span class="token number">9</span><span class="token punctuation">;</span>      						<span class="token comment">// LED connected to digital pin 9</span>

<span class="token keyword">void</span> <span class="token keyword">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token function">pinMode</span><span class="token punctuation">(</span>ledPin<span class="token punctuation">,</span> <span class="token constant">OUTPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  	<span class="token comment">// sets the pin as output</span>
  <span class="token function">analogWrite</span><span class="token punctuation">(</span>ledPin<span class="token punctuation">,</span><span class="token number">127</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 		<span class="token comment">// 50% duty</span>
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token keyword">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  
<span class="token punctuation">}</span>
</code></pre>
<p><img src="https://imgur.com/xF6i9HZ.png" alt="img"></p>
</li>
</ul>
<h2 id="i2c-inter-integrated-controller">I2C (inter-integrated controller)</h2>
<ul>
<li>
<p>I2C stands for <strong>Inter-Integrated controller.</strong> It is a bus interface connection protocol incorporated into devices for serial communication. It was originally designed by Philips Semiconductor in 1982. Recently, it is a widely used protocol for short-distance communication. It is also known as Two Wired Interface(TWI).</p>
</li>
<li>
<p>It uses only 2 bi-directional open-drain lines for data communication called SDA and SCL. Both these lines are pulled high.</p>
</li>
<li>
<p><strong>Serial Data (SDA) –</strong> Transfer of data takes place through this pin.</p>
</li>
<li>
<p><strong>Serial Clock (SCL) –</strong> It carries the clock signal.</p>
</li>
<li>
<p>I2C message packet<br>
<img src="https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-I2C-Message-Frame-and-Bit-2.png" alt="img"></p>
</li>
<li>
<p>I2C Start &amp; Stop Conditions</p>
<ul>
<li>START and STOP can be generated by keeping the SCL line high and changing the level of SDA. To generate START condition the SDA is changed from high to low while keeping the SCL high. To generate STOP condition SDA goes from low to high while keeping the SCL high, as shown in the figure below.<br>
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20210126122832/gfg31-300x120.png" alt="img"></li>
</ul>
</li>
<li>
<p>Repeated Start Condition</p>
<ul>
<li>During an I2C transfer there is often the need to first send a command and then read back an answer right away. This has to be done without the risk of another (multimaster) device interrupting this atomic operation. The I2C protocol defines a so-called repeated start condition. After having sent the address byte (address and read/write bit) the master may send any number of bytes followed by a stop condition. Instead of sending the stop condition it is also allowed to send another start condition again followed by an address (and of course including a read/write bit) and more data. This is defined recursively allowing any number of start conditions to be sent. The purpose of this is to allow combined write/read operations to one or more devices without releasing the bus and thus with the guarantee that the operation is not interrupted.<br>
<img src="https://www.i2c-bus.org/static/i2c/repeatedstart.gif" alt="img"></li>
</ul>
</li>
<li>
<p>Clock diagram<br>
<img src="https://vanhunteradams.com/Protocols/I2C/i2c_timing.png" alt="img"></p>
</li>
<li>
<p>API</p>
</li>
</ul>

<table>
<thead>
<tr>
<th>API</th>
<th>Usage</th>
<th>Master</th>
<th>Slave</th>
<th>Return</th>
</tr>
</thead>
<tbody>
<tr>
<td>begin(addr=0)</td>
<td>This function initializes the Wire library and join the I2C bus as a controller or a peripheral</td>
<td>begin()</td>
<td>begin(addr)</td>
<td>-</td>
</tr>
<tr>
<td>end()</td>
<td>Disable the Wire library, reversing the effect of <code>Wire.begin()</code></td>
<td>✔️</td>
<td>✔️</td>
<td>-</td>
</tr>
<tr>
<td>beginTransmission()</td>
<td>This function begins a transmission to the I2C peripheral device with the given address. Subsequently, queue bytes for transmission with the <code>write()</code> function and transmit them by calling <code>endTransmission()</code></td>
<td>✔️</td>
<td>❌</td>
<td>-</td>
</tr>
<tr>
<td>endTransmission(stop=true)</td>
<td>This function ends a transmission to a peripheral device that was begun by <code>beginTransmission()</code> and transmits the bytes that were queued by <code>write()</code>. <em>stop</em>: true or false. True will send a stop message, releasing the bus after transmission. False will send a restart, keeping the connection active.</td>
<td>✔️</td>
<td>❌</td>
<td><pre><br>0: success.<br>1: data too long to fit in transmit buffer.<br>2: received NACK on transmit of address.<br>3: received NACK on transmit of data.<br>4: other error.<br>5: timeout</pre></td>
</tr>
<tr>
<td>write(val),write(string), write(data, len)</td>
<td>This function writes data from a peripheral device in response to a request from a controller device, or queues bytes for transmission from a controller to peripheral device</td>
<td>✔️</td>
<td>✔️</td>
<td>number of bytes written</td>
</tr>
<tr>
<td>requestFrom(addr, bytes, stop=true)</td>
<td>This function is used by the controller device to request bytes from a peripheral device. The bytes may then be retrieved with the <code>available()</code> and <code>read()</code> functions</td>
<td>✔️</td>
<td>❌</td>
<td>the number of bytes returned from the peripheral device</td>
</tr>
<tr>
<td>available()</td>
<td>This function returns the number of bytes available for retrieval with <code>read()</code>. This function should be called on a controller device after a call to <code>requestFrom()</code> or on a peripheral inside the <code>onReceive()</code> handler. <code>available()</code> inherits from the Stream utility class</td>
<td>✔️</td>
<td>✔️</td>
<td>number of bytes available to read</td>
</tr>
<tr>
<td>read()</td>
<td>This function reads a byte that was transmitted from a peripheral device to a controller device after a call to <code>requestFrom()</code> or was transmitted from a controller device to a peripheral device. <code>read()</code> inherits from the Stream utility class</td>
<td>✔️</td>
<td>✔️</td>
<td>byte</td>
</tr>
<tr>
<td>setClock(clockFrequencyHz)</td>
<td>This function modifies the clock frequency for I2C communication. I2C peripheral devices have no minimum working clock frequency, however 100KHz is usually the baseline</td>
<td>✔️</td>
<td>❌</td>
<td></td>
</tr>
<tr>
<td>onReceive(handler)</td>
<td>This function registers a function to be called when a peripheral device receives a transmission from a controller device</td>
<td>❌</td>
<td>✔️</td>
<td>None</td>
</tr>
<tr>
<td>onRequest(handler)</td>
<td>This function registers a function to be called when a controller device requests data from a peripheral device</td>
<td>❌</td>
<td>✔️</td>
<td>None</td>
</tr>
</tbody>
</table><ul>
<li>
<p>Wiring diagram<br>
<img src="https://electrosome.com/wp-content/uploads/2018/02/I2C-Interface.png" alt="img"></p>
</li>
<li>
<p>ArduinoUNO I2C Master</p>
<pre class=" language-arduino"><code class="prism  language-arduino"><span class="token macro property">#<span class="token directive keyword">include</span> <span class="token string">&lt;Wire.h&gt;</span></span>
 
<span class="token macro property">#<span class="token directive keyword">define</span> LED0_PIN 13</span>
 
<span class="token keyword">int</span> AN_POT<span class="token punctuation">;</span>
<span class="token keyword">byte</span> RxByte<span class="token punctuation">;</span>
 
<span class="token keyword">void</span> <span class="token keyword">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Initialize I2C (Master Mode: address is optional)</span>
  <span class="token function">pinMode</span><span class="token punctuation">(</span>LED0_PIN<span class="token punctuation">,</span> <span class="token constant">OUTPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
 
<span class="token keyword">void</span> <span class="token keyword">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token comment">// I2C TX</span>
  AN_POT <span class="token operator">=</span> <span class="token function">analogRead</span><span class="token punctuation">(</span>A0<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">beginTransmission</span><span class="token punctuation">(</span><span class="token number">0x55</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Transmit to device with address 85 (0x55)</span>
  <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token punctuation">(</span>AN_POT<span class="token operator">&gt;&gt;</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>      <span class="token comment">// Sends Potentiometer Reading (8Bit)</span>
  <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">endTransmission</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>       <span class="token comment">// Stop transmitting</span>
  <span class="token comment">// I2C RX</span>
  <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">requestFrom</span><span class="token punctuation">(</span><span class="token number">0x55</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Request From Slave @ 0x55, Data Length = 1Byte</span>
  <span class="token keyword">while</span><span class="token punctuation">(</span><span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">available</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>  <span class="token comment">// Read Received Datat From Slave Device</span>
    RxByte <span class="token operator">=</span> <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">read</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
  <span class="token function">digitalWrite</span><span class="token punctuation">(</span>LED0_PIN<span class="token punctuation">,</span> <span class="token punctuation">(</span>RxByte<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token function">delay</span><span class="token punctuation">(</span><span class="token number">100</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p>ArduinoUNO I2C Slave</p>
<pre class=" language-arduino"><code class="prism  language-arduino"><span class="token macro property">#<span class="token directive keyword">include</span> <span class="token string">&lt;Wire.h&gt;</span></span>

<span class="token macro property">#<span class="token directive keyword">define</span> BTN0_PIN 4</span>

 
<span class="token keyword">byte</span> RxByte<span class="token punctuation">;</span>
<span class="token keyword">byte</span> TxByte <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
 
<span class="token keyword">void</span> <span class="token function">I2C_RxHandler</span><span class="token punctuation">(</span><span class="token keyword">int</span> numBytes<span class="token punctuation">)</span>
<span class="token punctuation">{</span>
  <span class="token keyword">while</span><span class="token punctuation">(</span><span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">available</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>  <span class="token comment">// Read Any Received Data</span>
    RxByte <span class="token operator">=</span> <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">read</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token builtin">Serial</span><span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span>RxByte<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
 
<span class="token keyword">void</span> <span class="token function">I2C_TxHandler</span><span class="token punctuation">(</span><span class="token keyword">void</span><span class="token punctuation">)</span>
<span class="token punctuation">{</span>
  <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>TxByte<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
 
<span class="token keyword">void</span> <span class="token keyword">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token builtin">Serial</span><span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token number">115200</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token function">pinMode</span><span class="token punctuation">(</span>BTN0_PIN<span class="token punctuation">,</span> <span class="token constant">INPUT_PULLUP</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token number">0x55</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Initialize I2C (Slave Mode: address=0x55 )</span>
  <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">onReceive</span><span class="token punctuation">(</span>I2C_RxHandler<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token builtin">Wire</span><span class="token punctuation">.</span><span class="token function">onRequest</span><span class="token punctuation">(</span>I2C_TxHandler<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
 
<span class="token keyword">void</span> <span class="token keyword">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">byte</span> BtnsData <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
  BtnsData <span class="token operator">=</span> <span class="token function">digitalRead</span><span class="token punctuation">(</span>BTN0_PIN<span class="token punctuation">)</span><span class="token punctuation">;</span>
  TxByte <span class="token operator">=</span> BtnsData<span class="token punctuation">;</span>
  <span class="token function">delay</span><span class="token punctuation">(</span><span class="token number">10</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
</ul>
<h2 id="spi--serial-peripheral-interface-">SPI ( Serial peripheral interface )</h2>
<ul>
<li>
<p>SPI is a common communication protocol used by many different devices. For example, SD card reader modules, RFID card reader modules, and 2.4 GHz wireless transmitter/receivers all use SPI to communicate with microcontrollers.</p>
</li>
<li>
<p>One unique benefit of SPI is the fact that data can be transferred without interruption. Any number of bits can be sent or received in a continuous stream. With I2C and UART, data is sent in packets, limited to a specific number of bits. Start and stop conditions define the beginning and end of each packet, so the data is interrupted during transmission.</p>
</li>
<li>
<p>Devices communicating via SPI are in a master-slave relationship. The master is the controlling device (usually a microcontroller), while the slave (usually a sensor, display, or memory chip) takes instruction from the master. The simplest configuration of SPI is a single master, single slave system, but one master can control more than one slave (more on this below).</p>
</li>
<li>
<p>SPI uses minimum 3(SS, SCLK, MOSI) to 4(SS, SCLK, MOSI, MISO)  wires to communicate with slave.</p>
</li>
<li>
<p><strong>MOSI (Master Output/Slave Input)</strong> – Line for the master to send data to the slave.</p>
</li>
<li>
<p><strong>MISO (Master Input/Slave Output)</strong> – Line for the slave to send data to the master.</p>
</li>
<li>
<p><strong>SCLK (Clock)</strong> – Line for the clock signal.</p>
</li>
<li>
<p><strong>SS/CS (Slave Select/Chip Select)</strong> – Line for the master to select which slave to send data to.</p>
</li>
<li>
<p>Master with multiple slave wiring diagram.<br>
<img src="https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Multiple-Slave-Configuration-Separate-Slave-Select-768x787.png" alt=""></p>
</li>
<li>
<p>SPI Modes</p>
</li>
</ul>

<table>
<thead>
<tr>
<th>Mode</th>
<th>Clock Polarity (CPOL)</th>
<th>Clock Phase (CPHA)</th>
<th>Output Edge</th>
<th>Data Capture</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPI_MODE0</td>
<td>0</td>
<td>0</td>
<td>Falling</td>
<td>Rising</td>
</tr>
<tr>
<td>SPI_MODE0</td>
<td>0</td>
<td>1</td>
<td>Rising</td>
<td>Falling</td>
</tr>
<tr>
<td>SPI_MODE0</td>
<td>1</td>
<td>0</td>
<td>Rising</td>
<td>Falling</td>
</tr>
<tr>
<td>SPI_MODE0</td>
<td>1</td>
<td>1</td>
<td>Falling</td>
<td>Rising</td>
</tr>
</tbody>
</table><ul>
<li>SPI_MODE0 clock diagram</li>
</ul>
<p><img src="https://www.analog.com/-/media/images/analog-dialogue/en/volume-52/number-3/articles/introduction-to-spi-interface/205973_fig_02.png" alt=""></p>
<ul>
<li>
<p>SPI_MODE1 clock diagram<br>
<img src="https://www.analog.com/-/media/images/analog-dialogue/en/volume-52/number-3/articles/introduction-to-spi-interface/205973_fig_03.png" alt=""></p>
</li>
<li>
<p>SPI_MODE2 clock diagram<br>
<img src="https://www.analog.com/-/media/images/analog-dialogue/en/volume-52/number-3/articles/introduction-to-spi-interface/205973_fig_05.png" alt=""></p>
</li>
<li>
<p>SPI_MODE3 clock diagram<br>
<img src="https://www.analog.com/-/media/images/analog-dialogue/en/volume-52/number-3/articles/introduction-to-spi-interface/205973_fig_04.png" alt=""></p>
</li>
<li>
<p>API</p>
</li>
</ul>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>begin()</td>
<td>Initializes the SPI bus by setting SCK, MOSI, and SS to outputs, pulling SCK and MOSI low, and SS high</td>
</tr>
<tr>
<td>beginTransaction(settings)</td>
<td>Initializes the SPI bus using the defined SPISettings</td>
</tr>
<tr>
<td>endTransaction()</td>
<td>Stop using the SPI bus. Normally this is called after de-asserting the chip select, to allow other libraries to use the SPI bus</td>
</tr>
<tr>
<td>end()</td>
<td>Disables the SPI bus (leaving pin modes unchanged)</td>
</tr>
<tr>
<td>setBitOrder(order)</td>
<td>Sets the order of the bits shifted out of and into the SPI bus, either LSBFIRST (least-significant bit first) or MSBFIRST (most-significant bit first)</td>
</tr>
<tr>
<td>setClockDivider(div)</td>
<td>Sets the SPI clock divider relative to the system clock. On AVR based boards, the dividers available are 2, 4, 8, 16, 32, 64 or 128. The default setting is SPI_CLOCK_DIV4, which sets the SPI clock to one-quarter the frequency of the system clock (4 Mhz for the boards at 16 MHz)</td>
</tr>
<tr>
<td>setDataMode(mode)</td>
<td>Sets the SPI data mode: that is, clock polarity and phase</td>
</tr>
<tr>
<td>transfer(val),transfer16(val16),transfer(buff,size)</td>
<td>SPI transfer is based on a simultaneous send and receive: the received data is returned in receivedVal (or receivedVal16). In case of buffer transfers the received data is stored in the buffer in-place (the old data is replaced with the data received)</td>
</tr>
<tr>
<td>usingInterrupt(interruptNumber)</td>
<td>If your program will perform SPI transactions within an interrupt, call this function to register the interrupt number or name with the SPI library</td>
</tr>
<tr>
<td>SPISettings(speedMaximum, dataOrder, dataMode)</td>
<td>The <code>SPISettings</code> object is used to configure the SPI port for your SPI device. All 3 parameters are combined to a single <code>SPISettings</code> object, which is given to <code>SPI.beginTransaction(SPISettings(14000000, MSBFIRST, SPI_MODE0))</code></td>
</tr>
</tbody>
</table><ul>
<li>
<p>SPI Master example</p>
<pre class=" language-arduino"><code class="prism  language-arduino"><span class="token macro property">#<span class="token directive keyword">include</span><span class="token string">&lt;SPI.h&gt;</span>                             </span><span class="token comment">//Library for SPI </span>

<span class="token macro property">#<span class="token directive keyword">define</span> LED 13</span>
<span class="token macro property">#<span class="token directive keyword">define</span> BTN 4</span>

<span class="token keyword">void</span> <span class="token keyword">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
	<span class="token builtin">Serial</span><span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token number">115200</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

	<span class="token function">pinMode</span><span class="token punctuation">(</span>LED<span class="token punctuation">,</span><span class="token constant">OUTPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span>		<span class="token comment">// LED output</span>
	<span class="token function">pinMode</span><span class="token punctuation">(</span>BTN<span class="token punctuation">,</span><span class="token constant">INPUT_PULLUP</span><span class="token punctuation">)</span><span class="token punctuation">;</span>	<span class="token comment">// BTN input</span>

	<span class="token builtin">SPI</span><span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>				<span class="token comment">// SPI Master Init</span>

	<span class="token function">digitalWrite</span><span class="token punctuation">(</span>SS<span class="token punctuation">,</span> <span class="token constant">HIGH</span><span class="token punctuation">)</span><span class="token punctuation">;</span>		<span class="token comment">// Detach SPI Slave device</span>
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token keyword">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
	<span class="token function">digitalWrite</span><span class="token punctuation">(</span>SS<span class="token punctuation">,</span> <span class="token constant">LOW</span><span class="token punctuation">)</span>		<span class="token comment">// attach SPI device</span>

	<span class="token comment">// Send BTN state of Master </span>
	<span class="token keyword">byte</span> send <span class="token operator">=</span> <span class="token function">digitalRead</span><span class="token punctuation">(</span>BTN<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token keyword">byte</span> recv <span class="token operator">=</span> <span class="token builtin">SPI</span><span class="token punctuation">.</span><span class="token function">transfer</span><span class="token punctuation">(</span>send<span class="token punctuation">)</span><span class="token punctuation">;</span>

	<span class="token comment">// Show Slave BTN status</span>
	<span class="token keyword">if</span><span class="token punctuation">(</span>recv <span class="token operator">==</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
		<span class="token function">digitalWrite</span><span class="token punctuation">(</span>LED<span class="token punctuation">,</span><span class="token constant">HIGH</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span><span class="token keyword">else</span><span class="token punctuation">{</span>
		<span class="token function">digitalWrite</span><span class="token punctuation">(</span>LED<span class="token punctuation">,</span><span class="token constant">LOW</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>

	<span class="token function">digitalWrite</span><span class="token punctuation">(</span>SS<span class="token punctuation">,</span> <span class="token constant">HIGH</span><span class="token punctuation">)</span><span class="token punctuation">;</span>		<span class="token comment">// Detach slave</span>
	<span class="token function">delay</span><span class="token punctuation">(</span><span class="token number">1000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>       

</code></pre>
</li>
<li>
<p>SPI Slave example</p>
<pre class=" language-arduino"><code class="prism  language-arduino"><span class="token macro property">#<span class="token directive keyword">include</span><span class="token string">&lt;SPI.h&gt;</span>                             </span><span class="token comment">//Library for SPI </span>

<span class="token macro property">#<span class="token directive keyword">define</span> LED 13</span>
<span class="token macro property">#<span class="token directive keyword">define</span> BTN 4</span>

volatile <span class="token keyword">byte</span> rxdata <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
volatile <span class="token keyword">bool</span> rxdone <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>

<span class="token function">ISR</span> <span class="token punctuation">(</span>SPI_STC_vect<span class="token punctuation">)</span>   <span class="token comment">//Inerrrput routine function</span>
<span class="token punctuation">{</span>
  rxdata <span class="token operator">=</span> SPDR<span class="token punctuation">;</span>
  rxdone <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token keyword">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
	<span class="token builtin">Serial</span><span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token number">115200</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

	<span class="token function">pinMode</span><span class="token punctuation">(</span>LED<span class="token punctuation">,</span><span class="token constant">OUTPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span>		<span class="token comment">// LED output</span>
	<span class="token function">pinMode</span><span class="token punctuation">(</span>BTN<span class="token punctuation">,</span><span class="token constant">INPUT_PULLUP</span><span class="token punctuation">)</span><span class="token punctuation">;</span>	<span class="token comment">// BTN input</span>

	<span class="token comment">// Slave Init</span>
	<span class="token function">pinMode</span><span class="token punctuation">(</span>SS<span class="token punctuation">,</span> <span class="token constant">INPUT_PULLUP</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  	<span class="token function">pinMode</span><span class="token punctuation">(</span>MOSI<span class="token punctuation">,</span> <span class="token constant">INPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span>		<span class="token comment">// TODO: OUTPUT?</span>
  	<span class="token function">pinMode</span><span class="token punctuation">(</span>SCK<span class="token punctuation">,</span> <span class="token constant">INPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token function">pinMode</span><span class="token punctuation">(</span>MISO<span class="token punctuation">,</span><span class="token constant">OUTPUT</span><span class="token punctuation">)</span><span class="token punctuation">;</span>       <span class="token comment">// Sets MISO as OUTPUT (Have to Send data to Master IN </span>
	SPCR <span class="token operator">|</span><span class="token operator">=</span> <span class="token function">_BV</span><span class="token punctuation">(</span>SPE<span class="token punctuation">)</span><span class="token punctuation">;</span>           <span class="token comment">// Turn on SPI in Slave Mode</span>
	<span class="token builtin">SPI</span><span class="token punctuation">.</span><span class="token function">attachInterrupt</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>      <span class="token comment">// Interuupt ON is set for SPI commnucation</span>
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token keyword">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
	<span class="token keyword">if</span><span class="token punctuation">(</span>rxdone<span class="token punctuation">)</span><span class="token punctuation">{</span>
		<span class="token keyword">if</span><span class="token punctuation">(</span>rxdata<span class="token operator">==</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
			<span class="token function">digitalWrite</span><span class="token punctuation">(</span>LED<span class="token punctuation">,</span> <span class="token constant">HIGH</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span><span class="token keyword">else</span><span class="token punctuation">{</span>
			<span class="token function">digitalWrite</span><span class="token punctuation">(</span>LED<span class="token punctuation">,</span> <span class="token constant">LOW</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>
		rxdone <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>

	<span class="token comment">// Update SPDR with slave BTN status</span>
	SPDR <span class="token operator">=</span> <span class="token function">digitalRead</span><span class="token punctuation">(</span>BTN<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token function">delay</span><span class="token punctuation">(</span><span class="token number">100</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>       

</code></pre>
</li>
</ul>
<h2 id="reference">Reference</h2>
<ul>
<li><a href="https://www.arduino.cc/reference/en/">Arduino Reference</a></li>
</ul>

