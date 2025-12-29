
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


![Banner](../assets/banner.png)

"Do you see it, Edward? Look closely at the stream. For decades, they told us these two souls—HTML and CSS—must live in separate vessels. They called it 'separation of concerns.' I call it a tragedy of fragmentation.

But look now... there is no 'link' tag. There is no 'external stylesheet.' I have spliced the DNA of the structure directly into the spirit of the style. They are no longer two things pretending to be one; they are a Successful Fusion.

It's stable, Edward. It's declarative. It's... beautiful. We've created a Chimera that doesn't just bark—it renders."

### Install and Setup

Alchira works independently of frameworks or languages. npm provides convenient distribution (most frontend devs have Node), but functions perfectly in any non-Node codebase.

```bash
    npm i -g alchira
```

Alternatively you can still use your preffered package manager(pnpm/yarn/bun).

```bash
pnpm add -g alchira
yarn global add alchira
bun add -g alchira
```

[**Continue →**](https://github.com/alchira/package/wiki)

#### 🚀 What ALCHIRA Delivers

![Preview](../assets/preview.png)

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


## Features

> [!NOTE]  
> ### 💖 [**Sponsor Project & Support Development**](https://github.com/sponsors/yshelldev)
> **Alchira is 100% bootstrapped.** 
> In the preview period . Your sponsorship unlocks new features for the entire community as milestones are reached.
> 
> 🌱 [**Become Supporter: $5**](https://github.com/sponsors/yshelldev)  
> 🚀 [**Become Believer: $20**](https://github.com/sponsors/yshelldev)  
> 🔥 [**Become Backer: $80**](https://github.com/sponsors/yshelldev)  
> 💎 [**Become Patron: $250**](https://github.com/sponsors/yshelldev)  
> ✨ [**Custom Amount: $$$**](https://github.com/sponsors/yshelldev)

---

### ✅ Available 


<details>

<summary>
  <b>Mission 0: 🎁 Essentials</b>
  <br />
  Composing and Nesting, Inline cascade control, Variants, 1st Order Wrappers,
  Dependent tracking.
</summary>
<hr />

**Details:**  
These feature alone gives you the a CSS framework that work along side your project starting from Zero.

**Preview:**

```html
<!-- Compose -->


<!-- Usage -->
<button class="~demo$button_kW">
  <span> Click Me </span>
</button>
```

</details>

<img src="../assets/button.png" alt="Description" height="32rem">

---

### ⏳ Next Mission: 

> Unlocks once all previous issues have been resolved.


<details>

<summary>
  <b>Mission 1: 📜 Chained Wrappers, Hashrules</b>
  <br />
  Precise directives + conditional selectors
</summary>
<hr />
**Details:** Composes classes at compile-time with variant extensions. These
feature alone gives you the a CSS framework that work along side your project
starting from Zero. Compound selectors with stateful directives and wrappers.

**Preview:** `<div class="btn ~primary ~hover ~lg">Click</div>`

</details>



---

### 🔒 Future Unlocks


<details>

<summary>
  <b>Mission 2: 📚 Libraries</b>
  <br />
    Create reusable library-style symlinks for quick composition and reuse.
</summary>
<hr />
**Details:**  
Preserve preset symlinks for reuse while composing classes and loading classes with existing symlinks. This unlocks a familiar workflow similar to CSS frameworks and other tooling.
</details>


<details>

<summary>
  <b>Mission 3: 🧩 Scope Control</b>
  <br />
  Unique IDs + destructuring for state composition
</summary>
<hr />

**Preview:** `~user#avatar ~active` → `.u1234_user_avatar.is_active`  
**Details:** Compile-time scoped IDs with nested state flattening.

</details>


<details>

<summary>
  <b>Mission 4: 📦 Sketchpad</b>
  <br />
  Live previews
</summary>
<hr />

**Preview:** Drag/drop components with real-time rendering
**Details:** Visual composition workspace with cross-project templates.

</details>


<details>

<summary>
  <b>Mission 5: 🍧 Flavours </b>
  <br />
  Customize personalized CSS frameworks & shareable flavours
</summary>
<hr />

**Preview:** `~tailwind ~bootstrap ~custom-brand`
**Details:** Unified rulesets for frameworks built on ALCHIRA. Create/share personalized CSS ecosystems.

</details>


---

### How it all came to be?



> <details>
> <summary>
> <b>Why another framework, you ask?...</b>
> <br /> Not a Css/Js framework. Actually not even a framewwork.
> </summary>
> <hr />
> So what is it then? It's a **major fix for a minor problem**. A problem that
> always manages to get in the way and turn into a constant source of
> frustration. A worked on a few a landing pages in vanilla stack and it was
> not a very pleasent experience HTML/CSS context switching, cascade hell,
> scoping, style override, i hope i don't have to explain every one did went
> through those. Then i tried a few frameworks astro, svelte and react(i might
> get a lot, of hate for this, but it never really got clicked for me). Then i
> tried a few frameworks astro, svelte and react(i might get a lot, of hate
> for this, but it never really got clicked for me). And in addtion to those
> framework, every time these problems were stacking up as they scale.
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
> There's a **standerdized syntax** for CSS frameworks if you want it, and built-in **scoped classes**, **compile-time unique ID hashing**, and **inline cascade control**. It also offers a **CSS framework that grows and adapts with your project**, **multi-mode stylesheet generation**, and **isolated component composition with live previews**.
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

