# react-start

## setup

> npx create-react-app <name>

## components

> We can create components, its same as html tags. We can use these components as per our needs ie they are reusable.
```
const About = () => {
  return (
    <div>
      <h1>This is about page</h1>
    </div>
  )
}

export default About;
```

> Now we can use the about About compnent in anu other componets like <About /> 

## Master page

> If we have some code that is common to all pages/componets like header and footer. Header and footer are common to all pages. So we need a master componet which have header and footer code. 
```
const Base = ({ title = "Welcome to website", children }) => {
  return (
    <div className="container-fluid">
      <h1> This is header </h1>
      
      { children }
      
      <h1> This is footer </h1>
    </div>
  )
}

export default Base;
```

> Now we can use this Base in other compnents ie About, Home etc like -
```
const About = () => {
  return (
    <Base>
      <h1> this is about page </h1>
    </Base>
  )
}

export default About;
```
