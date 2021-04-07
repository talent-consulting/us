## Welcome to Talent Consulting

At Talent we are strong proponents of Agile methodologies. Taking the flexible approach to delivery but ensuring the project is delivered to timescale, scope and budget...sometimes a difficult balancing act! But this is where our broad experience and coding standards come to the fore. 

![Talent](/images/Talent.png)

## Contents

- [Coding Design](#coding-design)
  - [Coding Standards](#coding-standards)
  - [Naming Conventions](#naming-conventions)
  - [Comments](#comments)
- [Security](#security)
- [Architectural Principles](#architectural-principles)
  - [Two predominant architectural types](#two-predominant-architectural-types)
- [Government Design Systems](#government-design-systems)
  - [GOV.UK Design System](#govuk-design-system)
  - [Technology Code of Practice](#technology-code-of-practice)
  - [GDS Service Standard](#gds-service-standard)
  - [Digital Data and Technology](#digital-data-and-technology)

---




## Coding Design

- ### Convention over Configuration
  - Should only need to specify unconventional aspects of a system
  
    *"As a general rule we don't want to invent an enormous everything class that people have to inherit from. Instead we'd like the  runtimes to provide default behaviour for 'normal' objects, but to allow objects to override a given piece of default behaviour by inheriting from some specific interface."*

- ### Modular Design
  - Subdivide application into smaller parts, i.e. micro-services, with defined contracts
  
    *"design approach that creates things out of independent parts with standard interfaces that can be stacked, rearranged, customized, reused and so on"*
  
- ### Scalable Design
  - Ensure application modules can be scaled horizontally and vertically 

    *" scalability is the ability of a system to handle sudden changes in workload without negatively impacting performance. It’s usually broken down into three areas: Availability, Performance, Reliability"*

- ### Accessible Design
  - All users on all devices should be able to seamlessly and consistently access the service

    *"...a design process in which the needs of people with disabilities are specifically considered"*

    *"W3.org WCAG guidlines https://www.w3.org/WAI/"*

- ### DRY Code
  - Early identification of common routines and methods for abstraction and shared use

    *"I have an increasing sense that a pig-headed determination to
    remove all repetition can lead you a long
    way toward a good design and can help you
    apply and understand the patterns that are
    common in good designs. " **Martin Fowler**  *

- ### OO Open/Closed
  - Abiliy to add new functionality without changing existing code

    *"we should strive to write code that doesn’t have to be changed every time the requirements change" *

- ### OO Composition over inheritance
  - Composite reuse that allows classes to achieve polymorphism by composition not inheritance
 
    *"..a design principle that gives the design higher flexibility, it is better to compose what an object can do than extend what it is... "* 
 
 
- ### Single Responsibility Pattern
  - Focus modules/classes on a single concern and single responsibility

    *"..each component (method,class, module, service) should have a single responsibility: Business Logic, Control flow, Integration, Data.."* 

- ### Inversion of Control	
  - Allow the application to control the program flow via a framework or configuration
  
    *"..decouple your application to make future changes easier, code against interfaces, simpler to add unit tests.."*


[Back to Top](#contents)

---

### Coding Standards 

![Talent](/images/coding.jpg)


- Avoid hardcoded strings                                               
- Enum rather than numbers                                              
- Convert strings to lower/upper case before comparing                  
- Use string.empty not ""
- Avoid long methods, breakdown and refactor into many methods
- Avoid long code files < 1000 lines
- Member variables are private with accessors
- Any event handler should pass off to a method
- Use relative paths
- Smoke testing on initialisation
- Add Config file defaults failover if not found
- Config error reporting if incorrect value found
- Bespoke and verbose error messages with reason and possible solution
- Ideally One class per file
- Avoid passing too many parameters to a method, add class/structure
- Avoid passing null arrays, always pass initialised empty array
- Avoid too many folders in a single assembly
- Add a "finally" block to around DB access to close connection 


[Back to Top](#contents)


---

### Naming Conventions 
- Provide additional information about the use of an identifier
- Help formalize consistency and expectations within the team
- Facilitate the use of automated refactoring tools
- Enhance clarity and remove ambiguity
- Dissuade the use of overly long names, comical or abbreviations
- Avoid naming collisions across modules
- Ease project handovers of source code to relevant parties
- Promote understanding in case of code reuse after a long interval

[Back to Top](#contents)


---
 
### Comments
- If your code is readable then comments should be unnecessary 
- Meaningful but not verbose
- But if complex code then detail in the function header comment
- Use // not /* */ 

[Back to Top](#contents)

---

## Security
### Our security principles start from the National Cyber Security Centre principles below:

[![NCSC](images/security.jpg)](https://www.ncsc.gov.uk/collection/cloud-security/implementing-the-cloud-security-principles)

<img src="/images/security1.jpg" width="200" height="200" />

- Security by Design
- Principle of least privilege
- Separation of Users via User Management and IDAMS
- Secure Data in transit
- Secure Service Administration and use of the Service
- Asset Protection and Governance,
- Operational, Personnel and Supply Chain Security
- Auditing, logging and oversight

### Design
Our architectural design default is to use Micro-Services. 

Inherent in that topology is the separation of security boundaries and data isolation. 

The  threat surface is reduced due to the compartmentatlisation of the service components and independent deployments and security. So that a breach of one aspect of the system will not effect other aspects.

[Back to Top](#contents)


---

## Architectural Principles

![architectural](images/architectural.jpg) 

- Information Management 
- Business Continuity and DR 
- Data as an Asset to be Shared and Accessible
- Maximize Benefit to the Enterprise
- Ease-of-Use and Accessibility
- Control Technical Divergence

### Two predominant architectural types



| Micro-Services      				| Monolith 				 |
| --------------------------------------------- | -------------------------------------- |
|  		**Pros**      			| 		**Pros**       		 |
| Header      					| Simplicity       			 |
| Scalable					| Cross-cutting concerns       		 |
| Security Boundaries				| Performance       			 |
| Modular by Design				| Consistent Technology stack       	 |
| Independent CI/CD				| Focused release       		 |
| Maintainable/Zero Downtime			|        				 |
| Zero Downtime					|        				 |
| Diverse/Autonomous				|        				 |
| Low coupling					|        				 |
| 					|        				 |
| 	**Cons**				|  	**Cons**      			 |
| Complexity					| Reliability    			 |
| Eventual Consistency				| Large Updates/Releases       		 |
| Remote calls					| Technology stack       		 |
| Design for failure				| High coupling       			 |
| Cross-cutting concerns			|        				 |

[Back to Top](#contents)

---

## Government Design Systems

### GOVUK Design System

[![GDS](images/gdesign.png)](https://design-system.service.gov.uk/)

- Use this design system to make your service consistent with GOV.UK. 
- Learn from the research and experience of other service teams and avoid repeating work that’s already been done. 
- Make your service look like GOV.UK with guides for applying layout, typography, colour and images.
- Help users complete common tasks like entering names and addresses, filling in forms and creating accounts.

### Technology Code of Practice

[![GDSTech](images/gds.png)](https://www.gov.uk/government/publications/technology-code-of-practice/technology-code-of-practice/)

- You should use the Technology Code of Practice for all of your government technology projects or programmes. 
- Consider each point, align your project or programme with the mandatory points, and follow as many of the remaining points as is practical.
- You’ll get the most benefit by aligning your organisation’s technology and business strategies to the Technology Code of Practice.

### GDS Service Standard

[![GDSTech](images/gdsmanual.png)](https://www.gov.uk/service-manual/service-standard)

- The Service Standard helps teams to create and run great public services in a cohesive manner, maintaining consistent and accessible UX
- Solving whole problems and proofing that with User Research
- Multidisciplined Agile teams that iterate and improve 
- Secure and open source, re-using components and the right technology to create a reliable service

### Digital Data and Technology
Digital Data and Technology profession capability framework
[GDSTech](https://www.gov.uk/government/collections/digital-data-and-technology-profession-capability-framework)

[Back to Top](#contents)

---

## Contact



- **Birmingham**
1st Floor,
134 Edmund Street,
B3 2ES, UK
T. +44 (0) 117 332 0824


- **Manchester**
2nd Floor, Old Exchange Buildings,
29 – 31 King Street
M2 6AD, UK
T. +44 (0) 117 332 0824

- **Bristol**
Ground Floor, The Quorum,
Bond Street,
BS1 3AE, UK
T. +44 (0) 117 332 0824


- **London**
Sackler Studios
1-2 Bear Gardens
SE1 9ED
T. +44 (0) 117 332 0824


**E. contactus@talentconsulting.uk**


[Back to Top](#contents)



