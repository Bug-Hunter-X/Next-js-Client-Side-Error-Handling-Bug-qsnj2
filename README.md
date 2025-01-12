# Next.js Client-Side Error Handling Bug

This repository demonstrates a common issue in Next.js applications: how to gracefully handle errors that occur on the client-side during navigation.  The `about.js` page intentionally throws an error.  This example shows how to improve error handling to prevent a broken user experience.

## Bug

When navigating to the `/about` page, an unhandled error is thrown.  Next.js's default error handling isn't sufficient for this scenario, resulting in a blank page or a console error, and not a user-friendly error page.

## Solution

The solution involves implementing custom error boundaries to catch errors within components and display a more informative error message to the user.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.
4. Navigate to `/about`.

You will see a blank page (or a console error) instead of a user-friendly error message.