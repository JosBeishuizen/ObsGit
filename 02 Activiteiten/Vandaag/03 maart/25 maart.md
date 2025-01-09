# 25 maart
<span style="color: #688bc4;"><br>zaterdag 2023: eten bij Sara en Toon<br>het weer: wind en regen, 11°</span> 

```dataviewjs
const fnaam = dv.current().file.name;
let dag = fnaam.split(" ")[0];
if (dag.length === 1) {dag = "0" + dag}
let mnd = fnaam.split(" ")[1];
if (mnd === "januari") {mnd = "01"};
if (mnd === "februari") {mnd = "02"};
if (mnd === "maart") {mnd = "03"};
if (mnd === "april") {mnd = "04"};
if (mnd === "mei") {mnd = "05"};
if (mnd === "juni") {mnd = "06"};
if (mnd === "juli") {mnd = "07"};
if (mnd === "augustus") {mnd = "08"};
if (mnd === "september") {mnd = "09"};
if (mnd === "oktober") {mnd = "10"};
if (mnd === "november") {mnd = "11"};
if (mnd === "december") {mnd = "12"};
let page = dv.pages("#taken").file.tasks;
dv.taskList(page.where(t => t.text.includes(dag + "-" + mnd)), false);
```
<p style="padding-left: 2.7em; text-indent: -2.7em; margin: 0;"><font color=#8be9f6>12:18</font>  Nu een uur de kranten lezen en lunchen. Dan ekklesia </p>   
<p style="padding-left: 2.7em; text-indent: -2.7em; margin: 0;"><font color=#8be9f6>14:57</font>  Nu ekklesia.  verslag controleren. Eerst verslag openen.  </p>   
<p style="padding-left: 2.7em; text-indent: -2.7em; margin: 0;"><font color=#8be9f6>15:20</font>  Ik ga nu even in het dagboek schrijven. </p>   