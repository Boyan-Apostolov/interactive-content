# Reactive Forms

[slide hideTitle]

# Reactive Forms Overview

Reactive forms provide a model-driven approach to handling form inputs whose values change over time.

Reactive forms are immutable. A change to the form state returns a new state, which maintains the integrity of the model between changes. 

They are built around observable streams, where form inputs and values are provided, as streams of input values, which can be accessed synchronously.

Reactive forms also make testing easy.

This way, we are assured that our data is consistent and predictable when requested.

[/slide]

[slide hideTitle]

# Reactive Forms Module

To use reactive forms, we need the **Reactive Forms Module**.

```js
import { ReactiveFormsModule } from '@angular/forms'
```

After importing the **Reactive Forms Module**, we have access to all the needed directives like:
- **formGroup**
- **formControl** and **formControlName**
- **formGroupName**
- **formArrayName**

[/slide]

[slide hideTitle]

# The Component Class

In the component class, create instances of **FormGroup** and **FormControl** that we will bind later in the template.

By creating these controls in our component class, we get immediate access to listen for, **update**, and **validate** the state of the form input.

Update the template with the form control using the **formControl** binding provided by FormControlDirective.

The core idea is to transfer most of the logic from the template inside the component class.

```js
import { FormGroup, FormControl } from '@angular/forms'
```

```js
this.laptopForm = new FormGroup({
    processor : new FormControl('Intel Core i7'),
    ram : new FormControl('16 GB DDR4')
});
```

[/slide]

[slide hideTitle]

# The Template

In the template, we have to mark the main **formGroup** and after that add **formControlName** to each form control.

Here the **formControlName** is the name of the key instance.

```html
<form (ngSubmit)="save()" [formGroup]="laptopForm">
```

```html
<input type="text" class="form-control" id="processor"
    required
    formControlName="processor">
```

[/slide]

[slide hideTitle]

# Accessing Form Model Properties

There are two ways to access the properties of the form model.

This is the first one: `laptopForm.controls.processor.valid`.

This is the second one: `laptopForm.get('processor').valid`.

The idea is to shorten the template and transfer such logic in the component when using reactive forms.

[/slide]

[slide hideTitle]

# Using Form Builder

Use the **FormBuilder** service to avoid creating instances of **FormGroup** and **FormControl** name.

```js
import { FormBuilder } from '@angular/forms';
```

Inject it into the constructor.

```js
constructor(private fb : FormBuilder) { }
```

```js
this.laptopForm = this.fb.group({
    processor : 'Intel Core i7',
    ram : '16 GB DDR4'
});
```

[/slide]

[slide hideTitle]

# Validation

Angular gives us the possibility to **add** or **remove** validators dynamically in reactive forms based on some user action.

- **Cross-field** validation: It is validating one form control based on the value of another.
- We can also create custom validators with parameters:

For that, we create a **factory function**, which accepts the **parameter**. The **factory function** returns the **validator function**.
- We can adjust rules at runtime.

[/slide]

[slide hideTitle]

# Setting Up Build-in Validation

Defining our **FormGroup** with a **FormBuilder** allows us to add an array of validations using the **Validators** class.

```js
this.laptopForm = this.fb.group({
    processor : [
        'Intel core i7', [
            Validators.required,
            Validators.minLength(10)
        ]
    ]
});
```

[/slide]

[slide hideTitle]

# Ajust the Template

The **formGroup** directive has an errors property, which can be used to **show** errors only when needed.

```html
<div *ngIf="(laptopForm.get('processor').touched 
|| laptopForm.get('processor').dirty) 
&& laptopForm.get('processor').errors" class="alert alert-danger">
<span *ngIf="laptopForm.get('processor').errors.required">
  Processor is required!
</span>
<span *ngIf="laptopForm.get('processor').errors.minlength">
  Processor should be at least 10 symbols long!
</span>
</div>
```

[/slide]

[slide hideTitle]

# Watching and Reacting to Changes

Using **Reactive Forms** we have the ability to **watch** and **react** to changes on form **groups** and form **controls**.

Whenever a **value** of an input **changes**, we can **subscribe** to that event and handle the **observable**.

```js
this.laptopForm.get('os')
.valueChanges
.subscribe(console.log);
```

[/slide]

[slide hideTitle]

# Reactive Transformation Example

Import **throttleTIme** from the following library.

```js
import { throttleTime } 'rxjs/operators';
```

Attach the **throttleTIme** function to a form control's **valueChanges** event.

```js
processorControl.valueChanges
.pipe(throttleTime(1500))
.subscribe(value => {
    console.log(value);
});
```

[/slide]