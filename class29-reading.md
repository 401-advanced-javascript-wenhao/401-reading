# Reading 29 - Component Composition - 5/21/2020

## Routing
* `react-router` - toggle the visibility of components or pages based on the URL/Route that the user engages with
* `Browser Router` - it is a provider 
  * use `<Link>` or `<NavLink>` to link specific URL/Route
  * `<Link to="/">Home</Link>` <=> `<Route exact path="/" component={Home} />`

## Component Composition - Logical
* Send child components the raw data and allowing them to render the output as they decide

## Component Composition - Using Logic-less Children  
* `children` are already in JSX form
* Need to display `children` as a whole 
```javascript
<Results>
  { listings.map(listing => /*do something*/)}
</Results>
```