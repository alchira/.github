
  <b>
    <p align="center">
      <a href="https://github.com/alchira/package/wiki">Get Started</a>
      &nbsp; · &nbsp;
      <a href="https://github.com/alchira/tutorial">Tutorial</a>
      &nbsp; · &nbsp;
      <a href="https://github.com/sponsors/yshelldev">Sponsor</a>
      &nbsp; · &nbsp;
      <a href="https://github.com/orgs/alchira/discussions">Discussions</a>
    </p>
  </b>


### Alchira: Start Simple, Scale When You Need


#### Level 1: Want to use Utility classes?

Use ~ to trigger class loading in place:
```html
<div class="~flex ~flex-col">
  Click me
</div>
```
Provided that these classes are either available in libraries, or defined atlease once.


#### Level 2: Just want create new style?

Add $ for local scope:
```html
<div class="~$button_lu" >
  Click me
</div>
```

That's it. Styles with structure. No separate CSS file.
Reusable in same file.
```html
<button class="~$button_lu">
```

#### Level 3: Want reusable components?

Add $$ for global scope:
```html
<div class="~$$button" >
  Click me
</div>
```
Now its reusable accross project.


#### Level 4: What to group styles?

Add prefix as group identifier
```html
<div class="~group$$button" >
  Click me
</div>
```
Autosuggestions collects these in to separate groups and make navigation easier.


#### Level 5: Want to create varients?

Declare varients using attribute selectors like native CSS.
```html
<div class="~L5$$button" varient-1  >
  Click me
</div>
```
Variables are exposed in tooltips for along with the comments, if hovered over it.


#### Level 6: Extented styles later?

Extend using attribute selectors like native CSS.
```html
<div class="~L5$$button L6$extend-localy" varient-3 >
  Click me
</div>
```
The exposed variables will assit in providing the contract by existing classes. 


#### Level 7: Want to wrap you class in other selectors and Queries?

```html
<div class="L7$style" 

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

#### Level 8: Need cascade control?
- `~` for utilities (basic)
- `+` for components (stricter overides)
- `=` for overrides (final overides)

Multiple declarations will be used for establish the oranizaion of classes in while resolving inline classes. but it will help in the long run

#### Level 9: Need to design components in Isolation?

Use `<sketch> </sketch>` tag
```html

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

#### 🚀 What ALCHIRA Delivers

![Preview](../assets/preview.gif)

- **Unified Syntax for CSS + HTML** — Structure and style in one place, no context-switching.  
- **Standardized Syntax for CSS Frameworks** — Consistent syntax whether you use built-in or external frameworks.  
- **Component‑First Design** — Scoped composition without JavaScript framework overhead.  
- **Designer‑Friendly Workflow** — Visual-first authoring that compiles to clean production code.  
- **Personalized Flavors** — Native support for CSS framework variants and custom styling systems.  
- **Scoped Classes by Default** — Automatic isolation for predictable, conflict-free styling.  
- **Compile‑Time Unique ID Hashing** — Locally unique identifiers for precise scoping.  
- **Inline Cascade Control** — Fine-grained style override control directly in markup.  
- **Adaptive CSS Framework** — A stylesheet system that scales and evolves alongside your project as it grows.
- **Live Component Preview** — Isolated component composition with real-time updates.  
- **Creative Toolbox Philosophy** — Not a framework, but a system that flexes around your workflow.


## 🚀 Missions & Feature Unlocks

Alchira is currently in a high-intensity stabilization phase.  
Before we initiate the next mission, we are refining the core engine.  
Our current priority is absolute stability: hunting down edge cases and hardening existing features to ensure a rock-solid foundation.

### 💖 [**Fuel the Mission: Sponsor on GitHub**](https://github.com/sponsors/yshelldev)
**Alchira is a 100% bootstrapped project.**  
During the preview period, your support unlocks amazing new capabilities for everyone! 🎉

