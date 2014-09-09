# Scaling

> "The secret to building large apps is never build large apps. Break your applications into small pieces. Then, assemble those testable, bite-sized pieces into your big application" -

Justin Meyer, author JavaScriptMVC

## Definitions
> Scalability is the ability of a system, network, or process to handle a growing amount of work in a capable manner or its ability to be enlarged to accommodate that growth

Source: [Wikipedia](http://en.wikipedia.org/wiki/Scalability)

## Scalable JavaScript Application Architecture
[Slides by Nicolas C. Zakas](http://www.slideshare.net/nzakas/scalable-javascript-application-architecture)

### Presentation Key Points
- MVC
- Website is broken down into modules
- A web application module is an independent unit of functionality that is part of the total structure of a web application
- Web application modules consist of HTML + CSS + JavaScript
- A single modules should be able to live on its own
- Modules are looesely coupled. Changes to a module do not affect other modules.
- Each module has its sandbox
- Architecture: Modules -> Sandbox -> Application Core -> Base Library (Slide 108)
- Module rules
  + Only call own methods or sandbox methods
  + Only access DOM elements in the context of your module
  + Don't access non-native global objects
  + Anything else needed is requested through the sandbox
  + Don't create global objects
  + Don't talk to strangers
- The Sandbox
  + The sandbox ensures a consistent interface
  + Modules only know the sandbox
  + Jobs: Consistency, Security, Communication
- The Application Core
  + Manages modules
  + It's the application controller
  + Jobs
    * Manage module lifecycle
    * Enable inter-module communication
    * Error handling
    * To be extensible

Source: http://www.slideshare.net/nzakas/scalable-javascript-application-architecture

## CSS
Use a preprocessor such as SCSS (SASS), LESS or Stylus.




