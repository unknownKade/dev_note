### Layered Architecture
Commonly used 3-tier layered architecture. The layers are usually decoupled using abstaraction and Dependency Injection.
- Presentation Layer : presents data to end-user
- Logic Layer : contains business logic
- Data : controls data persistence

### Domain Driven Design
Each domain is responsible for its own business logic. They are independent logic units that message each other to interact. Data should not move between each domain.
[[TIL_250227-kr DDD]]
### Hexagonal Architecture
Uses ports and adapters for interacting with the outside of the program.
- Port : custom interface to application. Ports remain the same regardless of what the external source is.
- Adapter : converts in and output of port to interact with external sources