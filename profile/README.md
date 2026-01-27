

  <b>
    <p align="center">
      <a href="https://github.com/alchira/package/wiki">Get Started</a>
      &nbsp; · &nbsp;
      <a href="https://github.com/alchira/tutorial">Tutorial</a>
      &nbsp; · &nbsp;
      <a href="https://github.com/sponsors/yshelldev">Support</a>
      &nbsp; · &nbsp;
      <a href="https://github.com/orgs/alchira/discussions">Discussions</a>
    </p>
  </b>


---

## Alchira — a WebUI Workbench for HTML & CSS

Alchira is a **compile-time WebUI workbench** that lets you design, preview, and evolve web UI **without locking you into a framework or runtime**.

It produces **plain HTML and CSS** — no client runtime, no JS API, no magic in production.

What it changes is *how* you author UI.

---

### Why Alchira exists

Most UI tools optimize for **speed of creation**.  
They do *not* optimize for **safety of change**.

As projects grow, CSS tends to break down:

* Styles leak across components
* Refactors feel risky
* Variants and responsive logic scatter across files
* Cascade rules become implicit and fragile
* You stop trusting your own styles

Alchira is built for the opposite goal:

> **Make UI changes predictable, local, and reversible.**

If your UI changes often — redesigns, theming, refactors, experiments — Alchira is for you.  
If you’re happy shipping throwaway styles fast, you probably don’t need it.

---

### What kind of tool is this?

Alchira is **not**:

* a CSS framework
* a JS framework
* a runtime library
* a replacement for React, Vue, or Svelte

Alchira **is**:

* a **language layer** that unifies structure and styling
* a **Workbench** for designing UI systems safely

You write intent once.
Alchira compiles it into clean, optimized CSS and standard HTML.

---

### The core idea (in one sentence)

> **Structure and style belong together — and should be changed together.**

Instead of scattering intent across templates, CSS files, and config,
Alchira lets you declare *what a component is* and *how it behaves visually* in one place.

---

### You don’t have to go all-in

Alchira is intentionally **progressive**.

You can use it:

* just for utility classes
* just for scoped component styles
* just for safer variants
* or as a full UI workbench with live previews

Stop at any point.
Everything still compiles to standard CSS.

---

### What Alchira gives you

* **Unified HTML + CSS authoring** — no context switching
* **Scoped styles by default** — fewer leaks, safer refactors
* **Explicit cascade control** — no selector guessing
* **Variants and responsive logic where components are used**
* **Compile-time isolation** — no runtime cost
* **Editor-native workflows** — preview, inspect, and navigate instantly

---

If this sounds like something you’ve been missing, continue below.
If not — that’s okay. Alchira is intentionally opinionated.

---

⬇️ **Start simple. Add power only when you need it.**

---

> Some tags starts with `\<` as escape charector for tags, in the following examples.

### Level 1: Want to use Utility classes?

Use ~ to trigger class loading in place:
```html
\<div class="~flex ~flex-col"> {{content}} </div>
<script>
  const classnames = ["\~flex","\~flex-col"]
</script>
```
Provided that these classes are either available in libraries, or defined atlease once.  
Using `~` trigger avoids colltion with other desing systems.  
Using `\~` trigger to load classnames outside html tags.  


### Level 2: Just want create new style?

Use $ for local scope:
```html
\<button 
class="~$button-1" 
_$button-1="
  padding: 1rem; 
  background: blue;
">
  {{content}}
</button>
```

That's it. Styles with structure. No separate CSS file.
Reusable in same file.

```html
<button class="~$button">
```

Alternatively compose like utility classes and add custom attrubutes later.  
Use CSS like nesting for for states control.

```html
\<div 
class="~$button-3" 
_$button-3="
  + p-4 bg-blue; 
  &:hover { scale: 1.01; }
">
  {{content}}
</div>
```

### Level 3: Want scope styles globally?

Add $$ for global scope:
```html
\<div class="~$$button" _$$button="padding: 1rem; background: blue;">
  Click me
</div>
```
Now its reusable accross project.


### Level 4: What to group styles?

Add prefix as group identifier
```html
\<div class="~group$$button" group$$button="padding: 1rem; background: blue;">
  Click me
</div>
```
Autosuggestions collects these in to separate groups and make navigation easier.


### Level 5: Want to create varients?

Declare varients using attribute selectors like native CSS.
```html
\<div class="~L5$$button" varient-1 L5$$button="
    --bg-color: blue;
    padding: 1rem; 
    background: var(--bg-color);
    &[varient-1] { --bg-color: red; }
    &[varient-2] { --bg-color: green; }
" &="Add Comments like this.">
  Click me
</div>
```
Variables are exposed in tooltips for along with the comments, if hovered over it.


### Level 6: Extented styles later?

Extend using attribute selectors like native CSS.
```html
\<div class="~L5$$button L6$extend-localy" varient-3 L6$extend-locally="
    &[varient-3] { --bg-color: yellow; }
    &[varient-4] { --bg-color: cyan; }
">
  Click me
</div>
```
The exposed variables will assit in providing the contract by existing classes. 


### Level 7: Want to wrap you class in other selectors and Queries?

```html
\<div class="L7$style" L7$style="color: black;"
{@media (min-width: 620px)}&="color: red;"
>
  Click me
</div>
```
will be compiled to
```css
.L7$style {
    color: black
}

@media (min-width: 620px) {
    .L7$style {
        color: red;
    }
}
```

You can even chain multiple queries with:
    `{Query}&{.parent-class}&{[varient-state]}&="..."`
This replaces writing media queries and state control like theme-switching.

### Level 8: Need cascade control?
- `~` for utilities (basic)
- `+` for components (stricter overides)
- `=` for overrides (final overides)

Multiple declarations will be used for establish the organizaion of classes in while resolving inline classes. but it will help in the long run

### Level 9: Want to prevent Classname/ID leakage?

Use `<sketch> </sketch>` tag
```html
<!-- # will get replaced by a unique hash -->
<div id="_8j_8o_id" class="_8j_8o_class">...</div>
<script>
  // Reuse the hash id's by prefixing with "\#"
  const id = "_8j_8o_id"
  const classname = "_8j_8o_class"
</script>
```
*Needs configs to be properly configured*

### Level 10: Need to design components in Isolation?

Use `<sketch> </sketch>` tag
```html
\<sketch L10$preview>
    <div>
        <h1> Heading </h1>
        <p> {{contents}} </p>
        <button> Select </button>
    </div>
</sketch>
```
These components can be previewed in your editor webview, with live output


### Install and Setup

```bash
npm i -g alchira         # If you prefer npm
pnpm add -g alchira      # If you prefer pnpm
yarn global add alchira  # If you prefer yarn
bun add -g alchira       # If you prefer bun
```

**Alchira is Framework/language independent. Works in any codebase (uses Node for orchestration).**. 

[**Continue to Guide →**](https://github.com/alchira/package/wiki)
