```javascript
function App() {
  const [pokemon, setPokemon] = useState([]);
  const [loading, setLoading] = useState(true); // 2nd part
  useEffect(() => {
    const fetchData = async () => {
      const resp = await fetch("URL");
      const data = await resp.json();
      console.log(data);
      setPokemon(data.results); //2nd part
      setTimeout(() = > { //extra stuff
          setLoading(false);
      } 2000);
      })
    };
    fetchData();
  }, []);
  return (
    <div className="app">
      {loading && <h1>LOADING!</h1>}
    //   {loading && <span className="loader"></span>}
      {!loading && pokemon.map((poke) => <p key={poke.id}>{poke.pokemon}</p>)}
    </div>
  );
}
```

<th>

## Back from Break

- pokemon.js

```javascript
esport async function getPOkemon() {
    const resp = await fetch('URL');
    const data = await resp.json();
    return data;
}
```

```javascript
// function App() {
//   const [pokemon, setPokemon] = useState([]);
//   const [loading, setLoading] = useState(true); // 2nd part
//   useEffect(() => {
//     const fetchData = async () => {
//       const resp = await fetch("URL");
//       const data = await resp.json();
    'Replace above with a getPokemon Function'
//       console.log(data);
//       setPokemon(data.results); //2nd part
//       setTimeout(() = > { //extra stuff
//           setLoading(false);
//       } 2000);
//       })
//     };
//     fetchData();
//   }, []);
//   return (
//     <div className="app">
<h1> Pokedex </h1>
//       {loading && <h1>LOADING!</h1>}
//     //   {loading && <span className="loader"></span>}
//       {!loading && pokemon.map((poke) => <p key={poke.id}>{poke.pokemon}</p>)}
Repalced by Below code
    'Replace above with a PokeList function'
      {!loading &&
      <>
        <Controls />
        <PokeList pokemon={pokemon} />
    </>
//     </div>
//   );
// }
```

- componenets
  - controls
  * PokeList.js
  * setLoading
    - ADd 'if (loading) { fetch(data): }
      - add loading after fetchData in App.js

* ## ADd arugemnt to pokemon
  - Url search aprams to pokemon.js
    - const params = new URLSearchPArams();
    - params.set('pokemon', query);
* params added to URL (const = resp) string

```javascript
export default funciton Controls ({ query, setQuery, setLoading }) {
    return (
        <div>
            <input
            type="text"
            placeholder="Search Pokemon"
            value={query}
            onChange={(e) => {
                setQuery(e.target.value);
            }}
            />
            <button onClick={e => setLoading(true)}>Search</button>
        </div>

    )
}
```

```javascript
const [query, setQuery] = useState("");
```
