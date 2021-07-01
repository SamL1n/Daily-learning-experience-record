# how to style child component from parent component in Angular

background: I need to style the child component basing on the action in the parent component when I was doing the tic-tac-toe project.


I tried to find it out and visit the STACKOVERFLOW.com


Finally,I found a article specified [the style isolation of Angular](https://blog.angular-university.io/angular-host-context/).

I realized that to style child component from parent component was ## wrong!

the right way to solve the problem is to expose the style interface from child component.And then the parent component 
just needed to define the interface to style the child component.

### solution
`child.component.css`
```css
.player-o{
    background-color: aqua;
}

.player-x{
    background-color: blueviolet;
}
```
`child.component.ts`
```typescript
@Input() value!: "X" | "O";
```

`child.component.html`
```angular
<button [ngClass] = "{'player-o':value == 'O','player-X':value == 'X'}">{{value}}</button>
```

when parent component pass a `value` to the child component,it change the style of child component.

The most impotant thing is that the child component doesn't depend on any parent component.