> [!NOTE]
>
> <details>
> <summary>
> <b>Development Lifecycle</b>
> <br />
> We use a "Cold Forge" protocol: no new features are added until the current ones are stable.  
>
> New capabilities are unlocked by community funding. 
> 
> _(Expand to know more about feature release lifecycle.)_
> </summary>
> 
> | Phase | Status | Activity |
> | --- | --- | --- |
> | **1. Forge Stabilization** | 🛠️ **Active** | Hardening current features. No new additions allowed. |
> | **2. Target Declaration** | 📢 **Announced** | Bugs are cleared. The next **Funding Target** is revealed. |
> | **3. The Funding Cycle** | ⏳ **Waiting** | The community contributes to reach the financial milestone. |
> | **4. Feature Unleash** | 🔓 **Unlocked** | Target met. New features enter the **Insider Alpha**. |
> | **5. The Insider Loop** | 🧪 **Priority** | Previous funders get first access and priority support. |
> | **6. Public Shift** | 🌍 **Public** | Features move to a Public Beta for everyone. |
> 
> </details>

---

### 🌍 Public Beta 


<details>

<summary>
  <b>Mission 0: 🎁 Essentials</b>
  <br />
  Composing and Nesting, Inline cascade control, Variants, 1st Order Wrappers,
  Dependent tracking.
</summary>
<hr />

These features alone provide a CSS framework that grows alongside your project from Zero. This "Successful Fusion" is achieved through the following core pillars:

