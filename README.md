![Image for short guide](https://source.unsplash.com/vkCyrRJsHss)

# About

1. This guide will show you how to setup NextJS in the shortest amount of time as possible so you can start getting into the meat of your code!

2. to clone this repo, you can go to:

- https://github.com/grokkingcoding/quickest-nextjs-setup-ever.git

# The Quickest NextJS Setup Guide

1. Go to the NextJS website and follow this the steps in this link: https://nextjs.org/learn/basics/create-nextjs-app/setup. Joke!

2. Ok, lets really get into it now!

3. Make sure you have node installed on your machine. In your terminal, run the following command:

```
node -v
```

If nodejs is not installed, you can go and download using this link: https://nodejs.org/en/download/

4. Install npx on your machine. Go to your Terminal and enter thw following command:

```
    npm i -g npx or sudo npm i -g npx
```

5. Go to your Desktop or anywhere you want to save your nextjs app folder

```
cd Desktop
```

6. Then run the following command in your terminal:

```
npx create-next-app replace-this-with-name-of-your-app
```

To make it clear if I wanted to create a nextJs app called youtube-clone, I would run this command:

```
npx create-next-app youtube-clone
```

7. Then go inside the app folder by:

```
cd name-of-your-app-folder
```

8. Then run:

```
npm run dev
```

9. the next few steps will focus on some quick changes to really set you up!

10. Go to the "pages" folder in your nextjs app directory

11. Open up the file called index.js NOT \_app.js

You should see something like this (may it may have changed by the time you read this!):

```
import Head from 'next/head'
import Image from 'next/image'
import styles from '../styles/Home.module.css'

export default function Home() {
  return (
    <div className={styles.container}>
      <Head>
        <title>Create Next App</title>
        <meta name="description" content="Generated by create next app" />
        <link rel="icon" href="/favicon.ico" />
      </Head>

      <main className={styles.main}>
        <h1 className={styles.title}>
          Welcome to <a href="https://nextjs.org">Next.js!</a>
        </h1>

        <p className={styles.description}>
          Get started by editing{' '}
          <code className={styles.code}>pages/index.js</code>
        </p>

        <div className={styles.grid}>
          <a href="https://nextjs.org/docs" className={styles.card}>
            <h2>Documentation &rarr;</h2>
            <p>Find in-depth information about Next.js features and API.</p>
          </a>

          <a href="https://nextjs.org/learn" className={styles.card}>
            <h2>Learn &rarr;</h2>
            <p>Learn about Next.js in an interactive course with quizzes!</p>
          </a>

          <a
            href="https://github.com/vercel/next.js/tree/master/examples"
            className={styles.card}
          >
            <h2>Examples &rarr;</h2>
            <p>Discover and deploy boilerplate example Next.js projects.</p>
          </a>

          <a
            href="https://vercel.com/new?utm_source=create-next-app&utm_medium=default-template&utm_campaign=create-next-app"
            className={styles.card}
          >
            <h2>Deploy &rarr;</h2>
            <p>
              Instantly deploy your Next.js site to a public URL with Vercel.
            </p>
          </a>
        </div>
      </main>

      <footer className={styles.footer}>
        <a
          href="https://vercel.com?utm_source=create-next-app&utm_medium=default-template&utm_campaign=create-next-app"
          target="_blank"
          rel="noopener noreferrer"
        >
          Powered by{' '}
          <span className={styles.logo}>
            <Image src="/vercel.svg" alt="Vercel Logo" width={72} height={16} />
          </span>
        </a>
      </footer>
    </div>
  )
}

```

12. Remove the default nextjs html and add in your own for testing.

So maybe you can try adding a <p> tag to include a paragraph and see how things look:

```
import Head from 'next/head'
import styles from '../styles/Home.module.css'

export default function Home() {
  return (
    <div className={styles.container}>

      <Head>
        <title>Create Next App</title>
        <link rel="icon" href="/favicon.ico" />
      </Head>

        <p>
            Modifying html in nextjs app to see how it looks!
        </p>
    </div>
  )
}
```

13. Next we are going to change how css structured in the nextjs app.

14. Go to public and add a css file called styles.css

15. Then go to \_app.js and import the styles.css you just created by including at the top of \_app.js this import statemen:

```
import '../public/styles.css'
```

Just a note if you are using npm bootstap, this is where you will import the bootstrap library too.

```
import 'bootstrap/dist/css/bootstrap.css'
```

16. Now your whole app can use the css from your styles.css and bootstrap.css

17. Delete the styles folder that was included by default when you created the nextjs app

18. Now go into index.js and remove the old styles code which looks like this:

```
import styles from '../styles/Home.module.css'
```

Now you need to remove the styling method that was used in the html from before:

so remove "styles.container"

```
<div className={styles.container}>
```

19. Now it is time to change the index.js file to index.jsx. You can do this by editing the extension to .jsx instead of .js. So your index.js file should look like this after:

```
index.jsx
```

20. So to sum up we changed how css was used in the app and changed .js files to .jsx files. That's it, you are ready to roll with nextjs!
