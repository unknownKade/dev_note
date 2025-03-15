 Software architecture style where the main concept is dependencies between components point inward towards domain objects. In hexagonal architecture Entity, Domain, UseCases reside in the core and expose ports as interfacess that adapters can be connected to to connect them to external sources.



## Domain
- can contain both state and behavior. the closer state is to behavior the better
- has no outward dependency
	- Single Responsibility Principle
	- provides an api for use cases to operate on them
	- is unaffected by other layers and evolves free of dependencies

## UseCases
- class for handling usecases of the application
- contains all business rule valdiations and logic specific to use case
- has no outward dependency and uses ports








# References
[Spring Java Hexagonal Architecture](https://reflectoring.io/spring-hexagonal/)