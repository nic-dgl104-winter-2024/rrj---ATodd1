# SSENSE/vue-carousel
## Basic information about the open source project:  
The SSENSE vue-carousel is a versatile and responsive carousel component built using Vue.js. It offers a range of features that make it a powerful tool for creating dynamic and interactive carousels within Vue.js applications.
### link to my fork:  
https://github.com/ATodd1/vue-carousel  
## Summary of the issue examined:  
**Feature: Add keypress listeners to control carousel with keyboard input #248**  
**Description:**  
Enhance the SSENSE vue-carousel's accessibility and user experience by implementing keyboard input controls. This feature aims to allow users to navigate through carousel slides using keyboard keys, providing an alternative method of interaction alongside touch and drag gestures.

**Implementation Approach:**  
Introduce keypress event listeners to detect keyboard input. Upon detecting keypress events, the carousel component will respond accordingly by navigating to the previous or next slide based on the pressed key. This implementation ensures seamless integration of keyboard navigation functionality into the existing carousel behavior.  

## Detailed discussion of issue contributed too: Implementing Keyboard Controls for Carousel  

Contributing to the implementation of keyboard control for the carousel feature (#248) in the SSENSE vue-carousel project proved to be an intriguing endeavor, albeit one riddled with challenges. The idea itself seemed straightforward at first glance—enable users to navigate through carousel slides using keyboard input. However, the complexity lay not in the concept but in the vast expanse of the codebase.  

Navigating through thousands of lines of code spread across multiple files within the project posed a formidable challenge. While I grasped the essence of what needed to be accomplished and had a clear understanding of the implementation process, pinpointing the exact location for integrating the keyboard control logic proved to be elusive. The intricacies of the existing code structure, coupled with the absence of comprehensive documentation, compounded the difficulty of this task.  

In my pursuit to unravel the mysteries of the codebase and contribute meaningfully to the issue, I embarked on a thorough exploration of the project's existing code and relevant documentation. Despite my best efforts, the lack of clarity and coherence within the codebase often left me grappling with uncertainty. The absence of clear guidelines or conventions for feature implementation further complicated matters, making it challenging to discern the optimal approach for incorporating the keyboard control functionality seamlessly.  

In my quest for guidance and assistance, I sought insights from the community and reviewed the contributions of others who had engaged with the same issue. However, my attempts to seek clarification or assistance were met with silence, reflecting the apparent stagnation in project maintenance and community engagement. The absence of timely responses to queries and the apparent lack of active development activity underscored the challenges inherent in contributing to open-source projects with limited community support.  

Despite encountering obstacles along the way, my determination to overcome these challenges and make a meaningful contribution to the project remains undeterred. While the journey may be fraught with uncertainties and complexities, the opportunity to learn and grow through hands-on experience with real-world codebases is invaluable. As I continue to navigate the intricacies of the SSENSE vue-carousel project, I remain committed to overcoming obstacles and leveraging this experience to enhance my skills as a developer.

Despite not being able to contribute to the actual project, I still made a mock up of what I imagined the implementation would look like:  

```
export default {
  // Other component options...
  mounted() {
    document.addEventListener('keydown', this.handleKeyDown);
  },
  beforeDestroy() {
    document.removeEventListener('keydown', this.handleKeyDown);
  },
  methods: {
    handleKeyDown(event) {
      switch (event.key) {
        case 'ArrowLeft':
          // Navigate to the previous slide
          this.$refs.carousel.prev();
          break;
        case 'ArrowRight':
          // Navigate to the next slide
          this.$refs.carousel.next();
          break;
        // Add more cases if needed for additional functionality
      }
    }
  }
}
```

## Reflections of success:  


## Next steps:  
**Evaluate the Project's Viability:** I will assess whether the project is actively maintained and whether it aligns with my goals and interests. I'll look into factors such as the frequency of updates, community engagement, and the project's relevance to my skill development and career objectives.   

**Engage with the Community:** Despite previous experiences, I'll continue to reach out to the project's community for assistance and guidance. I understand that while responses may have been limited in the past, persistence and proactive engagement can sometimes yield valuable insights and support.  

**Review Project Documentation:** I'll take time to thoroughly review any available documentation, including README files, contribution guidelines, and code comments. Understanding the project's architecture and conventions will provide me with clarity and facilitate my contributions.  

**Break Down the Task:** To simplify the implementation process and make it more approachable, I'll break down the task of implementing keyboard control into smaller, manageable subtasks. I'll identify specific components or modules where the keyboard control logic needs to be integrated.



## guidline review  
There was a great set of guidelines for contributing such as “Squash your commits”, “Branch naming conventions” and “Commit Message Format”.  
It wasn’t quite as full as I expected it to be but concise is much better.  
What I learned from this particute CONTRIBUTING.md was:  
**General advice:**  
* Non-trivial changes should be discussed in an issue first  
* Develop in a topic branch, not master  
* Squash your commits  


**Branch Naming Conventions such as:**  
* Use grouping tokens (words) at the beginning of your branch names. Example:  
```
wip       Works in progress; stuff we know won't be finished soon  
feat      Feature I'm adding or expanding  
bug       Bug fix or experiment  
junk      Throwaway branch created to experiment
```  
* Define and use short lead tokens to differentiate branches in a way that is meaningful to your workflow.  
* Use slashes to separate parts of your branch names.  
* Do not use bare numbers as leading parts.  
* Avoid long descriptive names for long-lived branches.  

**Commit Message Format**  
```  
<type>(<scope>): <subject>  
```  
**Example:**  
```  
#271 feat(standard): add style config and refactor to match  
#270 fix(config): only override publicPath when served by webpack   
#269 feat(eslint-config-defaults): replace eslint-config-airbnb  
```  
**And how Type was one of the following:**  
* **feat**: A new feature  
* **fix**: A bug fix  
* **docs**: Documentation only changes  
* **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)  
* **refactor**: A code change that neither fixes a bug or adds a feature  
* **test**: Adding missing tests  
* **chore**: Changes to the build process or auxiliary tools and libraries such as documentation generatio

