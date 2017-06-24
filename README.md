##### About
Sample application showcasing redux and polymer 2.0.

there are 3 routes which share a redux store containing a friends list, a username and a loading state. 

Add your own Friend provides an input field to quickly add a name to the friends list and displays the list of friends.

Add a stranger uses an action register from the redux store to fetch a random user from the randomuser.me api.  while fetch is working, the state.loading will be set to true until the promise is resolved, after which time the state.username will get updated and pushed to the friends list, which will be updated in the other Views.

View your list of friends displays only the list of friends

##### Get Started

Once project is cloned, simply run 'npm run doit' to get the application up and running.

Bower will need to resolve some version issues, just answer 2 if prompted.

### Start the development server

This command serves the app at `http://localhost:8080` and provides basic URL
routing for the app:

    polymer serve

### Build

This command performs HTML, CSS, and JS minification on the application
dependencies, and generates a service-worker.js file with code to pre-cache the
dependencies based on the entrypoint and fragments specified in `polymer.json`.
The minified files are output to the `build/unbundled` folder, and are suitable
for serving from a HTTP/2+Push compatible server.

In addition the command also creates a fallback `build/bundled` folder,
generated using fragment bundling, suitable for serving from non
H2/push-compatible servers or to clients that do not support H2/Push.

    polymer build