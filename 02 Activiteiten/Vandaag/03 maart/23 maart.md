# 23 maart
<span style="color: #688bc4;"><br>donderdag 2023: <br>het weer: , °</span> 

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
- [x] oppassen op EAO

<p style="padding-left: 2.7em; text-indent: -2.7em; margin: 0;"><font color=#8be9f3>21:30  </font>  Nu nog even h3 lezen. </p>   