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
    - .ts
    `import { NgForm } from '@angular/fomrs'`
    
