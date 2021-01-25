# Summary

[slide hideTitle]

## In this lesson you learnt:

- There are three types of Directives
    - Components, Structural, Attribute
```js
@Directive({
    selector: '[appHighlight]' 
})
export class HighlightDirective {
    constructor() { }
}
```
- There are two ways to handle forms in Angular
    - Template-driven Forms
    - Reactive Forms
```js
import { Component } from '@angular/core';
import { FormControl } from '@angular/forms';

@Component({
  selector: 'app-name-editor',
  templateUrl: './name-editor.component.html',
  styleUrls: ['./name-editor.component.css']
})
export class NameEditorComponent {
  name = new FormControl('');
}
```
- Directives are integrated into Form Modules

## In the next lesson you will learn:

Workshop - Forms

[/slide]