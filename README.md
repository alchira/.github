---
title: Getting Started
---

## Node Package

- Alchira is distributed via **npm**.
- Custom flavors created by independent developers are also published on npm.
- You can install an existing flavor for your project, or create a personal flavor and reuse it across projects.
- To start your own flavor, use the scaffold template: https://github.com/alchira/scaffold

### Core runtime (alchira)

- **Package:** [alchira](https://www.npmjs.com/package/alchira)
- Installs the appropriate core binary for your OS.
- Provides the CLI used to orchestrate flavors and run builds.

```bash
# Local Installation
npm install -g alchira
# Local Command Run
alchira {command}
al {command}

# Global Installation
npm install --save-dev alchira
# Global Command Run
npx alchira {command}
npx al {command}
```

### Flavored Template (@alchira/scaffold)

- **Link:** [@alchira/scaffold](https://www.npmjs.com/package/@alchira/scaffold)
- [alchira](#unflavoured-alchira) will be installed along with flavor and all the commands will work the same manner.
- To initialize flavour run

```bash
# Local Initialization
npx al init {flavor-package-name}

# Global Initialization
al init {flavor-package-name}
```

## Editor extension

- **VS Code:** [Marketplace](https://marketplace.visualstudio.com/items?itemName=yshelldev.alchira)
- **Open VSX:** [yshelldev.alchira-client](https://open-vsx.org/extension/yshelldev/alchira-client)
- Adds full language support and extra tooling for Alchira configured projects.
- Bundles an Alchira core, so no separate install is required for small workflows.
- Plug‑and‑play setup, ideal for trying Alchira or for small projects.

![Preview](./assets/preview.png)

---

> - **Continue with tutorial repo: `git clone https://github.com/alchira/tutorial.git`**  
>   *Tutorial repo contains the same documentation in a more interactive manner.*
