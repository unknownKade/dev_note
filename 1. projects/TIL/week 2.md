# Circuit Breaker
- checks and stops/restarts calls between services to maintain stability of the overall system
- when calls fail repeatedly the circuit breaker detects this as a system failure and isolates it to not affect other parts of the system
- managed through three states
	- Close : circuit breaker is closed and all calls are passed. when a call fails the fail counter goes up
	- Open : all calls attempts are stopped and returned as failed
	- Half-CLosed : 

# Resilence4j
- Closed : 
- Half :