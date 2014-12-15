# POC about FE for Myrmex 2

What are we looking for ? 

In the end, a browser only understands HTML, CSS and JS. What will make the difference is:
- our methodology
- the stack we use to produce those files
- the way we serve the information

For a POC about FE, let's assume the FE and the BE have to be decoupled which is a good practice when considering web-services.

## We need ... an easy way to request and to serve data.

Rest, Soap, Xml-Rpc, Corba, ... actually, we should decouple this as well.

## We need ... to find what we need

There are A LOT of frameworks out there. We must have:
- modularity
- templating
- two-way data binding
- client/server handling
- security
- libraries (charts, datatables, reporting)
- logging
- maintainable structure
- speed
- tests 

... and like to have:
- scaffolding
- mocking: services, resources

## We need to choose an architecture

In a decoupled architecture, there are 2 types of accessible servers: assets servers and web-services.

- **The web-services** give only the information, JSON, XML, ... based on a query. Those can require data from other web-services, authentication servers (LDAP, Active directory, ...) or proprietary systems like SAP.

- **The asset servers** give either static HTML, CSS, JS files to the browser or dynamically generated files based on requests he made himself to the web-services.

