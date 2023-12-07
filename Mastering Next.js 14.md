#nextjs-tutorial 
https://youtu.be/GowPe3iiqTs?list=PLqWpppPogrrrAX45apJf6igkMgP7cBIow

[[Nextjs Routing]]

# Layout
![[Pasted image 20231121144919.png]]

# generateMetadata
```jsx
import React, { useEffect } from "react";
import { useRouter } from "next/router";

const Post = ({ params }) => {
  const router = useRouter();

  useEffect(() => {
    if (params.id === "4") {
      router.push("/login");
    }
  }, [params.id, router]);

  return <div>Post {params.id}</div>;
};

export default Post;

export const generateMetadata = async ({ params }) => {
  return {
    title: params.id,
    description: `All about post ${params.id}`,
  };
};
```

# Backend with Nextjs
use `route.js` instead of `page.js` inside the `api` folder

# middleware
![[Pasted image 20231122080351.png]]
