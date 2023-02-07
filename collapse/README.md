## COLLAPSE

## <a href="https://collapse-bdd35e.webflow.io/" target="_blank">DEMO</a>

## Installation

Add styles to footer:
```html
<style>
[wm-c-content] {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s;
}
</style>
```

Add script link to footer:
```html
<script src="https://cdn.jsdelivr.net/gh/snphq/webflow-modules/collapse/1.1.0/index.min.js" type="text/javascript"></script>
```

## Usage

### core components

***single block***

`wm-c` - main attribute for block.

`wm-c="open"` - "open" value shows hidden content by default.

`wm-c-content` - attribute for hidden content.

`wm-c-btn` - collapse button attribute.

***one visible block from list***

`wm-c-list` - main attribute for blocks wrapper.

`wm-c-item` - main attribute for block.

`wm-c-item="open"` - "open" value shows hidden content by default.

`wm-c-content` and `wm-c-btn` same as for the single block.

***styles***

`m_wm-c-open` - classname, added to the collapse button when content visible, add styles for open state if you need it.

### - Simple copy / paste from webflow account (recommended)

Copy prepared block with modal from SNP webflow account: "modules" folder, "Collapse" project. Then customize elements with your own classes and designs.

### - Creating html and styles from scratch

**html structure for single block:**
```html
<div wm-c="open">
  <div wm-c-content>
    <br>
    Pulvinar mattis nunc sed blandit libero volutpat sed cras ornare. Imperdiet dui accumsan sit amet nulla facilisi morbi. Porta nibh venenatis cras sed felis eget velit. Aliquet eget sit amet tellus cras adipiscing enim. Augue ut lectus arcu bibendum at varius vel pharetra vel. Sit amet nisl purus in mollis.
  </div>
  <div wm-c-btn>collapse button</div>
</div>
```

**html structure for list:**
```html
<div wm-c-list>
  <div wm-c-item="open">
    <div wm-c-btn>collapse button</div>
    <div wm-c-content>
      <br>
      Pulvinar mattis nunc sed blandit libero volutpat sed cras ornare. Imperdiet dui accumsan sit amet nulla facilisi morbi. Porta nibh venenatis cras sed felis eget velit. Aliquet eget sit amet tellus cras adipiscing enim. Augue ut lectus arcu bibendum at varius vel pharetra vel. Sit amet nisl purus in mollis.
    </div>
  </div>

  <div wm-c-item>
    <div wm-c-btn>collapse button</div>
    <div wm-c-content>
      <br>
      Pulvinar mattis nunc sed blandit libero volutpat sed cras ornare. Imperdiet dui accumsan sit amet nulla facilisi morbi. Porta nibh venenatis cras sed felis eget velit. Aliquet eget sit amet tellus cras adipiscing enim. Augue ut lectus arcu bibendum at varius vel pharetra vel. Sit amet nisl purus in mollis.
    </div>
  </div>

  <div wm-c-item>
    <div wm-c-btn>collapse button</div>
    <div wm-c-content>
      <br>
      Pulvinar mattis nunc sed blandit libero volutpat sed cras ornare. Imperdiet dui accumsan sit amet nulla facilisi morbi. Porta nibh venenatis cras sed felis eget velit. Aliquet eget sit amet tellus cras adipiscing enim. Augue ut lectus arcu bibendum at varius vel pharetra vel. Sit amet nisl purus in mollis.
    </div>
  </div>
</div>
```

**styles:**
```css
[wm-c-content] {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s;
}
```
