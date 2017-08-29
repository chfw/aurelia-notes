# Aurelia Plugin

A plugin is a modular code that can be independently configured and shared with
other projects.

## How to write a built-in aurelia plugin?

### Step 1

Create a new folder named "myplugin" and write up three files::

```
<template>
test.html
</template>
```

```
export class TestMe{
  contructor (){
    console.log("I am a test controller");
  }
}
```

```
import {Aurelia} from 'aurelia-framework';

export function configure(aurelia: Aurelia){
  aurelia.globalResources('./test');
}
```

### Step 2

In your main.ts, add

```
.plugin(PLATFORM.moduleName('oauth'))
```

### Step 3

In webpack.config.js, add

```
plugins: [
  new AureliaPlugin({
    includeSubModules: [
	  {moduleId: 'myplugin'}
	]
  }),..
  new ModuleDependenciesPlugin({
    'myplugin': ['./test']
  }),
```
