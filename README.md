# React Router Dom Catch-All Route Issue

This repository demonstrates a subtle issue with React Router Dom's catch-all route (`path="/*"`).  When navigating to any route other than the explicitly defined routes, the catch-all route should display a 404 Not Found message.  However, in certain cases, it can lead to unexpected behavior.

## The Issue
The issue arises when you have a specific route defined *before* the catch-all route that could potentially overlap (due to nested routes). This example uses a simple scenario with only two routes: one for the homepage and one for the about page.  The problem occurs when an invalid route is accessed, as it doesn't always correctly fall into the catch-all route.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to a route that doesn't exist (e.g., `/invalid-route`).

You might find that the catch-all route may not trigger correctly.