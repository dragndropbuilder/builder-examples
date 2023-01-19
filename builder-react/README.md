## Install via npm

Step 1: Install npm package
```
npm i @videostation/reportbuilder --save
```

Step 2: Load the library 
In App.js add the following
```
import '../node_modules/@videostation/reportbuilder/elements';
```

Step 3: Render the report builder component
In the template, `<div><vs-form-builder></vs-form-builder></div>`

 

Sample App.js file

```javascript
import React, { useEffect, useState } from 'react';

import './App.scss';

// load from node_modules
import '../node_modules/@videostation/reportbuilder/elements';

function App() {
  return (
    <div className="app">
      <div><b>React App</b></div>
      <div><vs-form-builder></vs-form-builder></div>
    </div>
  )
}

export default App;
```

## Install via CDN
Step 1: Create a file with the following JavaScript snippet to load the library from CDN

```javascript
const loadReportBuilder = (callback) => {
    const existingScript = document.getElementById('videoStationRB');
    if (!existingScript) {
        const script = document.createElement('script');
        script.src = 'https://unpkg.com/@videostation/reportbuilder@latest/elements.js';
        script.id = 'videoStationRB';
        document.body.appendChild(script);
        script.onload = () => { 
        if (callback) callback();
        };
    }
    if (existingScript && callback) callback();
    };
export default loadReportBuilder;
```
`Note: The file is named as LoadReportBuilder.js for the document purpose`

Step 2: Import loadReportBuilder in the component which will display Report builder
```
import loadReportBuilder from './LoadReportBuilder.js';
```

Step 3: Use State hook to check the load state
```javascript
const [loaded, setLoaded] = useState(false);
  useEffect(() => {
    loadReportBuilder(() => {
      setLoaded(true);
    });
  });
```
Step 4: Render the report builder component\
```
<div>{loaded ? <vs-form-builder></vs-form-builder> : ''}</div>
```

 

Sample App.js file
```
import React, { useEffect, useState } from 'react';

import './App.scss';

import loadReportBuilder from './LoadReportBuilder.js';

function App() {
 
  const [loaded, setLoaded] = useState(false);
  useEffect(() => {
    loadReportBuilder(() => {
      setLoaded(true);
    });
  });

  return (
    <div className="app">
      <div><b>React App</b></div>
      { showSelected ? <Selected /> : null }
      <div><vs-form-builder></vs-form-builder></div>
      <div>{loaded ? <vs-form-builder></vs-form-builder> : ''}</div>
    </div>
  )
}

export default App;
```
## Development

To get started:

```bash
$ npm install
```

To see the demo app, run:

```bash
$ npm start
```