# POC about FE for Myrmex 2

What are we looking for ? 

In the end, a browser only understands HTML, CSS and JS. What will make the difference is:
- our methodology
- the stack we use to produce those files
- the way we serve the information

For a POC about FE, let's assume the FE and the BE have to be decoupled which is a good practice when considering web-services.

## We need ... an easy way to request and to serve data.

Rest, Soap, Xml-Rpc, Corba, ... actually, we should decouple this as well.

## We need ... features

There are A LOT of frameworks out there. We must have:
- modularity
- mvc
- templating
- two-way data binding
- client/server handling
- security
- 3rd party libraries (charts, datatables, reporting)
- logging
- maintainable structure
- speed
- tests 
- documentation
- support

... and like to have:
- scaffolding
- mocking: services, resources
- intellisense

## We need ... to choose an architecture

In a decoupled architecture, there are 2 types of accessible servers: assets servers and web-services.

- **The web-services** give only the information, JSON, XML, ... based on a query. Those can require data from other web-services, authentication servers (LDAP, Active directory, ...) or proprietary systems like SAP.

- **The asset servers** give either static HTML, CSS, JS files to the browser or dynamically generated files based on requests he made himself to the web-services.

## And the challengers are

### GWT by Google

Not supported anymore. Last "stable" version is unstable. -> unreliable.

### Vaadin 

Based on GWT, won't evolve anymore. However, still a good transpiler to be considered.

### <strike>Backbone</strike>

Backbone is a library not a framework:
- frameworks are prescriptive and restrictive.
- libraries are focused and specific.

We want a framework because it constraints the developer to conventions which make the team-working easier in the end. Developing a framework based on libraries would be redundant and unmaintainable by a small team.

### AngularJS by Google

Main advantage: we know it, it is actively developed and maintained, a lot of libraries are available out there.
Testable, quite tough but testable. Meet all our requirements except one... being server agnostic.

### ReactJS by Facebook

Quite new, ReactJS is promising and must be tested

### EmberJS

URL oriented, nice usability but lacks flexibility.
