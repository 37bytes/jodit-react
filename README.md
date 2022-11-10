# [React Jodit WYSIWYG Editor](https://github.com/jodit/jodit-react) fork

React wrapper for [@37bytes/offer-builder-jodit-fork](https://github.com/37bytes/jodit/tree/offer-builder-jodit-fork), [jodit](https://xdsoft.net/jodit/) fork.

## Installation

```bash
npm install @37bytes/offer-builder-jodit-react-fork --save
```

## Update editor version
```bash
npm update @37bytes/offer-builder-jodit-react-fork
```

## Run demo
```bash
npm install --dev
npm run demo
```

and open
```
http://localhost:4000/
```

## Usage

### 1. Require and use Jodit-react component inside your application.

```jsx
import React, {useState, useRef, useMemo} from 'react';
import JoditEditor from "@37bytes/offer-builder-jodit-react-fork";

const Example = ({placeholder}) => {
	const editor = useRef(null)
	const [content, setContent] = useState('')

	const config = useMemo({
		readonly: false // all options from https://xdsoft.net/jodit/doc/,
		placeholder: placeholder || 'Start typings...'
	}, [placeholder])

	return (
            <JoditEditor
            	ref={editor}
                value={content}
                config={config}
		tabIndex={1} // tabIndex of textarea
		onBlur={newContent => setContent(newContent)} // preferred to use only this option to update the content for performance reasons
                onChange={newContent => {}}
            />
        );
}
```


License
-----
This package is available under `MIT` License.
