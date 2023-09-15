# arcade

## Create labels that introduce a new line on the last space in the field:

```
var words = Split($feature.NAME, " ")
var expression = ""
for (var index in words) {
   var connector = IIf(index == Count(words) - 1, TextFormatting.NewLine, IIf(index == 0, "", " "))
   expression += Concatenate(connector, words[index])
}
return expression
```
