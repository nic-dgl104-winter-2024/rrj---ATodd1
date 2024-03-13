## SSENSE/vue-carousel - CONTRIBUTING.md
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
* **chore**: Changes to the build process or auxiliary tools and libraries such as documentation generation  
