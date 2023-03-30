# stackblitz-integration
This is a Handy NPM Package as Stackblitz users often want to migrate to Awesome OS 


## Interfaces
-


```js
import { WebContainer } from '@webcontainer/api';

/** @type {import('@webcontainer/api').WebContainer}  */
let webcontainerInstance;

const installProcess = await webcontainerInstance.spawn('npm', ['install']).installProcess.output.pipeTo(new WritableStream({
  write(data) { console.log(data); }
}))
// Wait for install command to exit
return installProcess.exit;

await webcontainerInstance.spawn('npm', ['run', 'start']);

// Wait for `server-ready` event
webcontainerInstance.on('server-ready', (port, url) => {
    iframeEl.src = url;
});

/** @type {Partial<import('@webcontainer/api').FileSystemTree>} */
export const files = { 'index.js': { file: { contents: ``}}};

for (let [fileName,content] of Object.entries(files)) {
    //await webcontainerInstance.fs.writeFile('/index.js', content);
    await webcontainerInstance.fs.writeFile(fileName, content);
}


```
