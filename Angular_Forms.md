# Making Forms
## Template Based Forms
- App.modeule.ts 
    - Import the forms to the module 
      `import { FormsModule } from '@angular/forms;`
    - Add to imports Array:
      `imports [ FormsModule, ... ]`
- In the Component
    - .html
    `<form #formObject="ngForm" (submit)="getData(formObject.value)">` needs ngForm
      `<input ngModel name="userName">` needs ngModel and name to enter into form object
      `<button>Submit</button>`
    template reference varable #formObject
    directive ="ngForm" 
              ="ngModel"
              ="ngModelGroup"
    - .ts
    `import { NgForm } from '@angular/forms'`
## Built in Validators
- min(), max(), required(), requiredTrue(), email(), minLength(), maxLength(), pattern(), nullValidator(), compose(), composeAsync()  
- Validators.pattern('[0-9]') uses regex
- function validator write your own function

## Reactive Forms

- FormControl - input element on the page with the name value
- FormGroup - An Object, A group of FormControls encapsulated together formGroup.value gets the vlaues
- FormArray - allows us to push, etc. can take FormControls or FormGroups
- FormControlName - getter for the FormGroup
- FormBuilder - shorthand syntax to create forms fb.group, fb.control, fb.array 

Dynamic form 10:30 in video https://www.youtube.com/watch?v=iqXiic6hE9U

16:42 dynamic add button

- use a FormArray array.input(index, forGroup) have a button do this


    
