---
layout: cover
background: https://source.unsplash.com/collection/94734566/1920x1080
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
transition: slide-left
title: Welcome to Slidev
mdc: true
---

# Welcome to Slidev

Presentation slides for developers

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: content
transition: fade-out
---

# What is Slidev?

Slidev is a slides maker and presenter designed for developers, consist of the following features

- 📝 **Text-based** - focus on the content with Markdown, and then style them later
- 🎨 **Themable** - theme can be shared and used with npm packages
- 🧑‍💻 **Developer Friendly** - code highlighting, live coding with autocompletion
- 🤹 **Interactive** - embedding Vue components to enhance your expressions
- 🎥 **Recording** - built-in recording and camera view
- 📤 **Portable** - export into PDF, PNGs, or even a hostable SPA
- 🛠 **Hackable** - anything possible on a webpage

<br>
<br>

Read more about [Why Slidev?](https://sli.dev/guide/why)

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---
layout: default
---

# Problem Scenario:

When dealing with forms on the frontend, we often need to sync the state of form input elements with corresponding state in JavaScript. It can be cumbersome to manually wire up value bindings and change event listeners:

```html
<input
  :value="text"
  @input="event => text = event.target.value"
/>
```

The `v-model` directive helps us simplify the above to:

```html
<input v-model="text">
```

In addition, `v-model` can be used on inputs of different types, `textarea`, and `select` elements. It automatically expands to different DOM property and event pairs based on the element it is used on:

<img
      class="w-[20rem] absolute -top-5 -right-6"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997462/zuiw7o50cq3xzzqyeyi8.svg"
      alt="top"
    />

<img
      class="w-[20rem] absolute top-[27rem] -left-5"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997461/gvlauyrg7lkmtkkaywib.svg"
      alt="bottom"
    />

---
transition: slide-up
level: 2
---

# Basic Usage:

<div grid="~ cols-2 gap-4">
<div>

## Text

```html
<p>Message is: {{ message }}</p>
<input v-model="message" placeholder="edit me" />
```
<Text />

</div>
<div>

## Textarea

Note that interpolation inside `<textarea>` won't work. Use `v-model` instead.

```html
<!-- bad -->
<textarea>{{ text }}</textarea>

<!-- good -->
<textarea v-model="text"></textarea>
```

<Textarea />

</div>
</div>

<img
      class="w-[20rem] absolute -top-5 -right-6"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997462/zuiw7o50cq3xzzqyeyi8.svg"
      alt="top"
    />

<img
      class="w-[20rem] absolute top-[27rem] -left-5"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997461/gvlauyrg7lkmtkkaywib.svg"
      alt="bottom"
    />

---
transition: slide-up
level: 2
---

# Basic Usage:

<div grid="~ cols-2 gap-4">
<div>

## Checkbox

Single checkbox, boolean value:

```html
<input type="checkbox" id="checkbox" v-model="checked" />
<label for="checkbox">{{ checked }}</label>
```
<CheckboxSingle />

</div>
<div>

## Array of checkboxes

We can also bind multiple checkboxes to the same array.

```js
const checkedNames = ref([])
```

```html
<div>Checked names: {{ checkedNames }}</div>

<input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
<label for="jack">Jack</label>

<input type="checkbox" id="john" value="John" v-model="checkedNames">
<label for="john">John</label>

<input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
<label for="mike">Mike</label>
```

<CheckboxArrays />

</div>
</div>

<img
      class="w-[20rem] absolute -top-5 -right-6"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997462/zuiw7o50cq3xzzqyeyi8.svg"
      alt="top"
    />

<img
      class="w-[20rem] absolute top-[27rem] -left-5"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997461/gvlauyrg7lkmtkkaywib.svg"
      alt="bottom"
    />

---
transition: slide-up
level: 2
---

# Basic Usage:

<div grid="~ cols-2 gap-4">
<div>

## Radio

```html
<div>Picked: {{ picked }}</div>

<input type="radio" id="one" value="One" v-model="picked" />
<label for="one">One</label>

<input type="radio" id="two" value="Two" v-model="picked" />
<label for="two">Two</label>
```
<Radio />

</div>
<div>

## Select

Single Select:

```html
<div>Selected: {{ selected }}</div>

<select v-model="selected" class="bg-red-300">
  <option disabled value="">Please select one</option>
  <option>A</option>
  <option>B</option>
  <option>C</option>
</select>
```

<SingleSelect />

</div>
</div>

<img
      class="w-[20rem] absolute -top-5 -right-6"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997462/zuiw7o50cq3xzzqyeyi8.svg"
      alt="top"
    />

<img
      class="w-[20rem] absolute top-[27rem] -left-5"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997461/gvlauyrg7lkmtkkaywib.svg"
      alt="bottom"
    />

---
transition: slide-up
level: 2
---

# Select Continuation

### Multiple select (bound to array):

```html
<div>Selected: {{ selected }}</div>

<select v-model="selected" multiple>
  <option>A</option>
  <option>B</option>
  <option>C</option>
</select>
```
<MultipleSelect />

<img
      class="w-[20rem] absolute -top-5 -right-6"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997462/zuiw7o50cq3xzzqyeyi8.svg"
      alt="top"
    />

<img
      class="w-[20rem] absolute top-[27rem] -left-5"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997461/gvlauyrg7lkmtkkaywib.svg"
      alt="bottom"
    />
