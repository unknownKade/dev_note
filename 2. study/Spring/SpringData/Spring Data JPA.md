- On start-up Spring Data JPA creates the implementations of repository interfaces
- library
	- spring-data-jpa
	- spring-data-commons
- config
	- xml :``<jpa:repositories base-package = "">
	- java :``@Configurtion @EnableJPARepositories(basePackages= "")

[[Spring Data JpaRepository]]
[[Spring Data Web Support]]

- Why @Transactional(read only = true)? doesn't flush makes small perfomance enhance (Jpa book p682)[[Open Ends]]