### Layered Architecture
Commonly used 3-tier layered architecture. The layers are usually decoupled using abstaraction and Dependency Injection.
- Presentation Layer : presents data 
- Logic Layer : contains business logic
- Data : data ling

### Domain Driven Design
Each domain is 
### Hexagonal Architecture
A clean architecture using ports and adapters for interacting with the outside of the program.
- Port : custom interface to application. Ports remain the same regardless of what the external source is.
- Adapter : converts in and output of port to interact with external sources