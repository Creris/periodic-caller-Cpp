# Periodic caller for C++

This class allows you to run multiple functions in background on timer.

## API
### Typedefs
* ```c++ Periodic::Function = std::function<void()> ```
	* Denotes the type of function that can be added to Periodic instance to call.
### Functions
* ```c++ Periodic() ```
	* Constructs new empty Periodic object.
* ```c++ Periodic::restart() ```
	* Restarts the timer for given instance.
	* Only affects functions that are called periodically.
* ```c++ Periodic::addFunction(Periodic::Function function, uint64_t timeoutMicro, bool periodic) ```
	*  Adds function to internal list to call after at least timeoutMicro has passed.
	* If periodic is ```false```, the function is removed from the list after it has been invoked.