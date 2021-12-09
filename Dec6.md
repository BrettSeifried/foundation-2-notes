# Notes for Dec 6

- Supabase Stuff

## Blog List deliverable

- blogCard.js rendering from here
- services => client.js

  - Add blogs.js

# Julies Help

1. Hook up supa abse

- add blogs.js in services directory
  - esport `getBlogs` funciton which calls supabase
  - _very_ simiilar to `getRestaurants` from the Demo
- in App.js - hookup supabase call to your component.
  - need to add `blogs` state using `useState`
  - use useEffect to call `getBlogs` when the page initially renders
  * set the repsonse from `getBlogs` as your `blogs` state
    - console.log to make sure supbase call is working.

3. DO stuff from last week.

- do the stuff form alst week
  - looop through the `blogs` state viarable and render a `<BlodCard>` compoinent for each item in blogs.
