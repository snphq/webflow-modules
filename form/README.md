## FORM

## <a href="https://form-63d2ee.webflow.io/" target="_blank">DEMO</a>

## Installation
Add script link to footer:
```html
<script src="https://cdn.jsdelivr.net/gh/snphq/webflow-modules/form/1.0.0/index.min.js" type="text/javascript"></script>
```

## Usage

### core components

`name` - field key for field error.

`wm-f-field="name"` - field attribute, add it if field has validation.

`wm-f-required="name is required"` - field attribute, which trigger required validation, attribute value is error title.

`wm-f-email="must be email"` - field attribute, which trigger is email validation, attribute value is error title.

`wm-f-field-error="name"` - optional text block with error.

`autosize` - optional attribute for textarea, set height based on content.

### - Simple copy / paste from webflow account (recommended)

Copy prepared block with modal from SNP webflow account: "modules" folder, "Form" project. Then customize "form" and nested elements with your own classes and designs.

Add error styles for field and field-error with classname `m_wm-f-field-error`.

### - Creating html and styles from scratch

**html structure:**
```html
<form wm-f class="form" novalidate>
  <div>
    <input
      wm-f-field="name"
      wm-f-required="name is required"
      class="input"
      placeholder="name*"
    />
    <div wm-f-field-error="name" class="field-error"></div>
  </div>

  <div>
    <input
      wm-f-field="email"
      wm-f-required="email is required"
      wm-f-email="must be email"
      class="input"
      placeholder="email*"
      type="email"
    />
    <div wm-f-field-error="email" class="field-error"></div>
  </div>

  <textarea autosize placeholder="message" class="input"></textarea>

  <button type="submit" class="button">submit</button>
</form>
```

**styles:**
```css
textarea {
  resize: none;
}

.button {
  font-size: 20px;
  border-radius: 5px;
  cursor: pointer;
  padding: 15px;
  background-color: #b18c3c;
  display: inline-block;
  user-select: none;
  border: none;
  color: $white;
}

.form {
  width: 300px;
  display: flex;
  flex-direction: column;
  gap: 40px;
}

.input {
  width: 100%;
  padding: 5px 0;
  background-color: transparent;
  font-size: 20px;
  outline: none;
  margin: 0;
  border: none;
  color: $white;
  border-bottom: 1px solid #d7dae0;
}

.input.m_wm-f-field-error {
  border-color: $red;
}

.field-error {
  margin-top: 10px;
  color: $white;
  opacity: 0;
}

.field-error.m_wm-f-field-error {
  opacity: 1;
}
```
