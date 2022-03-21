# AutoAce

Guilherme Ranoya, 2020

## What's it?

Create multiple instances of [Ace Editor (Web Code Editor)](https://ace.c9.io/) and Livecode Views from those instances.

## How to use it?

Load AutoAce into the document:

```html
<script src="https://www.ranoya.com/Assets/JSLibs/AutoAce/multiAce.js"></script>
```

Use `<pre>` elements as the code editors space. You can set inicial code into them:

```html
<pre
  class="editor codefull"
  id="editor_1"
  data-linguagem="java"
  data-acetheme="tomorrow"
>
  void setup() {
    size(150,150);
    background(#78008A);
    frameRate(20);
  }
</pre>
```

Set the `class` property with "editor" to mark this element for AutoAce to transform into a code editor, and define a id for it starting as "editor\_" in the `id` property. You can set the code language for Ace in the `data-linguagem` property, and the Ace theme in the `data-acetheme`.

If you want a Livecode view of the code in each code editor, create `<iframe>` elements with "View\_" and the `id` of the desired editor:

```html
<iframe id="View_editor_1"></iframe>
```

See a [working example here](https://www.ranoya.com/Assets/JSLibs/AutoAce/example.html).

You can insert previous and post codes to complete the ones edited in `<pre>` elements. To do that, create variables "Predata*" and "Postdata*" completed with the editors `id`, like these:

```js
Predata_editor_1 = "<h1>";
Postdata_editor_1 = "</h1>";
```

These editors can run javascript code, and anything loaded in the page (or via Predata).
