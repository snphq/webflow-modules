## HORIZONTAL SCROLL

## [DEMO](https://horizontall-scroll-a2154a.webflow.io)

## Installation
Add styles link to head:
```html
<link href="https://cdn.jsdelivr.net/gh/snphq/webflow-modules/horizontal-scroll/1.0.0/index.min.css" rel="stylesheet" type="text/css">
```
Add script link to footer:
```html
<script src="https://cdn.jsdelivr.net/gh/snphq/webflow-modules/horizontal-scroll/1.0.0/index.min.js" type="text/javascript"></script>
```

## Usage
Best way is to copy prepared "gallery" block with horizontall scroll from SNP webflow account: "modules" folder, "Horizontall scroll" project. Then add your own styles instead "gallery" class styles.
index.css can help to escape custom code styles:
```css
.wm-hs-track-wrapper {
  overflow: hidden;
}

.wm-hs-track {
  width: max-content;
}
```

**html structure:**
```html
<div class="wm-hs" wm-hs>
    <div class="wm-hs-container">
      <div class="wm-hs-track-wrapper">
        <div class="wm-hs-track" wm-hs-track>
          <div></div>
          <div></div>
          ...
        </div>
      </div>
    </div>
  </div>
  ```

  **styles:**
  ```css
  .wm-hs {
  width: 100%;
  position: relative;
  min-height: 100vh;
}

.wm-hs-container {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  z-index: 1;
}

.wm-hs-track-wrapper {
  position: sticky;
  top: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.wm-hs-track {
  height: 100%;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-shrink: 0;
  width: max-content;
}
```
