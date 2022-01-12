# The Final week of Study

    * AUthencation, showing who you are. ie ID at a Bar.
        * consist of E-mail and Password
    Authorization
        * Where you are allowed to go.
        * What you are allowed to see.

    * Client => emailpassword => Server => token (wristband) back to client.
        *each new request sends up a token.

### Form

    * Form w/ E-mail and password to be sent to Supabase
        *Returns client with a token, which is stored in state.

## Supa Base

    * just get users in Supabase automatically.

### RLS

    * Puts ID on a person(?)

## SUpa BAse

    * Supabase website has sign up and sign in code in there.

# Project

    * servies and users already written for us. so YAY!
    * new difference is the cline.auth
        * built into Supabase
        * Return information on the user.

## Project

    */signup
        * Formw/ E-mail, Password, Submit
        * Keep track / STATE
            * E-mail & Password
        * EVENTS
            * onSubmit or onClick
    *<Auth> => <AuthForm>
        * AuthForm jsut taken email, password, eventHandler as props
    * <AuthForm> => <AuthView>
        *call signUpUser to superbase and return a token (into local storage)
    *Routes
        *2 links for sign in and sign up.
        * /SignIn
            * Display SignIn view
                * Calling <AUthForm>
                    *<AuthForm>
                        * Looks like forms with email, setEmail, password, setPassword, handleSubmit.
            * Add in State
                * const of email, set email, use state as empty string
                    * pass all of those into <AuthForm >
            * What to do when a user submits
                * const handle submit, and prevent default
                    * Call and await signInUser.
                        * Have email and apssword in state
                    * pass in E-mail and apssword into signInUser.
            * console log the data to make sure you are getting user information.
                * Network request in payload can see passed up e-mail and password.
                * respone is the access_token.
                * Tokens expire automatically when no request are being done.
            * Supabase checks for auth token in local storage to see if it's stillc atcive.
                * getUser Function
                * Check if a currently logged in user in local Storage.
                    * Apps.js
                     * const currentUser, setCurrentUser = useState(getUer())
                    * Default user to get User function.
                    * conosle log currentUser to see if Supabase knows if im logged in. look for role authenticated
        *once authenicated and logged in
            * Route  path "/"
                *{currentUser && <h1> I am signed in
                * {!current user && <h1> not signed in}
                * Delete local storage key under application to test log out before logout button is added.
            * App.js
                *add a try catch for signInUser(email,password)
                * const an error message state
                * pass errorMessage into AuthForm on APss.js and AuthForm.js


        * /SignUp
            * what is different.
            * Make a route for /signUp
                * pass in <SignUp />
                    * Copy and paste SignIn() to SignUp)
                        *SigninUser to signUpUser.
                        * MAgic Happens?????? and it works
            * Have a single Auth view.
                * AUth.js copy over signInUser
                    *Change funciton to Auth
                        * add a const [type, setType] to apps.JS
                            * useState('signin')
                            * Try
                                const resp =
                                    * type === 'singin' ?
                                    await signInUser(email, Password)
                                    :
                                    await signUpUser(email, password)
                    * how ot change setType.
            * Change form sing in to signup in auth.js
                * <h1> onclick  setType signin and onclick setType signup.
        *Turned 2 forms into one.\
            * class Active added auth.JS in setType. can now CSS it
            *import dynamicClasses for
                * left side is the state you want to set, right side is the thing it is.
                    * active: type === 'singin' OR 'signup'

## One single route, that shows 2 different things based on if you are logged in or logged out

    * When not lgoged in, see signIn or signUp
    * Once logged in, you see I am signed in.

### logout function

    * already written in users.js
    * App.js
        * const logoutUser = () =>
            await logout();
            setCurrentUser(null)
        * crabby hands and add button to current user&&
            * onClick=(logoutUser)

# Fom scratch

    * is-cmoplete check box
    *How to get user Id for to-do
        * User id = current user
            * client.auth.user().id
            client.from('todos').insert([{ task: task, user_id: clien.tauith.user().id }]); in todos.js
        * getUser client.auth.session

# Plan

    *signin and sign Up same as today
    * Simpler dog adoption
        * less fields
        * One page. where
            * simple list,
            * simple form to do
        * more complicated
            * additional to pass up user informaiton when making a dog
        * not current user, show AUth, can set auth component.
        * check componsnets in inspector for proper states
            * Each state detemines what function will be called.

# Next day notes

    * Allow react to change the state for us.
    * toggelCompleted is like updateDog
