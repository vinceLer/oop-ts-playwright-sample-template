<div align="center">
    <h1>
        🎭 oop-ts-playwright-sample-template
    </h1>
</div>

# ⚙️ Dependencies

- @playwright/test: 1.56.1
- @types/node: 24.10.0


# 🛠️ Prerequisites 

Before getting started, make sure you have **Node.js** installed along with one of the following package managers:

- [pnpm](https://pnpm.io/)  
- [npm](https://www.npmjs.com/)

<br>

# ✨ Getting Started

## 📋 Clone the repository 

```bash
git clone https://github.com/vinceler/oop-ts-playwright-sample-template.git
cd oop-ts-playwright-sample-template
```

## 📦 Install dependencies 

Using pnpm:

```bash 
pnpm install
```

Or using npm:

```bash 
npm install
```

## 🚀 Run tests 

Using pnpm:

```bash 
pnpm exec playwright test
```

Or using npm:

```bash 
npx playwright test
```

## 🏗️ Architecture 

```bash
📦 oop-ts-playwright-sample-template/
├── 📁 common/                     # Shared resources and global data
│   └── 📁 data/                   # Common data, configuration files (CSV, JSON, etc.)
│       └── 📄 urls.ts
│
├── 📁 core/                       # Core framework logic
│   └── 📁 base/                   # Base classes setup
│       ├── 🧩 base-layout.ts      # Defines layout-level components or UI regions
│       ├── 🧩 base-locator.ts     # Generic locator definitions and helper methods
│       ├── 🧩 base-page.ts        # Base Page Object class (navigation, actions, common methods)
│       └── 🧩 base-ui.ts          # UI interactions and shared interface utilities
│
├── 📁 src/                        # Main project source code
│   ├── 📁 locators/               # Page Object locators and selectors
│   │   └── 📁 pages/              
│   └── 📁 pages                   # Page Object Model (POM) implementations
│
├── 📁 tests/                      # Automated test scripts and scenarios
│   └── 🧪 example.spec.ts
│
├── 📄 package.json                # Project metadata, dependencies, and npm/pnpm scripts
├── 📄 pnpm-workspaces.yaml        # pnpm monorepo workspace configuration
├── 📄 tsconfig.json               # TypeScript compiler options and build settings
├── 📄 .env                        # Environment variables (API keys, credentials, etc.)
├── 📄 .gitignore                  # Files and folders ignored by Git
└── 📄 README.md                   # Project documentation (you’re reading it!)
```

### 🧠 Legend

| Icon | Item | Description |
|:------|:------|:-------------|
| 📁 | Folder | Logical container for files |
| 📄 | File | Source or configuration file |
| 🧩 | Component | Reusable module or class |
| ⚙️ | Core/Base | Framework setup and shared logic |
| 📊 | Data | Shared configuration or test data |
| 🧭 | Locators | UI selectors for automation |
| 🧪 | Tests | Test scripts and cases |

---

### 🧰 Core Layer (`core/base/`)

This layer defines the **foundation of the automation framework**, providing reusable abstractions for consistency and maintainability.

| File | Description |
|:-------------------|:--------------------------------|
| **`base-layout.ts`** | Defines reusable layout structures and top-level UI regions (headers, sidebars, footers, etc.) for consistent page design. |
| **`base-locator.ts`** | Abstract base class for page locators. Manages the Playwright `Page` reference and provides a structure for caching reusable locators, promoting code reuse and maintainability across page objects. |
| **`base-page.ts`** | Base Page Object class. Centralizes navigation, waits, and shared browser actions to ensure consistent behavior across all pages. |
| **`base-ui.ts`** | Abstract base class for UI components. Manages a `Page` reference, resolves a `Locator` automatically, and provides a `raw` getter for reusable UI interactions. |

---

### 🔩 Root Configuration Files

| File | Purpose |
|:------|:---------|
| **`package.json`** | Defines dependencies, scripts, and metadata for npm/pnpm. |
| **`pnpm-workspaces.yaml`** | Configures workspace packages for pnpm monorepo setups. |
| **`tsconfig.json`** | TypeScript compiler options and path mappings. |
| **`.env`** | Secure environment variables. |
| **`.gitignore`** | Files and folders ignored by Git. |
| **`README.md`** | Main documentation. |

---

## ⚡ CLI Shortcuts

| Task | Script | Actual Command | Notes |
|:----------------------------|:-----------------|:-------------------------------------|:-------------------------------------------|
| **Run tests** | `pnpm test` | `pnpm exec playwright test` | Runs all tests using Playwright |
| **Run tests in debug mode** | `pnpm debug` | `pnpm exec playwright test --debug` | Launches tests in Playwright debug mode |
| **Open test report** | `pnpm report` | `pnpm exec playwright show-report` | Opens the HTML report, accessible at [http://localhost:9323](http://localhost:9323) |
