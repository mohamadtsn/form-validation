# FormValidation

The best validation library for JavaScript.

![FormValidation](/art/screenshot.png)

## Using
- added this code in index.js`(entry point packages file)`
```js
window.FormValidation = require("@mohamadtsn/formvalidation/dist/amd/index");
window.FormValidation.plugins.Bootstrap = require("@mohamadtsn/custom/formvalidation/dist/amd/plugins/Bootstrap").default;
window.FormValidation.plugins.Icon = require("@mohamadtsn/custom/formvalidation/dist/amd/plugins/Icon").default;
window.FormValidation.plugins.AutoFocus = require("@mohamadtsn/custom/formvalidation/dist/amd/plugins/AutoFocus").default;
window.FormValidation.locales = require("@mohamadtsn/custom/formvalidation/dist/amd/locales/fa_IR").default;
```

## Declaring validation rules

- [x] Declarative mode

```html
<form id="registrationForm">
    <input
        name="userName"
        data-fv-not-empty="true"
        data-fv-not-empty___message="The username is required"
        data-fv-string-length="true"
        data-fv-string-length___min="6"
        data-fv-string-length___message="The name must be more than 6 characters long"
    />
</form>
```

- [x] Programmatic mode

```js
FormValidation.formValidation(
    document.getElementById('registrationForm'),
    {
        fields: {
            userName: {
                validators: {
                    notEmpty: {
                        message: 'The username is required',
                    },
                    stringLength: {
                        message: 'The name must be more than 6 characters long',
                        min: 6,                        
                    },
                },
            },
        },
    },
);
```

## Integration with your stack

- [x] Support native form
- [x] Support popular CSS frameworks via plugins
- [x] Support popular JavaScript frameworks
- [x] Easy to integrate with a framework

## Play nice with form libraries

- [x] Autocomplete
- [x] Color picker
- [x] Custom checkbox
- [x] Custom radio
- [x] Date picker
- [x] International telephone input
- [x] Mask input
- [x] Rich editor
- [x] Select
- [x] Star rating
- [x] Tag input
- [x] Time picker
- [x] Toggle
- [x] Wizard

and more!

## Supported browsers

Support the latest version of

- [x] Chrome
- [x] Firefox
- [x] Safari
- [x] Opera
- [x] Edge
- [x] Internet Explorer 11
