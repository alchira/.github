# 3. Directory

## Setup folder
```
    xtyles/
    ├── libraries
    |   ├── _scaffold_
    |   |    └── *.css
    |   └── *.css
    ├── #at-rules.css
    ├── #constants.css
    ├── #elements.css
    ├── #extends.css
    ├── configure.jsonc
    ├── hashrules.jsonc
    └── vendors.jsonc
```

### `./#at-rules.css`
- Defines preface directives for exported stylesheets.
- Declares preface-level directives for exported stylesheets, such as `@import`, `@layer`, `@charset`, `@font-face` etc.

### `./#constants.css`
- Defines the core design tokens—colors, spacing, typography, and themes.
- Constants are context-aware and surfaced via LSP suggestions in valid scopes, enabling consistent styling.

> **Convention:**
> To prevent naming collisions and maintain clarity, all constants should follow the standard prefix format:  **`---{...}`**. This naming convention ensures safe resolution across files and avoids unintended conflicts in symbolic or dynamic contexts
---

### `./#elements.css`
- Encourages semantic usage of tags by styling native tags directly.
- Offers classless CSS that dynamically adapts to the design system defined in `constants.css`, promoting minimal markup and clean semantics.

### `./#extends.css`
- Augments the base CSS with additional declarations and overrides.
- Ideal for post-compilation definitions, utility extensions, and scoped enhancements that build on the compiled source stylesheet.

---
### `./configure.jsonc`

```json
{
  "vendors": "none",
  "proxymap": [
    {
      "source": "src",
      "target": "xrc",
      "stylesheet": "styles.css",
      "extensions": {
        "html": [
          "class"
        ]
      }
    }
  ],
  "environment": "browser",
}
```

- **`vendors`**  
    Specifies vendor prefixing behavior.  
    Accepts `"none"` or a list of vendor targets (e.g., `"webkit"`, `"moz"`).
- **`proxymap`**  
    Defines proxy compilation behavior for source-to-target transformation.
	- **`source`**  
	    Path to the original source directory containing raw project files.
	- **`target`**  
	    Proxy output directory. Acts as a working compilation target for the source folder.
	- **`stylesheet`**  
	    Stylesheet appended to the final compiled output. Located within the target directory.
	- **`extensions`**  
	    Maps file types to attributes where symbolic classes will be injected.  
	    Example: `"html": ["class"]` targets HTML files and assist merge tooltip via extension for given attributes.
- **`environment`**  
    Used by Editor extention for standerd css completion in compilation blocks.  
    Refer Extention walkthorugh to see in action at [../tutorial/0.extention.md](../tutorial/0.extention.md).

### `./hashrules.jsonc`

```json
{
  "-DesignApproach": "#{-MobileFirst}",
  // Values for #DesignApproach
  "-MobileFirst": "min-width",
  "-DesktopFirst": "max-width",  
  // @media standards
  "Ms4": "media@(#{-DesignApproach}:0320px)",
  "Ms3": "media@(#{-DesignApproach}:0384px)",
  "Ms2": "media@(#{-DesignApproach}:0448px)",
  "Ms1": "media@(#{-DesignApproach}:0512px)",
  "Mmd": "media@(#{-DesignApproach}:0640px)",
  "Ml1": "media@(#{-DesignApproach}:0768px)",
  "Ml2": "media@(#{-DesignApproach}:0896px)",
  "Ml3": "media@(#{-DesignApproach}:1024px)",
  "Ml4": "media@(#{-DesignApproach}:1152px)",
  // @container standards
  "Cs4": "container@(#{-DesignApproach}:160px)",
  "Cs3": "container@(#{-DesignApproach}:192px)",
  "Cs2": "container@(#{-DesignApproach}:224px)",
  "Cs1": "container@(#{-DesignApproach}:256px)",
  "Cmd": "container@(#{-DesignApproach}:320px)",
  "Cl1": "container@(#{-DesignApproach}:384px)",
  "Cl2": "container@(#{-DesignApproach}:449px)",
  "Cl3": "container@(#{-DesignApproach}:512px)",
  "Cl4": "container@(#{-DesignApproach}:576px)",
  // Global States
  "Load": "body[data-loading='true']"
}
```

- `hashrules` define reusable **wrapper-attribute-snippets** as key-value pairs, where keys are restricted to characters: `A–Z`, `a–z`, `0–9`, and `-`.
-  Support **recursive loading**, enabling inheritance across definitions.
- To use a `hashrules` in a script, use the `#{___}` within **wrapper-attribute** of a tag. The `hashrule` will only take effect if the tag already includes a declared style.
- If a recursion loop is detected due to conflicting shorthand definitions, those entries will be ignored during compilation, with errors.

> For clarity and conflict avoidance, any `hashrule` used as a variable should begin with a **`-` prefix**.

### `./vendors.jsonc`

- If `configure.jsonc | vendors: none` : Paste custom vendor data in this file
- If `configure.jsonc | vendors: {url}` has a valid URL source file will by automatically updated occasionally for vendor provider data.

### `./libraries`

- Organize classes into groups with up to 6 levels of inheritance based on existing classes.
- Details on managing libraries are covered in the next section.

### `./libraries/_scaffold_`

- This folder contains the immutable part of your library supplied by the initalized flavour.
- It includes static class sources used for symclass generation.
