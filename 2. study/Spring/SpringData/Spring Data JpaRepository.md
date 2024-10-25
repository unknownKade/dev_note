SpringData : PagingAndSortingRepository -> CrudRepository -> Repository
Spring Data Jpa : JpaRepository -> PagingAndSortingRepository
#### Query
- Method Query
	- Query
- Query Method 
	- @Query in repository
	- `` @Query("select m from Member where m.username = :username or m.id = ?1)
	- @Param("variable-name") when parameter name is different from variable name
	- ?n for parameter based on location
- Named Query
	- @NamedQuery(name ="", query ="") on entity
- Query Hints
- Bulk
	- executeUpdate()
	- @Modifying
		- (clearAutomatically = true) to clear persistence context after bulk query
#### Specification
- Specifation uses composite patterns to predicate
	- where(), and(), or(), not()
	- ``List<Member> result = memberREpository.findAll(where(memberName(name)).and(isUsed()))
- JPASpecificationExecutor
	- Using executor make specifications for JPA criteria
	- ``public interface MemberRepository extends JpaRepository<Member, Long>, JpaSpecificationExecutor<Member>{}
- implementation sample jpa book p 570[[Open Ends]]
#### Persistence
- save() method
	- when id is null Hibernate used to return an error but JPA will create a new entity
	- if id exists, JPA uses persist() interface- which uses EntityManager.merge() underneath
- persistable interface
	- change when to create new entity logic with persistable interface
	- 
#### Custom Repository
- CutsomRepository -> CustomRepositoryImpl -> Repository
```java
public interface CustomRepository{}
public class CustomRepositoryImpl implements CustomRepository{}
public interface Repository extends JpaRepository<>, CustomRepository
```
- Implentations need to end with "Impl"
	- to change suffix
		- xml : repository-impl-postfix
		- @EnableJpaRepositories(repositoryImplementation ="Impl")