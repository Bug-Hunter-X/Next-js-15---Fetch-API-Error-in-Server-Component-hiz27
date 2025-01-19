# Next.js 15 - Fetch API Error in Server Component

This repository demonstrates a common error encountered when using the Fetch API within server components in Next.js 15.  The issue arises because the serverless function environment of server components doesn't have direct access to the browser's Fetch API.

## Problem

The `pages/about.js` file attempts to fetch data from an API route (`/api/data`) using the `fetch` API.  This will result in an error during the server-side rendering process.

## Solution

The solution involves using a client component to handle the API call.  The `pages/aboutSolution.js` file provides a corrected implementation where the data fetching is delegated to a client component which can access the browser's `fetch` API.

## Setup

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.

Navigate to `/about` to see the original error and `/aboutsolution` to see the solution.