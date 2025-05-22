
---

<p align="center">
  <h1 align="center">🔒 ownersv2-obfuscator</h1>
  <p align="center">A lightweight npm package to obfuscate HTML with anti-debug protection 🚀</p>
  <p align="center">
    <a href="https://www.npmjs.com/package/ownersv2_obfuscator"><img src="https://img.shields.io/npm/v/obfuscate-html.svg?style=flat-square" alt="npm version"></a>
    <a href="https://github.com/haji-mix/ownersv2-obfuscator/blob/main/LICENSE"><img src="https://img.shields.io/npm/l/obfuscate-html.svg?style=flat-square" alt="License"></a>
    <a href="https://github.com/haji-mix/ownersv2-obfuscator"><img src="https://img.shields.io/github/stars/haji-mix/obfuscate-html?style=flat-square" alt="GitHub Stars"></a>
  </p>
</p>

---

## 🌟 Overview

`ownersv2-obfuscator` is a sleek, dependency-free package that obfuscates HTML content, embedding anti-debug protection to deter developer tools usage. Perfect for securing client-side HTML in Express.js applications. Supports CommonJS, ESM, and TypeScript! 🛠️

**GitHub**: [Kenneth Panio](https://github.com/haji-mix)  
**Repository**: [ownersv2-obfuscator](https://github.com/haji-mix/ownersv2-obfuscator)

---

## ✨ Features

- 🔐 **HTML Obfuscation**: Encodes HTML to make it harder to read or reverse-engineer.
- 🛡️ **Anti-Debug Protection**: Detects developer tools (e.g., F12, Ctrl+Shift+I) and triggers alerts or page reloads.
- 🔄 **Configurable Iterations**: Control obfuscation strength with multiple encoding passes.
- 📦 **Universal Support**: Works with CommonJS, ESM, and TypeScript.
- ⚡ **Lightweight**: No external dependencies.

---

## 📦 Installation

Get started in seconds:

```bash
npm install ownersv2-obfuscator
```

---

## 🚀 Usage in Express.js

Integrate `ownersv2-obfuscator` into your Express.js app to serve protected HTML. Below are examples for CommonJS, ESM, and TypeScript environments.

### 🧩 CommonJS Example

```javascript
const express = require('express');
const { obfuscate } = require('ownersv2-obfuscator');

const app = express();

app.get('/', (req, res) => {
  const html = '<h1>Hello, World!</h1><p>Secure this page!</p>';
  try {
    const obfuscatedHtml = obfuscate(html, 1); // 2 iterations for extra protection
    res.send(obfuscatedHtml);
  } catch (error) {
    res.status(500).send('Error obfuscating HTML');
  }
});

app.listen(3000, () => {
  console.log('Server live at http://localhost:3000 🌐');
});
```

### 📘 ESM Example

```javascript
import express from 'express';
import { obfuscate } from 'ownersv2-obfuscator';

const app = express();

app.get('/', (req, res) => {
  const html = '<h1>Hello, World!</h1><p>Secure this page!</p>';
  try {
    const obfuscatedHtml = obfuscate(html, 1); // 2 iterations for extra protection
    res.send(obfuscatedHtml);
  } catch (error) {
    res.status(500).send('Error obfuscating HTML');
  }
});

app.listen(3000, () => {
  console.log('Server live at http://localhost:3000 🌐');
});
```

### 🛠️ TypeScript Example

```typescript
import express from 'express';
import { obfuscate } from 'ownersv2-obfuscator';

const app = express();

app.get('/', (req, res) => {
  const html: string = '<h1>Hello, World!</h1><p>Secure this page!</p>';
  try {
    const obfuscatedHtml: string = obfuscate(html, 1); // 2 iterations for extra protection
    res.send(obfuscatedHtml);
  } catch (error) {
    res.status(500).send('Error obfuscating HTML');
  }
});

app.listen(3000, () => {
  console.log('Server live at http://localhost:3000 🌐');
});
```

---

## 📚 API

### `obfuscate(html: string, iterations?: number | string): string`

Obfuscates an HTML string with anti-debug protection.

- **Parameters**:
  - `html`: The HTML string to obfuscate (required, must be a string).
  - `iterations`: Number of obfuscation iterations (optional, defaults to 1). Accepts a number or string that parses to a positive integer.
- **Returns**: Obfuscated HTML string with embedded decoder and anti-debug scripts.
- **Throws**: Error if `html` is not a string.

**Example**:

```javascript
const { obfuscate } = require('ownersv2-obfuscator');
const html = '<h1>Hello, World!</h1>';
const obfuscated = obfuscate(html, 2);
console.log(obfuscated); // Obfuscated HTML with decoder and anti-debug scripts
```

---

## 💡 Notes

- **Anti-Debug Protection**: Blocks developer tools by triggering alerts and reloading the page if tools like DevTools or Eruda are detected.
- **Obfuscation Strength**: More `iterations` increase complexity but may slow performance. Recommended range: 1–3.
- **Security**: Provides basic obfuscation to deter casual inspection. Not a full security solution against determined attackers.
- **Input Validation**: Ensure `html` is a valid string to avoid errors.

---

## 🛠️ Development Setup

Try it locally:

1. Clone the repo:
   ```bash
   git clone https://github.com/haji-mix/ownersv2-obfuscator.git
   cd ownersv2-obfuscator
   ```

2. Install dependencies (only Express for examples):
   ```bash
   npm install express --save-dev
   ```

3. Run the example:
   ```bash
   node example/express-example.js
   ```

4. Open `http://localhost:3000` to see the obfuscated HTML in action! 🌐

---

## 🤝 Contributing

Love to see contributions! 🧑‍💻  
- Report issues or suggest features on [GitHub Issues](https://github.com/haji-mix/ownersv2-obfuscator/issues).
- Submit pull requests to [ownersv2-obfuscator](https://github.com/haji-mix/ownersv2-obfuscator).

---

## Author

GitHub: [Kenneth Panio](https://github.com/haji-mix)  
Feel free to connect, star the repo, or share feedback! 🌟

---

## 📜 License

[MIT](LICENSE)  
Built with 💖 for the web development community.

---
