
[[obsidian tutorials]]
# H1
## H2
### H3
#### H4
##### H5
###### H6


###### enable any css in obsidian
`settings > Apperiance > CSS Snippets > select file`
then reload css button next to it


create css file at path `yourVaultPath/.snippets/headingcolor.css` 
add these lines
```
.cm-header-1 { color: #f37b84; }
.cm-header-2 { color: #ffd98c; }
.cm-header-3 { color: #9ff369; }
.cm-header-4 { color: #59d5c4; }
.cm-header-5 { color: #2a8aff; }
.cm-header-6 { color: #b99aff; }
```


create css file at path `yourVaultPath/.snippets/readablelinelength.css` 
add these lines
```
body {
  --file-line-width:1300px
}
```