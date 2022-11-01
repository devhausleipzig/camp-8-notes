The selectors are ordered by specificity (highest at the bottom)

| Name | Syntax | Selects |
| --- | --- | --- |
| Universal | * | Every element |
| Root | :root | The html tag |
| Element | tagName | Every instance of the specified element |
| Class | .className | Every element that has the specified class |
| ID | \#id | The one element that has the specified id |

## Pseudo Selectors

| Name | Syntax | Selects |
| --- | --- | --- |
| Hover | selector:hover | Specified selector when the mouse hovers over it |
| Active | selector:active | Specified selector when that element is currently clicked |
| Visited | selector:visited | Specified selector when we previously used it to navigate (works only on `a`) |