- **Composing & Nesting:** Define UI as a unified structural topology.
- **Inline Cascade Control:** Master the cascade with `~`, `+`, and `=` operators.
- **Variants:** Manage state and regional logic directly within the declaration.
- **1st Order Wrappers:** Responsive logic (@#Mmd / @#Cmd) integrated as primary intent.
- **Dependent Tracking:** Automated structural awareness to prevent stylesheet bloat.

![Preview](../assets/feature/0_essentials.gif)

</details>


> [!IMPORTANT]
> The next mission remains **Locked** until all open issues in the current Forge Stabilization phase have been resolved and the funding target is met.

---

### 🔒 Future Unlocks 

> _Expand accordian to see feature previews._


<details>

<summary>
  <b> Mission 1: 🖼 Sketchpad </b>
  <br />
  Sketchpad Instant Previews. Faster Workflows.
</summary>
<hr />

**Stop guessing and start seeing:** Sketchpad brings live previews directly into your editor or external browser.  
While the built-in toolkit is lean and focused, it is designed to be fully extensible—allowing you to rebuild or customize the interface to suit your specific architectural needs.

**Tailored to your stack:** Sketchpad comes bundled with your preferred flavor. Unlock additional flavors to unleash the full potential of your development environment and specialized toolsets.  
With instant server-side updates for every edit, your feedback loop is now instantaneous. Build faster, debug visually, and stay in the flow.

![Preview](../assets/feature/1_sketchpad.gif)

</details>


<details>

<summary>
  <b>Mission 2: 📜 Chained Wrappers & Hashrules + Denest</b>
  <br />
  Precise directives + conditional selectors + Better selector organizaion
</summary>
<hr />

**Denest:** Destructive Nesting is a dedicated operator designed to keep long-chained selectors organized. It's the ultimate CSS power-up for managing complex UI states without losing code clarity.

**Multilevel Rule Control:** Manage rule states with precision using multilevel wrapping. By centering logic around the symlink, you ensure your styles remain both powerful and predictable.

**Hashrules:** Reuse & Scale Stop repeating yourself. Configure reusable wrapper snippets in `hashrules.jsonc`.

  - **Standardize:** Define snippets in `./alchira/hashrules.jsonc`.
  - **Sync:** Update a single file to reflect changes across your entire project.

![Preview](../assets/feature/2_hashrules.gif)

</details>


<details>

<summary>
  <b>Mission 3: 📚 Libraries</b>
  <br />
    Automated Style-Symlinks for Rapid Composition.
</summary>
<hr />

**Centralized CSS Factories:** Bulk-generate class blocks in ./alchira/libraries. Each block is assigned a unique symlink handle, making global styles easy to track, manage, and scale.

**Preprocessor Friendly:** Start with the Essential symlinks bundled with your flavor, or unleash your own preprocessor to generate custom library sets on the fly.

**Deep Architecture:** Support for 6 levels of inheritance allows for highly structured design tokens. Use `@--apply`/`+` to merge these library foundations into final HTML component sketches for advanced state management.

![Preview](../assets/feature/3_libraries.gif)

</details>


<details>

<summary>
  <b>Mission 4: 🧩 Advanced Scope Control </b>
  <br />
  Unique IDs, Scoped Classes, and Local Styling.
</summary>
<hr />

**Better Organization:** Utilize local file-scoped symlinks to prevent naming collisions. Only export the symlinks required for the task, keeping your internal logic private.

**Collision-Free IDs:** Leverage unique file hashes to generate one-of-a-kind class names and IDs automatically.

**Sketch Compositions:** Effortlessly combine local styles into robust compositions while maintaining strict scope boundaries.

![Preview](../assets/feature/4_scope-ops.gif)

</details>


<details>

<summary>
  <b>Mission 5: 🍧 Flavours </b>
  <br />
  Build & share custom CSS frameworks on Alchira.
</summary>
<hr />

Unified rulesets for team-enforced styling systems. Create immutable libraries, extend Sketchpad features, and ship config blueprints.

- **Team Standards** → Enforce consistent practices across projects  
- **Immutable Libraries** → Lock core styles, extend safely  
- **Personalize Sketchpad** → Build custom UIs/workflows from your preferred tools  
- **Config Blueprints** → One-click project kickstarts  

[**Spin your flavor →**](https://github.com/alchira/scaffold)

</details>


---

### How it all came to be?



> <details>
>
> <summary>
> <b>Why another framework, you ask?...</b>
> <br /> Not a Css/Js framework. Actually not even a framework.
> </summary>
> <hr />
> So what is it then? It's a **major fix for a minor problem**.  
> A problem that always manages to get in the way and turn into a constant source of frustration. A worked on a few a landing pages in vanilla stack and it was not a very pleasent experience HTML/CSS context switching, cascade hell, scoping, style override, i hope i don't have to explain every one did went through those. 
> Then i tried a few frameworks astro, svelte and react(i might get a lot, of hate for this, but react never really got clicked for me). And in addtion to those framework, every time these problems were stacking up as they scale. 
>
> </details>

> <details>
>
> <summary> 
> <b>Then what is this THING really?...</b>  
> <br/>A little bit of this, a little bit of that — hard to sum up in one word.
> </summary>
> <hr/>
> That's the tricky part. It lives in this weird intersection between tools we already use.  
> It comes with a **macro system for XML/HTML-like syntax**, but instead of shipping with a mountain of prebuilt classes like typical CSS frameworks, it lets you start from zero — or bring your own if you prefer.
>
> There's a **standardized syntax** for CSS frameworks if you want it, and built-in **scoped classes**, **compile-time unique ID hashing**, and **inline cascade control**. It also offers a **CSS framework that grows and adapts with your project**, **multi-mode stylesheet generation**, and **isolated component composition with live previews**.
>
> It's not a framework in the traditional sense — more like a creative toolbox that bends around your workflow.
>
> </details>

> <details>
>
> <summary> 
> <b>When/Where should you use it?...</b>  
> <br/>Whenever you want. Wherever you want. You`re the cowboy in these wilds.
> </summary>
> <hr/>
> It comes with very few rules — and almost unlimited flexibility.  
> You can make things fast, break things faster, and fix them just as easily. That`s the fun part.  
> It`s meant to feel natural and forgiving — something that lets you explore, not restrict.
>
> Personally i used it even for **this** markdown file.
>
> </details>

> <details>
>
> <summary> 
> <b>As for how it ended up like this?...</b>  
> <br/>I was too dumb to learn too many things and hold them all together in my head.
> </summary>
> <hr/>
> I come from a mixed background — part electronics, part design — and somewhere along that path, I fell into web development.  
> Over time, I realized I didn't have the patience to deal with a dozen disconnected tools just to make one thing work. I wanted something simple: a tool that did what I needed, stayed out of my way, and gave me room to create freely.
>
> What began as a tiny npm package for CSS slowly grew past its limits — creeping into HTML and evolving into something more ambitious. But I knew where to stop.  
> My battlefield was clear enough: **HTML** and **CSS** — **structure**, **style**, and all the **chaos** that comes with it.
>
> </details>

