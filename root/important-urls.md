const fs = require('fs');

const filePath = 'root/important-urls.md';

const fileDescriptor = fs.openSync(filePath, 'w');

const content = `# Important URLs\n\n* [Patcher Home](https://patcher.xyz/home)`;

fs.writeSync(fileDescriptor, content);

fs.closeSync(fileDescriptor);
