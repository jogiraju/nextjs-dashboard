## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

Source: https://nextjs.org/learn/dashboard-app/getting-started

npm install -g pnpm
npx create-next-app@latest nextjs-dashboard --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" --use-pnpm

cd nextjs-dashboard


    /app: Contains all the routes, components, and logic for your application, this is where you'll be mostly working from.
    /app/lib: Contains functions used in your application, such as reusable utility functions and data fetching functions.
    /app/ui: Contains all the UI components for your application, such as cards, tables, and forms. To save time, we've pre-styled these components for you.
    /public: Contains all the static assets for your application, such as images.
    Config Files: You'll also notice config files such as next.config.ts at the root of your application. Most of these files are created and pre-configured when you start a new project using create-next-app. You will not need to modify them in this course.

For this project, we've provided some placeholder data in app/lib/placeholder-data.ts. Each JavaScript object in the file represents a table in your database. 

In /app/lib/definitions.ts file, we manually define the types that will be returned from the database. 
If you're a TypeScript developer:

    We're manually declaring the data types, but for better type-safety, we recommend Prisma or Drizzle , which automatically generates types based on your database schema.
Next.js detects if your project uses TypeScript and automatically installs the necessary packages and configuration. Next.js also comes with a TypeScript plugin
for your code editor, to help with auto-completion and type-safety.

pnpm i
pnpm dev
Open http://localhost:3000
on your browser

How to add a global CSS file to your application.
Two different ways of styling: Tailwind and CSS modules.
How to conditionally add class names with the clsx utility package.

If you look inside the /app/ui folder, you'll see a file called global.css. You can import global.css in any component in your application, but it's usually good practice to add it to your top-level component. In Next.js, this is the root layout /app/layout.tsx file.

If you prefer writing traditional CSS rules or keeping your styles separate from your JSX - CSS Modules are a great alternative.

In addition to the approaches we've discussed, you can also style your Next.js application with:

    Sass which allows you to import .css and .scss files.
    CSS-in-JS libraries such as styled-jsx

, styled-components
, and emotion

One benefit of using layouts in Next.js is that on navigation, only the page components update while the layout won't re-render. This is called partial rendering which preserves client-side React state in the layout when transitioning between pages.

