# star wars API

- APplication Program Interface

```jsx
function App() {
    const [films, setFilms] = useState([]); //Called states
    const [loading, setLoading] = useState(true)

  useEffect(() => {
    const fetchData = async () => {
      const resp = await fetch("https://swapi.dev/api/films");
      const data = await resp.json();
      setFilms(data.resutls); // Film data nested in results key
      console.log(resp);
    };
    fetchData();
  }, []);

  return (
      <div className="App">
      {!loading &&
        {films.map((film) => ()
            <p key={film.title}>{film.title}</p>
        ))}}
    </div>
  <div className="App"></div>;
}
```