### link to issue:  
https://github.com/SSENSE/vue-carousel/issues/248
### link to external community project  
https://github.com/SSENSE/vue-carousel  

# Validator.js - Contributing 
## Basic information about the open source project:  
The open-source project Validator.js is a library of string validators and sanitizers. It provides a wide range of functions to validate and sanitize strings for various purposes, such as checking if a string contains certain characters, validating dates, verifying email addresses, validating credit card numbers, and much more. Validator.js offers extensive options for customization, allowing developers to tailor the validation process according to their specific requirements. It is designed to be easy to use and integrate into different JavaScript projects, offering a comprehensive solution for string validation needs.  

**A link to my fork**
https://github.com/ATodd1/validator.js/tree/new-number-add-  

## Summary of the issue examined:  
Issue #1761 titled "Mobile Phone validations - For The First Time Contributors" in the validator.js open source project aims to encourage new contributors to add phone number validations for countries that are currently not supported. The existing isMobilePhone validation function in the isMobilePhone.js file contains validations for less than 195 countries. Contributors are invited to identify countries that are not yet covered and create new validations for them. The task involves adding validations for new countries in the isMobilePhone.js file, writing tests for the new validations, and updating the isMobilePhone section in the project's README. Contributors are encouraged to check existing pull requests to ensure that the chosen country does not already have a pending validation. All pull requests are welcomed, and they will undergo review by project maintainers.  

## Detailed discussion of issues contributed too: Mobile Phone Validattions #1761  

During my involvement in the validator.js project, I had the opportunity to learn the intricacies of phone number validation, particularly in the context of contributing to the validation for Canadian phone numbers. Initially, I familiarized myself with the existing validation methods within the project, one of which particularly caught my attention – the ``` en-CA ``` method for validating Canadian phone numbers, defined as ``` /^((\+?1-?)|0)?[2-9]([0-9]{2})?[2-9]\d{6}$/. ``` Understanding the structure and logic behind this regular expression was a significant learning point for me.  

Upon examining the existing validations, I noticed the absence of validation specifically tailored for Canadian phone numbers. Motivated by this gap and intrigued by the validation process, I added support for Canadian phone number validation to the project. The steps involved were both challenging and enlightening. Firstly, I researched the standard formats and conventions for Canadian phone numbers, including area codes and number lengths, to ensure accuracy in the validation process.  

