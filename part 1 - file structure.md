[Source Code](https://github1s.com/hiteshchoudhary/nextjs-fullstack-auth/)

# [MongoDB atlas](https://youtu.be/iPGXk-i-VYU?list=PLRAV69dS1uWR7KF-zV6YPYtKYEHENETyE&t=843)
- `Build a database` -> `create` -> `Database` tab -> `Network Access` 
  -> `add IP address` to `0.0.0.0/0` which means `accessible to everyone` -> `confirm` 
  -> `Database Access` tab -> `add new database user` -> 
  ![[Pasted image 20230903160457.png]]
  use `numbers & characters` for password
-> ![[Pasted image 20230903160551.png]]
-> `add user`

# [Creating a project](https://youtu.be/iPGXk-i-VYU?list=PLRAV69dS1uWR7KF-zV6YPYtKYEHENETyE&t=1053)
```
npx create-next-app@latest 
```
# packages for this tutorial
```
npm install -D tailwindcss postcss autoprefixer
```

```
npm i axios bcryptjs jsonwebtoken nodemailer react-hot-toast mongoose 
```

# [Database Connection](https://youtu.be/iPGXk-i-VYU?list=PLRAV69dS1uWR7KF-zV6YPYtKYEHENETyE&t=2100)
`.env` file
```
MONGO_URI = mongodb+srv://saswe:pass1234@cluster0.cjnuuzy.mongodb.net/
TOKEN_SECRET = nextjstest
DOMAIN = http://localhost:3000
```

`src/dbConfig/dbConfig.ts`:
```ts
import mongoose from 'mongoose';

export async function connect() {
    try {
        mongoose.connect(process.env.MONGO_URI!, {
            useNewUrlParser: true,
            useUnifiedTopology: true,
            useCreateIndex: true,
        });

        const connection = mongoose.connection;

        connection.on('connected', () => {
            console.log('MongoDB connected successfully');
        });

        connection.on('error', (err) => {
            console.error('MongoDB connection error. Please make sure MongoDB is running. ' + err);
            process.exit(1); // Exit the application on connection error
        });
    } catch (error) {
        console.error('Something went wrong!');
        console.error(error);
    }
}
```



-----------------------------------------------------


![[Pasted image 20230903154337.png]]

![[Pasted image 20230903154425.png]]

![[Pasted image 20230830093030.png]]

- The back-end part needs to inside of `api` folder

![[Pasted image 20230830133431.png]]
- `api` needs database connection



