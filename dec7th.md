# general review

    * useState - react playground is a good place to practice
        * allows data that changes over time and stays insync with UX
        * View and state in sync
        const ... useState('what you want')
            * can change from function.
        *const [prop, setter] = useState('something you want')
        *onChange{(e) => setTer(e.target.value)}
        *hooks associated with functional components.
    * Idea of props (properties)
        * props how we pass informaiton to components
    * .map
        * const items = ['a', 'b', 'c']

        return(
            <div>
                {items.map((item) => (
                    <Detail key={item} text{item}>
                ))}
        )
    * destructure
        * Curly on left, = keys.
        * WIll look at Obj on the right. with that key
        * right side is the Obvj
    * How destructure works
        * const obj = {name: 'Benny', age: 7}
        * conat {name, age} = obj
        * Name (enter) returns Benny
    *App.js
        * set a component on a Route line will send everything as Props.
    * Connecting info from form to database
    * const myObj = {name, age} //= {name: name, age: age}
