# Day-1 2022 Notes

- When doing routes. but home or '/" at the bottom, always looks for the first match from top to bottom.

* component equals renders that component, or list as a child.
* React Router has some great hooks to use.

```javascript
<Route path="/contact">
  <AllContacts />
  /// can add some extra properties on this. ie logged in vs not logged in users
  from the same route.
</Route>
```

## Kick Ball Notes

- const params = useParams()
  - use fetchTeamById(params.id) within useEffect;
    - replaces fetchTeamById(props.match.params.id)

## Moving to a new form

-

## Testing

- Writing tests forces you to make well written code.

* don't forget env.test.local
* const { contrainer } = render(<Team match{{ params: { id: 2} }} />);
  -     destructure                          manually giving props
* await screen.finByText('Stumptown Lumberjacks')
* MemoryRouter for the test enviroment, much like BrowserRouter
  - Don't need memory router if theres no links.
* initialEntries={['/teams/2']} is what the user will click.
