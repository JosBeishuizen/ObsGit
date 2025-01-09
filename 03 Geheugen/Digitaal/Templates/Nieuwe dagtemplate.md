# <% tp.date.now("dddd",0,tp.file.title,"D MMMM") %> <% tp.file.title %> <% tp.date.now("YYYY")%>

⛅ , °<br>[[<% tp.date.now("D MMMM",-1,tp.file.title,"D MMMM")  %>]][[03 Geheugen/Dagboek/<% tp.date.now("YYYY/MMDD dddd D MMMM YYYY",0,tp.file.title,"D MMMM") %>| 📓 ]][[<% tp.date.now("D MMMM",1,tp.file.title,"D MMMM")  %>]]<%* let today = tp.date.now("YYYY-MM-DD",  0, tp.file.title, "D MMMM") %>
<% tp.file.include("[[Random Quote]]") %>
```tasks
(path includes Algemeen)
((due on <% today %>) OR ((due before <% today %>) AND NOT (is recurring))) AND NOT (done before <% today %>) AND NOT (created <% today %>)
# not done
hide due date
hide start date
hide recurrence rule
hide tags
hide backlink
hide done date
hide task count
hide created date
hide edit button
hide postpone button 
sort by priority 
```