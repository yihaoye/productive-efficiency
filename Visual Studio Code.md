Put mutiple cursors to every line (which is selected) ends (`option` `shift` `i` for Mac). [Ref](https://stackoverflow.com/questions/31490989/how-do-i-get-a-cursor-on-every-line-in-vscode)  
  
Move from above ends to heads / left most (`fn`+`<-` for Mac).  
  
在项目中根据文件名寻找文件：`command` + `p` for Mac.  
在项目中寻找内容包含指定字符串的文件：`command` + `shift` + `f` for Mac.  
  
怎样复制索搜 match 到的结果，[参考](https://stackoverflow.com/questions/41961368/visual-studio-code-how-to-copy-search-results)  
The following works for a single file:  
```
CTRL + F
Type your search string
CTRL + SHIFT + L to select all occurrences found (max. 9999)
ESC (or close search dialog with top-right X)
CTRL + I to select whole lines
CTRL + C
Open new file
CTRL + V
```  
  
VS Code 通过正则表达式搜索 UUID  
The regex for uuid is:  
`\b[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}\b`  
