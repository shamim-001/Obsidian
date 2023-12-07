#nextAuth 

[Start](https://youtu.be/gPQ9SD_qpuk?t=2)

-----------------------------------------------------


---------------------------------------
1. [[nextjs setup]] - Nextjs with shadcn/ui
2. Installation
```
npm install next-auth nodemailer
```

```
npm install @prisma/client @auth/prisma-adapter
npm install prisma --save-dev
npx prisma init
```
after creating schema
```bash
npx prisma generate
```

```bash
npx prisma db push
```

3. 
`app/api/auth/[...nextauth]/route.ts`
```ts
import { authOptions } from "@/app/utils/auth";
import NextAuth from "next-auth/next";
const handler = NextAuth(authOptions);
export { handler as GET, handler as POST };
```
`app/utils/auth.ts`
```ts
import type { NextAuthOptions } from "next-auth";
import GitHubProvider from "next-auth/providers/github";
import EmailProvider from "next-auth/providers/email";
import { PrismaAdapter } from "@auth/prisma-adapter";
import prisma from "./db";

export const authOptions: NextAuthOptions = {
  adapter: PrismaAdapter(prisma),
  providers: [
    GitHubProvider({
      clientId: process.env.GITHUB_ID as string,
      clientSecret: process.env.GITHUB_SECRET as string,
    }),
    EmailProvider({
      server: {
        host: process.env.EMAIL_SERVER_HOST!,
        port: parseInt(process.env.EMAIL_SERVER_PORT!),
        auth: {
          user: process.env.EMAIL_SERVER_USER!,
          pass: process.env.EMAIL_SERVER_PASSWORD!,
        },
      },
      from: process.env.EMAIL_FROM!,
    }),
  ],
};
```
`app/utils/db.ts`
```ts
import { PrismaClient } from "@prisma/client";

const prismaClientSingleton = (): PrismaClient => {
  return new PrismaClient();
};

declare global {
  var prisma: PrismaClient | undefined;
}

const prisma = globalThis.prisma ?? prismaClientSingleton();

export default prisma;

if (process.env.NODE_ENV !== "production") globalThis.prisma = prisma;

```
`.env`
```
EMAIL_SERVER_USER=username
EMAIL_SERVER_PASSWORD=password
EMAIL_SERVER_HOST=smtp.example.com
EMAIL_SERVER_PORT=587
EMAIL_FROM=noreply@example.com
```
use resend for email service
`components/auth/NextAuthProvider.tsx`
```ts
"use client";
import { SessionProvider } from "next-auth/react";
import React, { ReactNode } from "react";

const NextAuthProvider = ({ children }: { children: ReactNode }) => {
  return <SessionProvider>{children}</SessionProvider>;
};

export default NextAuthProvider;

```

`layout.tsx`
```ts
<html lang="en">
  <body className={inter.className}>
    <NextAuthProvider>{children}</NextAuthProvider>
  </body>
</html>
```
