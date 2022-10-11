# Next.js & Contentlayer starter

This is a minimal Next.js & Contentlayer starter that comes configured with MDX support, code highlighting, and tailwind css.

[Demo](https://contentlayer-starter.vercel.app/)

## Getting Started

Clone this repository and install all dependencies

```bash
git clone https://github.com/achintyajha/contentlayer-next-mdx-starter/ my-blog
npm i
```

That's it! To create new posts, head over to the content/blog folder and create new MDX files. The name of the file is used for generating the slug while the frontmatter is used for adding the date, title, and description.

## Using custom components

To use your own components in your MDX files, import them to the pages/blog/[slug].tsx page, and add them to the `MDXcomponents` variable. To give custom name aliases to these components use the following syntax - 

```js
// pages/blog/[slug].tsx
import Image from "next/image"

const MDXcomponents = {
  // Pass Custom Components here (for use in markdown files)
  img: Image,
};
```

See more in the [Contentlayer docs](https://www.contentlayer.dev/docs/reference/next-contentlayer#usemdxcomponent)

## Custom Page Types

To create other page types, define them in the contentlayer.config.ts file, just like the `Post` type has been defined. Create a corresponding index and slug page for the type in `pages` directory.
