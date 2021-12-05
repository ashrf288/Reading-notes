
## Dynamic Routes

```
import { useRouter } from 'next/router'

const Post = () => {
  const router = useRouter()
  const { pid } = router.query

  return <p>Post: {pid}</p>
}

{ "foo": "bar", "pid": "abc" }

export default Post

```

![](https://nextjs.org/static/images/learn/dynamic-routes/page-path-external-data.png)


In `idex.js` page:

```
import Link from 'next/link'


function Home() {
  return (
    <ul>
      <li>
        <Link href="/post/abc">
          <a>Go to pages/post/[pid].js</a>
        </Link>
      </li>
      <li>
        <Link href="/post/abc?foo=bar">
          <a>Also goes to pages/post/[pid].js</a>
        </Link>
      </li>
      <li>
        <Link href="/post/abc/a-comment">
          <a>Go to pages/post/[pid]/[comment].js</a>
        </Link>
      </li>
    </ul>
  )
}

export default Home
```

## Deploying Your Next.js App

### Deploy to Vercel

1. Create a Vercel Account
2. Import your nextjs-blog repository