With this knowledge in hand, I proceeded to implement the validation logic following the established patterns within the isMobilePhone.js file. This involved crafting a regular expression that accurately captured the variations in Canadian phone number formats while adhering to the project's standards and conventions. Additionally, I ensured that the new validation method was appropriately documented within the README file, providing clear instructions for users and contributors alike.  

## Reflections:  

As a beginner to programming, the experience of working on this issue was both challenging and rewarding. While I may have initially felt overwhelmed by the complexity of the codebase, I found the idea of validation itself to be fascinating. Exploring the various validators offered by the project and gaining insights into their functionality was a valuable learning experience for me. Despite encountering obstacles along the way, such as difficulties in contributing to other projects, the process of adding support for Canadian phone number validation was a gratifying accomplishment.  

In the weeks following my initial contribution, I continued to refine and expand upon the validation methods I had implemented. This ongoing engagement with the project allowed me to further deepen my understanding of validation techniques and hone my skills as a contributor. Overall, my journey in contributing to the validator.js project has been an enriching experience, and I look forward to further opportunities for learning and growth within the open-source community.

## Next Steps:  
**Submit Code for Review:** In the next phase of my involvement with the validator.js project, I plan to submit the code I've added for review by the project maintainers and fellow contributors. This step is crucial to ensure the quality and compatibility of my contributions with the project standards. I'll carefully document any changes made and provide clear explanations for the implemented code to facilitate the review process.  

**Reach Out to Community:** As I continue my journey with validator.js, I aim to actively engage with the community of developers and enthusiasts involved in the project. This involves reaching out through project forums, discussion threads, or social media channels to seek advice, share insights, and foster collaborative relationships. By connecting with others in the community, I hope to gain valuable feedback, learn from their experiences, and contribute to the collective growth of the project.

## Contributing Guidlines:  

This was another short and consise guidline, very basic instructions that broke down as follows  

1. Fork the repo on GitHub
2. Clone the project to your own machine
3. Work on your fork
   * Make your changes and additions
       * Most of your changes should be focused on src/ and test/ folders and/or README.md.
       * Files such as validator.js, validator.min.js and files in lib/ folder are autogenerated when running tests (npm test) and need not to be changed manually.
  * Change or add tests if needed
  * Run tests and make sure they pass
  * Add changes to README.md if needed
4. Commit changes to your own branch
5. Make sure you merge the latest from "upstream" and resolve conflicts if there is any
6. Repeat step 3(3) above
7. Push your work back up to your fork
8. Submit a Pull request so that we can review your changes


**Link to issue**  
https://github.com/validatorjs/validator.js/issues/1761  


**Link to external communtiy project**  
https://github.com/validatorjs/validator.js  

# Rocket.Chat  

## Basic information about the source project:  
Rocket.Chat is a fully customizable communications platform developed in JavaScript. It caters to organizations within stringent data protection standards, providing a versatile solution for team communications. The platform supports real time conversations within teams, across companies and within customers, fostering increased productivity and customer satisfaction.  

**Link to my fork**  
https://github.com/ATodd1/Rocket.Chat  

## Summary of the issue examined: 
**Update Emoji library #24917**  
Currently, emojis in the emoji picker are limited to Emoji 12. The current set seem to be the one in the npm package emojione (emojione-assets in the dev dependencies). However, this project has been discontinued due to a change of name. It should be replaced by the newer emoji-toolkit package. 

## Detailed discussion of the issues contributed too: 

I'll admit I had issues with this one.  
Upon delving into the issue, I initially perceived it as a JavaScript-related task. However, as I delved deeper, I realized that the primary focus was on CSS rather than JavaScript. This realization led me to reassess my approach and understanding of the problem at hand.  

Despite this initial misunderstanding, I was determined to contribute meaningfully to the project. Recognizing the importance of clarity and guidance for future contributors, I took the initiative to outline a step-by-step tutorial. This tutorial was not only a means to demonstrate my grasp of the task but also aimed to provide a helpful resource for others navigating similar challenges.  

