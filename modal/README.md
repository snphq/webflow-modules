## MODAL / MOBILE MENU

## <a href="https://modal-mobile-menu.webflow.io/" target="_blank">DEMO</a>

## Installation
Add styles link to head:
```html
<link href="https://cdn.jsdelivr.net/gh/snphq/webflow-modules/modal/1.0.0/index.min.css" rel="stylesheet" type="text/css">
```
Add script link to footer:
```html
<script src="https://cdn.jsdelivr.net/gh/snphq/webflow-modules/modal/1.0.0/index.min.js" type="text/javascript"></script>
```

## Usage

### Open / close animation:

If you need animation, you can create your own and apply it with `.m_wm-m-show` and `.m_wm-m-close` classnames.

You can use build in **FADE** animation:
```css
[wm-m=product].m_wm-m-show {
  animation: fadeIn 0.3s;
}

[wm-m=product].m_wm-m-close {
  animation: fadeOut 0.3s;
}
```

Example how to create your own animation:
```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes fadeOut {
  from {
    visibility: visible;
    opacity: 1;
  }
  to { opacity: 0; }
}
```

### core components

`menu` - modal key, common for current modal, open and close buttons.

`wm-m-open="menu"` - show modal button attribute.

`wm-m-close="menu"` - hide modal button attribute.

`wm-m="menu"` - modal element.

### - Simple copy / paste from webflow account (recommended)

Copy prepared block with modal from SNP webflow account: "modules" folder, "Modal / Mobile menu" project. Then customize "mobile-menu" or "modal" and nested elements with your own classes and designs.

### - Creating html and styles from scratch

**html structure:**
```html
<div wm-m-open="menu">open menu</div>

<div wm-m="menu" class="modal-container">
  <div class="mobile-menu">
    <div wm-m-close="menu">close</div>
    <div class="mobile-menu-content">
      <div class="mobile-menu-nav">
        <a href="/#home">home</a>
        <a href="/#about">about</a>
        <a href="/#products">products</a>
        <a href="/#careers">careers</a>
        <a href="/#projects">projects</a>
        <a href="/#price">price</a>
        <a href="/#blog">blog</a>
      </div>
    </div>
  </div>
</div>

<div wm-m-open="product">open modal</div>

<div wm-m="product" class="modal-container">
  <div class="modal">
    <div wm-m-close="product" class="modal-backdrop"></div>
    <div class="modal-content">
      <div wm-m-close="product">close</div>
      <div>product title</div>
      <div>product description</div>
    </div>
  </div>
</div>
  ```

**styles:**
```css
.modal-container {
  display: none;
}

.mobile-menu {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  background-color: #38566d;
}

.mobile-menu-content {
  overflow: auto;
  padding: 20vh 20vw;
  max-height: 60vh;
}

.mobile-menu-nav {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 100px;
}

.modal {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-backdrop {
  background-color: rgba(000, 000, 000, 0.7);
  width: 100%;
  height: 100%;
  position: absolute;
  z-index: -1;
}

.modal-content {
  position: relative;
  width: 500px;
  height: 200px;
  padding: 20px;
  background-color: #282c34;
}

[wm-m=product].m_wm-m-show {
  animation: fadeIn 0.3s;
}

[wm-m=product].m_wm-m-close {
  animation: fadeOut 0.3s;
}
```
