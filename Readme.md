
```
#
# Using of language tags, i.e.: "pl": "cos tam", "en": "something":
#

{
  "some informative name nowhere used":
  {
    "pragma_label": "CapitalizedLabelsWithoutSpacesRequired",
    "array_label": "UPPERCASE_STRING_WITH_UNDERLINES_REQUIRED",
    "contents": [
      "id": "UPPERCASE_REQUIRED",
      "pl": "Anuluj",                       <----- language tag
      "en": "Cancel"                        <----- language tag
    ]
  }
}
```

```
# "common"
#
# Use of "common" causes that language tags are ignored,
# so "pl" and "en" below will be ignored:
#
# ...
# "common": "some writting",
# "pl": "Anuluj",
# "en": "Cancel"
# ...
# 


{
  "some informative name nowhere used":
  {
    "pragma_label": "CapitalizedLabelsWithoutSpacesRequired",
    "array_label": "UPPERCASE_STRING_WITH_UNDERLINES_REQUIRED",
    "contents": [
      "id": "UPPERCASE_REQUIRED",
      "common": "some writting"             <----- "common" tag
      "pl": "Anuluj",                       <----- will be ignored
      "en": "Cancel",                       <----- will be ignored
    ]
  }
}
```


```
#
# Using tag "underline".
#
# "pl":   "Anuluj",
# "pl_m": "------"
#
# Using language tag with extension "_m" ( mask )
# informs which chars replace with underline chars.
#
# You can mask also single chars i.e.:
#
# "pl":   "Anuluj",
# "pl_m": " - - -"
#
# Chars "Auu" will be normal,
# and "nlj" will be underscored,
#
# ATTENTION:
#
# Function doesn't have safety feature, so probably will crash 
# if masking string will be longer than string to mask.
#

{
  "some informative name nowhere used":
  {
    "pragma_label": "CapitalizedLabelsWithoutSpacesRequired",
    "array_label": "UPPERCASE_STRING_WITH_UNDERLINES_REQUIRED",
    "contents": [
      "id": "UPPERCASE_REQUIRED",
      "pl":   "Anuluj",
      "pl_m": "------",                       <----- mask for underline
      "en": "Cancel"
    ]
  }
}
```



```
# Tag "menu_opt"
# "menu_opt": "1"       # [ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, < ]
#
# Char "<" is replaced with arrow one ( back from menu ).
# Option with "menu_opt" is inserted before text.
#
# Arrow is taken from normal charset.
# Digits are taken from +$80 charset ( negative ).
#
```



```
# Tag "comment": "some comment blablablabla"
#
# tagi inne niż "menu_opt", "pl", "en", "common" i inne wymagane
# Tags other than "menu_opt", "pl", "en", "common" and other required
# mentioned before are ignored so they can be used as comments.
```


```
############
### BUGS ###
############
#
# Using empty tags will cause error, i.e.:
#
# "common": "",
# "pl": "",
# "en": ""
# etc
#
# example SOLUTION - any single character i.e. space,
# or completely removing tag.
#
# "common": " "
#
```









