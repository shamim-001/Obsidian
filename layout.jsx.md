
```jsx
import "@styles/globals.css";

export const metadata = {
  title: "Promptopia",
  description: "Discover & Share AI Prompts",
};

const RootLayout = ({ children }) => (
  <html lang="en">
    <head>
      <meta charSet="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>{metadata.title}</title>
      <meta name="description" content={metadata.description} />
      {/* Additional meta tags, stylesheets, or scripts can be added here */}
    </head>
    <body>
      <div>
		{children}
      </div>
    </body>
  </html>
);

export default RootLayout;
```

