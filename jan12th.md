# add a feature on kick ball or simliar

    * All the code is there,
    * Main challenge is to create the database, add row level secruity, including policies, protect the routes
        * protect, if authenticated, then they can see the route,
        * not AUth, redirec to sign in page.

## Problem

    * can edit without being logged in
    * edit delete only if you are logged in.
        * Can't add a new team unless logged in

### Supa base

    * create a new project.
        8 enable row level security when creating a table.
        * Copy paste SQL into read me
            * read me 5th section "SQL editor"
        * TURN OFF EMAIL CONFIRMATION

    * UpDate/Delete from scratch. Auth/Not Auth tempalte
    * policies
        * people icon CLick on Auth -> policies,
        * RLS locks everything, opens up as you add policies.
        * Each Policy associated with an action
            *uid has to match user_id in the table

    * Creating our policies
        * Create from Template.
            *Use this Template. just says tru?e save policy
                * True means everyone can see it.
                * Try to edit unAuth, get a 404 error.

    * SUpabase people icon, policies
        * Who can use it.
        * Copy and paste Role in there from Readme into policies (update)
            * give it a name, describes waht the policy does.
                * Review and save
        * Can now add teams(?)

    * Delete
        * Policy, copy role=auth from Readme,
        * save it

### React for Deliverable.

    * after sign out, not see edit forms or teams.
    * redirect non AUTH to Sign In.
        * /new route.
            * using a render
                * another way to render out a specefic component with a specefic view
        * Redirect, renders component. usehistory goes back to a page.

    * optional protected route
        * 2nd row. far right.
        * Protected route used often.

### Look at deliverable

    * hide edit, delete, add team is for us to figure out
    *