Navigating the Rocket.Chat codebase posed its own set of challenges. The project was divided across multiple repositories, with one dedicated to Rocket.Chat and another to JoyPixels. This division made it difficult to pinpoint the exact files and packages responsible for emoji handling. While most of the emoji-related files appeared to be CSS files, identifying the corresponding JavaScript files proved to be elusive.  

Despite these challenges, I remained committed to finding a solution. While my knowledge of the codebase may have been limited at the time, I strived to offer insights and suggestions that could potentially aid in resolving the issue. Although I may not have fully comprehended how to modify the JavaScript files to address the problem, I sought to contribute in any way possible.  

In crafting the tutorial, I aimed to bridge the gap between my understanding and the task at hand. By documenting the steps I believed should be followed to complete the task, I aimed to provide a roadmap for others facing similar uncertainties. My intention was not only to demonstrate my willingness to contribute but also to empower fellow community members to engage with the project and make meaningful contributions.  

In conclusion, while my initial approach may have been misguided, my commitment to the project and determination to contribute remained unwavering. Through this experience, I gained valuable insights into the complexities of open-source development and the importance of clear communication and collaboration within the community.  

below is the bit of tutorial I crafted:  



**Understanding the Current Implementation:**  

* Review the existing codebase, focusing on files related to the emoji picker functionality. In this case, emoji-parser.js is the relevant file.
Analyze how emojis are parsed, rendered, and displayed within messages by examining the emojiParser function.
* Identify any dependencies or external packages used for emoji handling.


**Researching the Issue:**

