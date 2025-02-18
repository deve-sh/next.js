# Invalid <Link> with <a> child

#### Why This Error Occurred

Starting with Next.js 13, `<Link>` renders as `<a>`, so attempting to use `<a>` as a child is invalid.

#### Possible Ways to Fix It

Run the `new-link` codemod to automatically upgrade previous versions of Next.js to the new `<Link>` usage:

```sh
npx @next/codemod new-link .
```

This will change `<Link><a id="link">Home<a></Link>` to `<Link id="link">Home</Link>`.

Alternatively, you can add the `legacyBehavior` prop `<Link legacyBehavior><a id="link">Home<a></Link>`.

### Useful Links

- [next/link](https://nextjs.org/docs/api-reference/next/link)
