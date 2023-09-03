#nextjs #metadata
```ts
import type { Metadata } from "next";

export const generateMetadata = async ({
  params: { userId },
}: Params): Promise<Metadata> => {
  const userData: Promise<User> = getUser(userId);
  const user = await userData;

  return {
    title: user.name,
    description: `This is the page of ${user.name}`,
  };
};
```