* Read the description of the issue (#24917) regarding the need to update the emoji library to Emoji 5.0.
* Understand the implications of upgrading the emoji library, including any changes in data structure or functionality.


**Preparing the Development Environment:**  

* Set up a development environment for Rocket.Chat, including installing necessary dependencies and tools like Node.js and npm.
* Clone the Rocket.Chat repository from GitHub to your local machine.


**Identifying Relevant Files and Packages:**

* Locate the files and packages responsible for emoji handling within the Rocket.Chat codebase.
* Determine which files need modification to update the emoji library to Emoji 5.0.


**Updating the Emoji Library:**

* Replace the existing emoji library (emojione) with the newer emoji-toolkit package, as specified in the issue description.
* Ensure compatibility with Emoji 5.0 by updating any code that relies on specific attributes or structures.


**Testing the Changes:**

* Test the updated emoji picker functionality locally to ensure that emojis are parsed, rendered, and displayed correctly.
* Verify that the emoji picker works as expected across different browsers and platforms.


**Documenting the Changes:**

* Document the changes made to update the emoji library, including any modifications to code or configuration files.
* Update relevant documentation or README files to reflect the changes and provide instructions for future contributors.


**Submitting the Pull Request:**

* Create a new branch in your local repository for the changes related to updating the emoji library.
* Commit the changes and push the branch to your fork of the Rocket.Chat repository on GitHub.
* Open a pull request (PR) against the main Rocket.Chat repository, detailing the changes made and referencing the issue (#24917).


**Engaging with the Community:**  

* Reach out to the Rocket.Chat community on forums, chat channels, or social media platforms to discuss your contribution and gather feedback.
* Collaborate with maintainers and other contributors to address any comments or suggestions on your PR.


**Reviewing and Merging the PR:**

* Participate in the review process by addressing feedback from maintainers and reviewers.
* Once the PR is approved, it will be merged into the main branch of the Rocket.Chat repository, completing the contribution process.

## Reflections of success:  
Well, this one left me feeling more defeted than succuessful, while I did get a great insight into open source communities and exactly what a full project looks like, I'm realizing my understand is a bit behind where it should be at this point.  
I really wanted to make a diffrence in these projects and as the weeks went by I grew more and more disshartend by my ability to actually contribute in any way at all.

## Next steps:  
**Clarify Understanding:** Recognizing the importance of a clear understanding of the issue, I will revisit the problem statement and related documentation. This step will ensure that I have a solid grasp of the task at hand, allowing me to proceed with confidence and accuracy.  

**Further Exploration:** To deepen my understanding of the codebase, I will embark on a thorough exploration. I'll delve into relevant JavaScript files, if available, to identify potential areas for contribution in addition to the CSS-centric aspects of the issue. By familiarizing myself with the structure and organization of the codebase, I'll enhance my ability to navigate it effectively.  

**Seek Guidance:** Recognizing the value of collaboration and mentorship, I will seek guidance from experienced contributors and project maintainers. By reaching out for support and advice, I aim to leverage the collective wisdom of the community to overcome challenges and make meaningful contributions to the project.  

## Link to issue  
https://github.com/RocketChat/Rocket.Chat/issues/24917
## Link to external community project
https://github.com/RocketChat/Rocket.Chat 



# Pattern Library  

## Basic infromation  

A multi-language library containing implementations of common software design and architecture patterns.  

**Link to my fork**  
https://github.com/ATodd1/pattern-library  

## Summary of the issues examined:
**1.Add skeleton outline for CONTRIBUTING.md #17** 
**Summary of the issue:**  

The issue examined, titled "Add skeleton outline for CONTRIBUTING.md," addresses the need to provide a structured outline for contributing to the DGL104 pattern-library project. This involves creating a CONTRIBUTING.md file with clear guidelines and instructions for potential contributors on how they can participate in the project. The goal is to streamline the contribution process and make it easier for individuals to get involved in various aspects of the project, including reporting bugs, suggesting enhancements, submitting code fixes, adding features, reviewing issues, and more.  

**What was done:**  

A comprehensive outline for the CONTRIBUTING.md file was drafted to guide potential contributors through the various ways they can contribute to the DGL104 pattern-library project. The outline covers essential topics such as project overview, prerequisites, ways to contribute, getting started, code style, testing, code review process, documentation, translations, versioning, continuous integration/continuous development (CI/CD), security, licensing, acknowledgments, and code of conduct. Each section provides detailed information and instructions to facilitate smooth and effective contributions from the community.  

By creating this skeleton outline for the CONTRIBUTING.md file, the project aims to foster a collaborative and inclusive environment where individuals of all skill levels can actively participate and contribute to the development and improvement of the DGL104 pattern-library. This initiative reflects the project's commitment to transparency, openness, and community engagement, ultimately leading to the growth and success of the project.

**2. Final README.md editing pass for formatting consistency #21**  

While I wasnt exactly assigned to this issue I did work on it slightly in the sense that I reviewed it for the criteria listed:  

* **Ensure headings are logically ordered:** The headings seem to be logically ordered, starting from the main title and descending into subsections.

* **All code blocks are wrapped in triple backticks:** The code blocks appear to be wrapped in triple backticks, which is appropriate.

* **All code blocks use appropriate language annotations:** It seems that code blocks are using appropriate language annotations where necessary, such as javascript.

* **All code in code blocks is properly indented and white space is used appropriately:** The code blocks and the content within them appear to be properly formatted with appropriate indentation.

* **All in-line references to code are wrapped in single backticks:** In-line references to code, such as variable names or code snippets, are not present in this document.

* **Markdown formatting is used appropriately and consistently:** Markdown formatting seems to be used consistently throughout the document, including headings, lists, and links.

* **Whitespace is correctly used in the raw .md code:** Whitespace appears to be used appropriately between paragraphs, headers, and lists.

* **All spurious HTML tags are removed:** The document does not contain any spurious HTML tags.

* **All markdown images include an appropriate alt-text:** There are no markdown images in this document.

* **All links are appropriately formatted as hyperlinks:** The links in the document seem to be appropriately formatted as hyperlinks.

Overall, the document appears to meet the criteria provided. Let me know if you need further assistance or if there are specific sections you'd like me to double-check.

**3. Review MVVM implementation and add clarifying comments #63**  

While I wasnt exactly assigned to this one either, I did take a look at it and did a little work on it:

```
import Observer from "./observer.js";
import Dep from "./dep.js";
import View from "../view.js";

/*
 * MVVM (Model-View-ViewModel) implementation
 * This class represents the core MVVM architecture, integrating data, views, and user interaction.
 */
export default class Mvvm {
    constructor(options) {
        this.$options = options;
        const el = document.querySelector(this.$options.el);

        // Initialize data
        this._data = this.$options.data;

        // Observe data changes
        new Observer(this._data, this);

        // Create a dependency tracker
        this.dep = new Dep();

        // Proxy for handling data access and updates
        const vm = new Proxy(this, {
            get(target, propKey) {
                // Check if the property exists in the target or data object, or in methods
                return Reflect.get(
                    Reflect.has(target, propKey) ? target :
                    Reflect.has(target._data, propKey) ? target._data :
                    target.$options.methods, propKey);
            },
            set(target, propkey, value) {
                // Set the property value and notify dependents
                Reflect.set(target._data, propkey, value);
                target.dep.notify();
                return true;
            },
        });

        // Initialize the view
        new View(el, vm);
    }
}
```
I also could have sworn I asked to be assigned to this issue because I did work on it, here is my sample:
```
// Model
class Model {
  constructor() {
    this.data = [];
  }

  // Methods to manipulate data
  addItem(item) {
    this.data.push(item);
  }

  removeItem(index) {
    this.data.splice(index, 1);
  }

  getData() {
    return this.data;
  }
}

// View
class View {
  constructor() {
    this.root = document.getElementById('app');
  }

  render(data) {
    this.root.innerHTML = data.map(item => `<div>${item}</div>`).join('');
  }
}

// Controller
class Controller {
  constructor(model, view) {
    this.model = model;
    this.view = view;

    // Bind event handlers
    this.view.root.addEventListener('click', this.handleClick.bind(this));
    
    // Initial render
    this.updateView();
  }

  handleClick() {
    // Example: Add item to model on click
    this.model.addItem('New Item');
    this.updateView();
  }

  updateView() {
    const data = this.model.getData();
    this.view.render(data);
  }
}

// Instantiate Model, View, and Controller
const model = new Model();
const view = new View();
const controller = new Controller(model, view);
```
In this implementation:  

The Model manages the application data.
The View renders the UI based on the data from the Model.
The Controller listens to user input from the View, updates the Model accordingly, and updates the View with the new data.
This separation of concerns makes the code more modular, maintainable, and easier to understand. It also allows for better scalability and reusability of code components.  


**4. Write definition of Strategy pattern in README.md #69**  

While I wasnt assigned to this issue I did do some work on it.  
**Strategy Pattern**  
The Strategy pattern is a behavioral design pattern that enables an object, called the context, to vary its behavior at runtime by selecting from multiple algorithms or strategies. This pattern defines a family of algorithms, encapsulates each one, and makes them interchangeable. By doing so, the Strategy pattern allows the client to choose the algorithm that best suits its needs without altering the context.  

**Key Components:**  
Context: The class that contains a reference to the strategy interface and is configured with a concrete strategy object.  

Strategy: The interface or abstract class that defines a set of methods for the algorithms. Concrete strategy classes implement these methods to provide specific behaviors.  

**Usage in This Project:**
In this project, we employ the Strategy pattern to encapsulate various algorithms or strategies that perform specific tasks. By defining a common interface for these strategies, we enable the context to dynamically select and execute the appropriate algorithm based on the current requirements or conditions.


## Detailed discussion of issues contributed too and reflections of success:

My journey into the world of open-source software development with the DGL104 pattern-library project was filled with both excitement and challenges. As a newcomer, I was eager to learn and contribute, but my lack of experience often posed hurdles along the way.  

One of the issues I tackled was to outline the CONTRIBUTING.md file. While I didn't contribute much to this particular issue, I understood its importance. I crafted a structured outline to guide potential contributors, highlighting ways to report bugs, suggest enhancements, and submit code fixes.  

Another task involved reviewing the README.md for formatting consistency. Although not specifically assigned, I took the initiative to ensure headings were logical, code blocks were properly formatted, and markdown was used consistently.  

Additionally, I delved into understanding and adding clarifying comments to the MVVM implementation. While I struggled with some concepts due to my limited experience, I managed to grasp the essence of the code and added comments to enhance readability.  

Lastly, though not directly assigned, I explored the Strategy pattern and proposed its definition for inclusion in the README.md. Despite facing challenges in grasping advanced design patterns, I persevered and contributed to the project's documentation.  

Throughout this journey, my primary obstacle was my novice status. Despite feeling inadequate at times, I endeavored to make up for it by showcasing my efforts in the CONTRIBUTING.md file. As I continue to learn and grow, I am confident that each contribution, no matter how small, brings me closer to becoming a proficient member of the open-source community.








 



