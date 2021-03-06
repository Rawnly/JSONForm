# JSON Form
> Generate form with ease

## Installation
```sh
    npm install @react-json-form/bootstrap --save

    # or

    yarn add @react-json-form/bootstrap
```

## Style
You can use both Github `@primer/css` and `bootstrap`, just import them in your project and it will work out of the box :tada:

## Usage
All you need to do is to define a structure, you can easily do it like in the example below:

```ts
import { FormStructure } from '@react-json-form/bootstrap'

interface FormValues {
    firstName: string;
    lastName: string;

    email:string;
}

const structure: FormStructure<FormValues> = [
    [
        {
            label: 'First Name',
            name: 'firstName',
        }, {
            label: 'Last Name',
            name: 'lastName',
        }
    ], [
        {
            label: 'Email',
            name: 'email',
            required: true,
            type: 'email',
            validation: {
                pattern: {
                    message: 'Please enter a valid email',
                    value: /[a-z0-9]@[a-z]\.[a-z]/gi
                }
            }
        }
    ]
]
```