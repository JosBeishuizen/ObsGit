<%* 
const quoteFiles = []
app.metadataCache.getCachedFiles().forEach(filename => { 
    if (filename.contains("☀️")) { 
        quoteFiles.push(filename.slice(0, filename.length - 3)) // cut off last three characters from filename, otherwise the links would contain `.md` at the end
        }
    })
const randomIndex = Math.floor(Math.random() * (quoteFiles.length -1))
tR += `[[${quoteFiles[randomIndex].split(/(\\|\/)/g).pop()}]]`
%>