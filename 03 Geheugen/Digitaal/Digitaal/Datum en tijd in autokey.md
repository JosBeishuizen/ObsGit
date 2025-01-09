# Datum en tijd in autokey
output = system.exec_command("date '+%H:%M'")
keyboard.send_keys(output[:5]+" ")

output = system.exec_command("date '+%d-%m-%Y'")
keyboard.send_keys(output[:10]+" ")

dag = system.exec_command("date '+%a'")
if dag == "Sun": dw = "zondag "
if dag == "Mon": dw = "maandag "
if dag == "Tues": dw = "dinsdag "
if dag == "Wednes": dw = "woensdag "
if dag == "Thurs": dw = "donderdag "
if dag == "Fri": dw = "vrijdag "
if dag == "Satur": dw = "zaterdag "
keyboard.send_keys("<tblauw>" + dw + "2022, °</tblauw>")
