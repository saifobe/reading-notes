# React and Next.js

## Next.js
Next.js is a framework for React that allows us to do server-side rendering and static site generation. It also has a file-based routing system that allows us to create pages by simply creating a file. It also has a built-in API system that allows us to create API endpoints by simply creating a file. It also has a built-in CSS module system that allows us to create CSS modules by simply creating a file.

### Why Next.js?
We chose Next.js because it is a framework that allows us to do server-side rendering and static site generation. It also has a file-based routing system that allows us to create pages by simply creating a file. It also has a built-in API system that allows us to create API endpoints by simply creating a file. It also has a built-in CSS module system that allows us to create CSS modules by simply creating a file.

### How to use Next.js?
We can use Next.js by installing it with npm and then running the following command:

```
npm install next
```

### How to create a page?
We can create a page by creating a file with the name of the page and then adding the following code:

```
import React from 'react'
import Link from 'next/link'

const IndexPage = () => (
  <div>
    <h1>Index Page</h1>
    <Link href="/about">
      <a>About Page</a>
    </Link>
  </div>
)

export default IndexPage
```

### How to create an API endpoint?
We can create an API endpoint by creating a file with the name of the endpoint and then adding the following code:

```
import { NextApiRequest, NextApiResponse } from 'next'

export default (req: NextApiRequest, res: NextApiResponse) => {
  res.status(200).json({ name: 'John Doe' })
}
```

## React
React is a JavaScript library for building user interfaces. It is maintained by Facebook and a community of individual developers and companies. React can be used to build single-page applications and mobile applications. It is used by many popular websites including Facebook, Instagram, Netflix, and Airbnb.

### Why React?
The main reason we chose React is because it has a large community of developers and companies that use it. This means that there are many resources available for learning React and many libraries available for extending React. It also has a large ecosystem of tools that can be used with React such as Redux, React Router, and React Native.

### How to use React?
We can use React by installing it with npm and then running the following command:

```
npm install react
```

### How to create a component?
We can create a component by creating a file with the name of the component and then adding the following code:

```
import React from 'react'

const Button = () => (
  <button type="button">Click Me!</button>
)

export default Button
```

### How to create a stateful component?
We can create a stateful component by creating a file with the name of the component and then adding the following code:

```
import React, { useState } from 'react'

const Counter = () => {
  const [count, setCount] = useState(0)

  return (
    <div>
      <p>You clicked {count} times</p>
      <button type="button" onClick={() => setCount(count + 1)}>
        Click Me!
      </button>
    </div>
  )
}

export default Counter
```

## Things I want to know more about? I want to know more about Next.js and React.

