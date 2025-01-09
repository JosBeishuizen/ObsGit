<%*
const filename = tp.file.selection()
const folder = app.vault.getAbstractFileByPath("01 Algemeen/Planning/Taken")
if (!tp.file.exists(filename))
{tp.file.create_new("", filename, false, folder)} 
%>[[<% filename %>]]