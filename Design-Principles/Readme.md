## Principles Of Software Design


### Principles of consider for container-based application design

* KISS  —  Keep it simple, stupid.
* DRY —  Don’t repeat yourself.
* YAGNI — You aren’t gonna need it.
* SoC —  Separation of concerns.

### Principles of Object Oriented Design 


* DRY (Don’t repeat yourself)
* Include Default Methods in Interfaces (JDK 8)
* Favor Composition over Inheritance
* Programming for Interface not for Implementation
* Minimize Coupling
* Maximize Cohesion
* KISS (Keep It Simple, Stupid)
* Delegation Principles
* Encapsulate What Changes
* YAGNI (you aren’t gonna need it)


#### SOLID design principle

* Single Responsibility Principal

A class should have one and only one responsibility. There should be only one reason to change. It should be loosly copuled and tightly cohesive. Some examples of single responsibility are:

```
• Persistence
• Validation
• Notification
• Error Handling
• Logging
• Class Selection / Instantiation
• Formatting
• Parsing
• Mapping
```

Example : Reading from a text file, writing to a database, making a service call and writing to a log all in the same method.

* Open and close principal

 'Open for extensions but closed for modificatio'

To add or change functionality in an existing class you should be able to do it by extending the class rather than modifying.

Example : Inheritance or subclasses, Passing arguments in function instead of hardcoding.


* Liskov substitution principle

‘Subclasses should be substitutable for their base classes’

 Objects of a superclass shall be replaceable with objects of its subclasses without breaking the application
 

*
*

### References
* https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper
* https://javatechonline.com/oops-design-principles/
* https://medium.com/@derodu/design-patterns-kiss-dry-tda-yagni-soc-828c112b89ee
