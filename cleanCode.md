# Summary of Uncle Bob's lecture of "Clean Code" (some parts are taken from the book "CLean Code" also):

## Two reasons of wanting to write clean code:
1. You are a programmer.
2. You want to be a better programmer.

           
## General rules
1. Follow standard conventions.
2. Keep it simple stupid. Simpler is always better. Reduce complexity as much as possible.
3. Boy scout rule: Leave the campground cleaner than you found it.
4. Always find root cause. Always look for the root cause of a problem.

## Names rules
1. Choose descriptive and unambiguous names.
2. Make meaningful distinction.
3. Use pronounceable names.
4. Use searchable names.
5. Replace magic numbers with named constants.
6. Avoid encodings. Don't append prefixes or type information.


Reveal your intent through names.

Variable name length are proportional to the scope size.

    If a variable is in a small scope, small name is preffered.
    Long variable name in long scopes for better understanding of the use. 

But it will be opposite for Functions name:

Function names are inversely proportional to the scope size.

     Large scope function means it will be used more frequently, so smaller name
     is preffered.
  
Name of classes is similar as functions.


## Functions rules
1. Small.
2. Do one thing.
3. Use descriptive names.
4. Prefer fewer arguments.
5. Have no side effects.
6. Don't use flag arguments. Split method into several independent methods that can be called from the client without the flag.

Good Code / Refactored Function

    Functions should not be 100 lines long.
    Functions should hardly ever be 20 lines long.
  
Shrunk Code / The Rules of Functions

    1st rule:   Functions should be small
    2nd rule:   They should be smaller than that.

Prose Code / Arguments

    Keep the argument count between 2-3
    Never use a arg type of boolean, use 2 different functions instead.
    
Avoid Switch Statements / Problems and Evolution of some programming languages

    Because they break.
  
Output Arguments has No Side Effects / Garbage Collection

Side effect functions come in pair, like open and close.

No Side Effects / Using Lambda

No Side Effects / Command and Query Separation

    Convention: Anything that returns a value by default they does not change 
    the system.
    Whoever returns void changes the system.
  
No Side Effects / Prefer Exceptions to returning error codes

    Inside in try block, we should keep only the try block, nothing others as prefix or suffix.


## Comments rules
1. Always try to explain yourself in code.
2. Don't be redundant.
3. Don't add obvious noise.
4. Don't use closing brace comments.
5. Don't comment out code. Just remove.
6. Use as explanation of intent.
7. Use as clarification of code.
8. Use as warning of consequences.

Purpose is to explain the code if the code can't explain itself.

Comments are good but not pure good.

Comments are actually failure, failure to make the code express itself. 

They should be used as a last atempt to explain the code.


Formatting

File size is not a function of project size.


#### Long code is not Good Code
#### DRY Principle (Don't Repeat Yourself)
#### Expectations / We will Not Ship Shit.
    Before uploading some code in the internet or publishing something, we should 
    make sure that the code works.
#### We will always be ready.
#### Stable Productivity.
#### Inexpensive Adaptability / The software must be changeable.
    Software = Soft + Ware(=Product) = Changable product.
    Softwares should be easy to change.
    If it is not easy, then it is just an another form of Hardware.
#### Continuous Improvement / The code should improve over time.
    Over time the code/design/system should improve, if not, then it's bad.
#### Fearless Competence / Conquer the fear with Test.
    Do not hesitate to use/update others code, we should clean the mess if it has 
    any, doesn't matter who created that. Unless that system/software will rot.
    
    We should conqure this fear with test.
#### We will not dump on QA / QA will find nothing.
    QA should not find nothing, as the programmers should ensure that everything 
    works fine.
    We should do "Automation" for testing.
#### We cover for each other / Teamwork.
    Pairing (Pair Programming)
#### Honest Estimates
    Estimations can be of 3 types: Best Case, Normal Case, Worst Case.
    We should cosider everything.
###### You to say "No".
    If you have given a task with a time that is not enough to do it properly,
    then you should be able to say "NO", you must say "NO".

#### Selection, Secuence and Interaction / No innovations have been made in the software for decades.
    All new programming language follow the same pattern for a very long time:
    Selection, Secuence and Interaction. 
    
## TDD (Test Driven Development)
    It is a very rich topic.
    In simple words: Write the test first (oviously the test will fail) and then
    make your code to pass the test. Repeat this for every test that comes to mind.
    
    Do not try to use the method just after knowing it, you may fail and find it
    frustrating.
    Learn the skills externally. Master the skills.
    Then use that into your work.

## Design rules
1. Keep configurable data at high levels.
2. Prefer polymorphism to if/else or switch/case.
3. Separate multi-threading code.
4. Prevent over-configurability.
5. Use dependency injection.
6. Follow Law of Demeter. A class should know only its direct dependencies.

## Understandability tips
1. Be consistent. If you do something a certain way, do all similar things in the same way.
2. Use explanatory variables.
3. Encapsulate boundary conditions. Boundary conditions are hard to keep track of. Put the processing for them in one place.
4. Prefer dedicated value objects to primitive type.
5. Avoid logical dependency. Don't write methods which works correctly depending on something else in the same class.
6. Avoid negative conditionals.


## Source code structure
1. Separate concepts vertically.
2. Related code should appear vertically dense.
3. Declare variables close to their usage.
4. Dependent functions should be close.
5. Similar functions should be close.
6. Place functions in the downward direction.
7. Keep lines short.
8. Don't use horizontal alignment.
9. Use white space to associate related things and disassociate weakly related.
10. Don't break indentation.

## Objects and data structures
1. Hide internal structure.
2. Prefer data structures.
3. Avoid hybrids structures (half object and half data).
4. Should be small.
5. Do one thing.
6. Small number of instance variables.
7. Base class should know nothing about their derivatives.
8. Better to have many functions than to pass some code into a function to select a behavior.
9. Prefer non-static methods to static methods.

## Tests
1. One assert per test.
2. Readable.
3. Fast.
4. Independent.
5. Repeatable.

## Code smells
1. Rigidity. The software is difficult to change. A small change causes a cascade of subsequent changes.
2. Fragility. The software breaks in many places due to a single change.
3. Immobility. You cannot reuse parts of the code in other projects because of involved risks and high effort.
4. Needless Complexity.
5. Needless Repetition.
6. Opacity. The code is hard to understand.
