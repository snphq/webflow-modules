## NATIVE SLIDER

## <a href="https://native-slider-1c209b.webflow.io/" target="_blank">DEMO</a>

## Installation
Add styles link to head:
```html
<link href="https://cdn.jsdelivr.net/gh/snphq/webflow-modules/native-slider/1.0.1/index.min.css" rel="stylesheet" type="text/css">
```
Add script link to footer:
```html
<script src="https://cdn.jsdelivr.net/gh/snphq/webflow-modules/native-slider/1.0.1/index.min.js" type="text/javascript"></script>
```

## Usage

### Optional functions:

Controls buttons:
```html
<div wm-ns-prev></div>
<div wm-ns-next></div>
```

Mouse dragging (add "draggable" value):
```html
<div wm-ns-list="draggable">...</div>
```

### - Simple copy / paste from webflow account (recommended)

Copy prepared block with slider from SNP webflow account: "modules" folder, "Native slider" project. Then customize "slider", "slide", "nav", "btn" elements with your own classes and designs.

Add disabled navigation button styles for "m_wm-ns-disabled" classname.

### - Creating html and styles from scratch

**html structure:**
```html
<div wm-ns>
  <div wm-ns-list="draggable" class="slider">
    <div class="slide">Slide 1</div>
    <div class="slide">Slide 2</div>
    <div class="slide">Slide 3</div>
    <div class="slide">Slide 4</div>
    <div class="slide">Slide 5</div>
    <div class="slide">Slide 6</div>
    <div class="slide">Slide 7</div>
    <div class="slide">Slide 8</div>
  </div>

  <div>
    <div wm-ns-prev class="m_wm-ns-disabled">previous</div>
    <div wm-ns-next>next</div>
  </div>
</div>
  ```

  **styles:**
  ```css
.slider {
  display: flex;
  gap: 10px;
  overflow: auto;
}

.slide {
  flex-shrink: 0;
  flex-grow: 0;
}

.slide:first-child {
  margin-left: 20px;
}

.slide:last-child {
  margin-right: 20px;
}

.m_wm-ns-disabled {
  opacity: 0.7;
}
```
