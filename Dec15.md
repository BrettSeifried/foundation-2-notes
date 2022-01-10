## Things to look up

    - depedency
    - props
    - useEffect
        - react takes the wheel and does a lot of things.
    - Fetch stuff
    -onChange={(e) => setRace(e.target.value)}
        - why is the e there? without e and => it will run on page load.

## Study over break

<a href="https://beta.reactjs.org/learn"> https://beta.reactjs.org/learn </a>

bbutton onClikc={handleClick}

- WAITS for button to be pushed
  button onClick={handleClick()}
- Runs the funciton when page loads.

# React ROuter - Kick ball manager

    - Detail Rotues
        - under <Switch>
    - Teams(books)
        - /teams/2 /teams/3
            - /teams/:id
                - gets put into a vairable, but always shows {team}
                <route path="/teams/:id" component: {team}>
                - info comes from views/teams/teasm.js
    - Players(characters)
        -/players
            -/players/:id
                -passes anything after : into a prop to see if it matches through (props.match.params.id)

### how to ask for a single team - servies(?)

    - pass in fetchTeamById(props.match.params.id)
        - fetchTeamById in SERVICES LAYER
            -fetchTeamById(id){
                const resp = await client.from('teams').select('*, players(*).match({ id }))
            return checkError(resp);
            }
        -client connect to SupaBAse, collect Team ID
        -select all columns and aossicated players
            - * = everything
            - players have a team_id, must match with team id.
        - match only give those back with this Id.
        -.match id matches team_id (from player) with id (team id)

#### views => teams (from database)

    - useffect, return what you want to display. link it to ${player.id}.
        - makes a link with that ID
        - <Link key={team.id} to={`/teams/${team.id}`}>
        {team.name}
        </Link>

    -  routes set up in App.js
        - " yeah I ahve a route for that!"
        - click a link, checks routes

### Route

    - App.js route <= views/team(s) <= servies/teams <= components/teams

    teams => teams:id

## Spotlight

/Books /Books:id
Route, HomePage, BookList(will need to turn those into Links.) - Route First - Create Links

# JUlie Picutrs

- APp.js - Router
  - views/Home.js, link to /books (catalog of books)
    -/books
    -/views/BookList.js
    -/books/1
    -/books/2
    -/books/:id
    /views/BookDetail.js

REACT_APP_SUPABASE_URL=https://jwkithqctyeqxnztsqjc.supabase.co
REACT_APP_SUPABASE_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyb2xlIjoiYW5vbiIsImlhdCI6MTYzNzcxNzEwMSwiZXhwIjoxOTUzMjkzMTAxfQ.HeNurSJnSyAk2ZZAejJhrc4QW0Fy_5VBQuTqDvaEdwE

1. add Router & Switch
   - make a home folder, Home.js
2. Add your links
