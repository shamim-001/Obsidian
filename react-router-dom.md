#react-packages #react-router-dom 
[[react-router-dom - notes]]

```bash
npm install react-router-dom
```

![[Pasted image 20230813064730.png]]


at the top of App.jsx
```js
import {
  Route,
  Routes,
  Link
} from "react-router-dom";
```

```jsx
const App = () => {
return (
<Router>
	<div className="container">
	<Header />
	<Routes>
		<Route path="/" exact element={<NotesListPage />} />
	</Routes>
	</div>
</Router>
);
};
```