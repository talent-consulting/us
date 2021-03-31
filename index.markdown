## Welcome to Talent Consulting

At Talent we are strong proponents of Agile methodologies. Taking the flexible approach to delivery but ensuring the project is delivered to timescale, scope and budget...sometimes a difficult balancing act! But this is where our broad experience and coding standards come to the fore. 

![Talent](/images/Talent.png)
---
## Coding Design

- ### Convention over configuration
  - Should only need to specify unconventional aspects of a system
- ### Modular Design
  - Subdivide application into smaller parts, i.e. micro-services, with defined contracts
  
- ### Scalable Design
  - Ensure application modules can be scaled horizontally and vertically 

- ### Accessible Design
  - All users on all devices should be able to seamlessly and consistently access the service

- ### DRY Code
  - Early identification of common routines and methods for abstraction and shared use

- ### OO Open/Closed
  - Abiliy to add new functionality without changing existing code

- ### OO Composition over inheritance
  - Composite reuse that allows classes to achieve polymorphism by composition not inheritance

- ### Single Responsibility Pattern
  - Focus modules/classes on a single concern and single responsibility

- ### Inversion of Control	
  - Allow the application to control the program flow via a framework or configuration

---

## Coding Standards 

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
---
## Naming Conventions 
- Provide additional information about the use of an identifier
- Help formalize consistency and expectations within the team
- Facilitate the use of automated refactoring tools
- Enhance clarity and remove ambiguity
- Dissuade the use of overly long names, comical or abbreviations
- Avoid naming collisions across modules
- Ease project handovers of source code to relevant parties
- Promote understanding in case of code reuse after a long interval
 ---
## Comments
- If your code is readable then comments should be unnecessary 
- Meaningful but not verbose
- But if complex code then detail in the function header comment
- Use // not /* */ 



# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/kwootten/karlwootten/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
