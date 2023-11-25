# router-context (in development)
## In the future: idiomatic, lightweight, extensible router for React applications.
## Right now: Very lightweight, non-extensible, useless to everyone but me

`<Router Provider declaredRoutes={routes} injectIndex={1} defaultPath={'/signin'}`  
&nbsp;&nbsp;`<Header />`  
&nbsp;&nbsp;`<Footer />`  
`</RouterProvider>`

In the above code, the component to be rendered at "/signin" will be injected between \<Header /> and \<Footer />. "routes" is an array of Routes. Instantiating this array effectively "registers" routes to be navigated too within the router context. Those routes might look like this:

`import SignIn from "./components/SignIn"`  
`import Home from "./components/Home"`  
`import type { Route } from './context/RouterContext'`    

`const routes: Route[] = [`  
&nbsp;&nbsp;`{`  
&nbsp;&nbsp;&nbsp;&nbsp;`path: "/signin",`  
&nbsp;&nbsp;`    component: SignIn`  
&nbsp;&nbsp;`},`  
&nbsp;&nbsp;`{`  
&nbsp;&nbsp;&nbsp;&nbsp;`path: "/home",`  
&nbsp;&nbsp;&nbsp;&nbsp;`component: Home`  
&nbsp;&nbsp;`}`  
`]`  
