# AbstractControl

## Description
It provides some of the shared behavior that all controls and groups of controls have, like running validators, calculating status, and resetting state. It also defines the properties that are shared between all sub-classes, like value, valid, and dirty. It shouldn't be instantiated directly.

## Properties

| Name | Description |
|----------|-------------------------------------------------------------|
| value: any | The current value of the control. For a FormControl, the current value. For an enabled FormGroup, the values of enabled controls as ab object with a key-value pair for each member of the group. For a disabled FormGroup, the values of all controls as an object with a key-value pair for each member of the group. For a FormArray, the values of enabled controls as an array. |
| valueChanges: Observable\<any> | A multicasting observable that emits an event every time the value of the control changes, in the UI or programatically. It also emits an event each time you call enable() or disable() without passing along {emitEvent: false} as a function argument. |

## Methods

| Name | Description |
|----------|-------------------------------------------------------------|
| setValidators(newValidator: ValidatorFn \| ValidatorFn[]): void | Sets the synchronous validators that are active on this control. Calling this overwrites any existing sync validators. When you add or remove a validator at run time, you must call updateValueAndValidity() for the new validation to take effect. |
| clearValidators(): void | Empties out the snyc validator list. When you add or remove a validator at run time, you must call updateValueAndValidity() for the new validation to take effect. |
| abstract setValue(value: any, options?: Object): void | Sets the value of the control. Abstract method (implemented in sub-classes). |
| updateVlueAndValidity(opts:{ onlySelf?: boolean; emitEvent?: boolean; } = {}): void | Recalculates the value and validation status of the control. By default, it also updates the value and validity of its ancestors. |
