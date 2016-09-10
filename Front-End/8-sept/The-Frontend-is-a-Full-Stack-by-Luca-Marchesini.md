# The Frontend is a Full Stack by Luca Marchesini

### Layers of an Architecture
```
 ----------------------------------
|                UI                 |
 ----------------------------------
|            View Logic             |
 ----------------------------------
|           Business Logic          |
 ----------------------------------
|           ORM (kind of)           |
 ----------------------------------
|        Persistence (Database)     |
 ----------------------------------
```

At the begining the Web Pages were just so static, until the user interacts
with all the Views(UI). Even to Reload the page isn't a option.

- **1995** JavaScript was implemented and use it for do small operations
without reload the page.
That was the first purpose of this scripting language.

- **2005** The creaton of AJAX, creates the hability to not only not reaload the page and do some operations just load new data from that layer of persistence.

- **2010** All the "Frameworks" become so popular and useful. (Angular, Backbone, Ember, etc...)
  We realize that we could create not only static website, just create Applications with that. We take care about Developer Experience.

- **2013** WebComponents or Components. *React*, *Angular 2*, *Vue.js*, *Polymer* and *Cycle.js*
  We have some abstraction for the old-HTML code that we were use do to. The components also provides a easy API. to represent the properties or the state that the single piece of UI have to render.

- **Now** Offline website comes in, we trait the Web as a Native Application on your phone. Using *Push Notification*, *Camera API*, *etc.*
So we create the concept of **Progressive Web Applications**.

  Also caring about the Application State, that always was there, in the jQuery days we still add some class or toggle another one, depends on some interaction.

  Now just become so complex to still work like saving the state of your app in the DOM as a CSS Class or a data structure.

  React aims for manipulate the global State, and not directly in the DOM.

  Also even newer, appears some technologies (solutions) for manage the state, Flux or Redux are capable to manage the global State of your application in a One way data flow, that allows us to represent the data from our models in a proper way, and only update this global state by interaction that the users trigger on the View, and this view update the global State (sometimes called Store).

- **2015** Falcor or GraphQL comes to solve the problem with the REST or ORM to get all of this data that the views need from the Database.
  Falcor - Falcor-client or GraphQL - Relay, are thinked about the same pattern as React, so forget about the DOM, just prove the data and the next layer is the responsable to represent it, manage state, and all the stuff that the Persistence Layer doesn't care.

  Both are in the model of **Single Enpoint API**, you just request with a "complex"-query and they will return all your demands with a JSON.
