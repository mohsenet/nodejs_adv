Node.js adventures


```bash
sudo apt update
sudo apt install nodejs npm
```

```bash
node -v
npm -v

npm install --verbose -g n8n

sudo npm uninstall -g n8n
```

---

```bash
mkdir is-core-example
cd is-core-example
npm init -y
```

```bash
npm install is-core-module
```

```javascript
const isCore = require('is-core-module');

// Test some module names
const modulesToTest = ['fs', 'path', 'http', 'express', 'lodash'];

modulesToTest.forEach(moduleName => {
  const result = isCore(moduleName);
  console.log(`Is '${moduleName}' a core module? ${result}`);
});

// You can also check for a specific Node.js version
console.log('\nChecking for Node.js v10:');
console.log('Is "util" core in v10?', isCore('util', { version: '10.0.0' }));
console.log('Is "worker_threads" core in v10?', isCore('worker_threads', { version: '10.0.0' }));
```

```bash
node test.js
```
