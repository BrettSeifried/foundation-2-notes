# Adding and editing stuff in Supabase

- When you want a shcange, look to services.
  - Services is for Supabase
    - One for update dog
    - Updated Dog - send the dog info to supabase to update the row
    - CreateDog send the dog info to supabase to create a new row
      - dog object {id:1, name 'benny', age: 6, image: 'https...', breed 'terrier'}
    - deleteDogById - tells supabase to delete row

## CRUD or editing

    * create /dogs/:id/edit as a router in Apps.js
    * rfc for react import at set up page. Created <DogEdit />
    *

## DogEdit

    ```javascript
    // import feetchDogById, useEffect, useState, DogForm

    export default funciton DogEdit() => {

        const [dog, setDog] = useState({});
        const params = useParams();

        useEffect(( => {
            const resp = await fetchdDogById(id);
            setDog(resp[0]);
        };
        fetchData()
    }, [params.id]);

    const updateDog(ket, value) => {
        dog[key] = value;
        //^^Update \/ Create a new Object so react will be happy and set in state.
        setDog({ ...dog });
    }

        return (
            <div>
                <h1>Edit Dog</h1>
                <DogForm {...dog} updateDog={updateDog}/>
                // check components to see if info is passed into DogForm props.
            <div>
        );
    }
    ```

## dogForm

    - Check Julie's code
        - use inputs, type, value, onchange, updateDog('name', e.target.value)

    - Look at blog elements, state and updater.

## Blogger

    - const and set for each column of the database
    - fetch data
    - pass all object props into DogForm
    - pass all down to the from as props.
    - put an updateDog in dogs.js
    - check Fetch
