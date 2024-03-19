---
Type: Learning
Course: ZTM
---
Creating a react project
`npx create-next-app@latest`
## Alternative Creation 
`npm create vite@latest`
- Project Name
- React 
- JavaScript
`cd project-name`
`npm install`
`npm run dev`
## Deploying React App 
- [Deployment](https://create-react-app.dev/docs/deployment/#github-pages)
## Communication with DOM 
```jsx
import { createRoot } from 'react-dom/client';
const domNode = document.getElementById('root');
const root = createRoot(domNode);

root.render(<App />);
```

## Component Skeleton 
```jsx 
import React from "react";

const Rank = () => {
    return (
        <div>
        </div>
    );
}
export default Rank;
```
