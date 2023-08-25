#react-query

```jsx
import { useQuery } from "@tanstack/react-query";
import axios from "axios";

const Home = () => {
  const { data: catFact, refetch } = useQuery(["cat"], () => {
    return axios.get("https://catfact.ninja/fact").then((res) => res.data);
  });
```
