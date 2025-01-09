# 8 juni
donderdag 2023: Egmond, COBEX; het weer: half bewolkt, 21°

```dataviewjs
const fnaam = await dv.current().file.name;
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
let page = await dv.pages("#taken").file.tasks;
dv.taskList(page.where(t => t.text.includes(dag + "-" + mnd)), false);
```
<p style="padding-left: 2.7em; text-indent: -2.7em; margin: 0;"><font color=#8be9f3>07:45  </font>  Even dagboek. </p>   
<p style="padding-left: 2.7em; text-indent: -2.7em; margin: 0;"><font color=#8be9f3>17:33  </font>  Artikel in Ad Valvad lezen en artikel in NRC </p>   