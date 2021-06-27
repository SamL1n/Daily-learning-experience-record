# ngClass

`string` - the CSS classes listed in the string (space delimited) are added

`Array` - the CSS classes declared as Array elements are added

`Object` - keys are CSS classes that get added when the expression given in the value evaluates to a truthy value, otherwise they are removed.

```html
<h1 [ngClass]="{'player-x':square == 'X','player-o':square == 'O'}"></h1>
```


```html
<some-element [ngClass]="'first second'">...</some-element>

<some-element [ngClass]="['first', 'second']">...</some-element>

<some-element [ngClass]="{'first': true, 'second': true, 'third': false}">...</some-element>

<some-element [ngClass]="stringExp|arrayExp|objExp">...</some-element>

<some-element [ngClass]="{'class1 class2 class3' : true}">...</some-element>
```