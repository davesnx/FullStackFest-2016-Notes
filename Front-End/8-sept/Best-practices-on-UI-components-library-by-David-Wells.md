# Best Practices on building a UI Component Library for your company by David Wells

### Q: What's the perfect scenario on the Front-End?

- Build one, use everywhere
- Organized
- Syncronized
- Self contained, isolated

--

### The problem?
Scalability accross a big company maintain all the perfect scenario values.

Example: React Components UI Architecture

--

### Design System (aka style guide)
Ref: [LightningDesignSystem.com](https://www.lightningdesignsystem.com) from SalesForce
Ref: [ux.mulesoft.com](http://ux.mulesoft.com)

### What contain a style guide
  - **Documentation** (not only page documentation, also inline code documentation)
  - **Live** code playground
  - **Usage** Examples
  - **Platform** guidelines

### How to build it
#### Breaking things down  
  Check visually on the UI/Mock which stuff do you have and you will see that
  Everything is a component

  Ref: Atom Design

  Anatomy of a Component: Screaming Architecture
  They create the site of serverless with **phenomic**
  Ref: [phenomic](https://github.com/MoOx/phenomic)

#### How to handle CSS?
  They use PostCSS and CSS Modules.
  Explain how CSS Modules works...

#### How to global assets like vars, mixins, icons, etc... (reset, normalize?)
  Don't use mixins or vars, just PostCSS powered by JS.

-

[@DavidWells](https://twitter.com/DavidWells)
