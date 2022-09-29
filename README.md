# UML and Object Oriented Design Overview <!-- omit in toc -->

## Contents <!-- omit in toc -->

- [1. What are Software Development Methodologies?](#1-what-are-software-development-methodologies)
  - [1.1. The Waterfall Model](#11-the-waterfall-model)
    - [1.1.1. Phases of the Waterfall Model](#111-phases-of-the-waterfall-model)
    - [1.1.2. Resume](#112-resume)
  - [1.2. The Agile Approach](#12-the-agile-approach)
    - [1.2.1. How to works](#121-how-to-works)
    - [1.2.2. Sprints](#122-sprints)
    - [1.2.3. Advantages](#123-advantages)
    - [1.2.4. Differences](#124-differences)
  - [1.3. Waterfall or Agile?](#13-waterfall-or-agile)
- [2. Core object orientation concepts](#2-core-object-orientation-concepts)
  - [2.1. Objects](#21-objects)
  - [2.2. Class](#22-class)
  - [2.3. Abstraction](#23-abstraction)
  - [2.4. Encapsulation](#24-encapsulation)
  - [2.5. Inheritance](#25-inheritance)
  - [2.6. Polymorphism](#26-polymorphism)
  - [2.7. More about](#27-more-about)
- [3. Object oriented analysis and design](#3-object-oriented-analysis-and-design)
  - [3.1. Collect the requirements](#31-collect-the-requirements)
  - [3.2. Description of the software system](#32-description-of-the-software-system)
  - [3.3. Identify the things that form our system](#33-identify-the-things-that-form-our-system)
  - [3.4. Describe the behavior of our system](#34-describe-the-behavior-of-our-system)
- [4. Diagrams](#4-diagrams)
  - [4.1. What's UML?](#41-whats-uml)
  - [4.2. Use Case](#42-use-case)
  - [4.3. Class](#43-class)
  - [4.4. Sequence](#44-sequence)
  - [4.5. Activity](#45-activity)
  - [4.6. Statechart](#46-statechart)

# 1. What are Software Development Methodologies?

- There are different ways to develop a software system.
- I will talk about two of the most popular development methodologies:
  - The **Waterfall** model, which requires you to have a detailed plan before starting any coding.
  - The change-friendly, responsive **Agile approach**, which works great for projects where the expectations can change rapidly and frequently.
- _None of these systems can precisely describe every step of the software development process._

## 1.1. The Waterfall Model

- The Waterfall is a linear model.
- It defines development steps or phases.
- You start executing one step, complete it and then start the next one.
- The development process flows in cascades.
- Each development phase requires the previous one to be completed.

### 1.1.1. Phases of the Waterfall Model

1. Collect and analyze requirements

- The expected functionality of the future application must be **clarified with the stakeholders**.
- All the details must be **documented thoroughly**.

2. Architecture definition

- Defining the architecture is like creating the blueprint for a building.
- The design should be as clear and detailed as possible.
  - Components/packages.
  - Key types.
  - Interactions.
  - Security.
  - Performance.
  - Fault-tolerance.
  - Robustness.
  - Extensibility.
  - 3rd party usage.

3. Implementation

- The software development phase is usually divided into smaller units.
- Each unit is then implemented and tested by developers.

4. Verification

- The software is evaluated based on predefined criteria.
- We must check whether the product provides the functionality we agreed on.
- Tests are executed to ensure that the software works as expected.
- We test for:
  - Functional
  - Performance
  - Security
  - Usability issues.
- Detected problems are recorded and fixed.
- The process goes on until all severe bugs are fixed.
- The verification phase may also bring to surface deeper bugs and critical issues that may affect the planned release.

5. Maintenance

- Is about fixing smaller bugs.
  - But more often than not, it may also include functional enhancements.
- The client may come up with new requirements that involve substantial changes.
- You may feel tempted to squeeze in "just one more patch" in the maintenance phase.
- **This is usually a bad idea. In this case, we need to set up a new waterfall project and repeat all the steps.**

![WaterfallModel](/Images/WaterfallModel.png)

### 1.1.2. Resume

- The Waterfall model is used for:
  - Life-control
  - Medical
  - Military systems.
- This model requires us to clarify all the requirements and create a detailed plan upfront.
- The Waterfall is a perfect choice if all requirements are precisely defined and won't change over time.
- The Waterfall has received some criticism for its inability to respond to changes.
- Due to its linear structure, new requirements can't be considered at later phases of the development process.
- If the client changes their mind frequently, or our design misses essential aspects, we're going to hit problems during development or testing.
- In such cases, we should follow a different approach.

## 1.2. The Agile Approach

- Agile is a relatively new approach to software project management.
- It all began with the agile manifesto in 2001.
- This manifesto was an attempt to end the proliferation of methodologies that had developed.
- The agile manifesto defines four values:
  - **Individuals and interactions** over the processes and tools:
    - This doesn't mean that we won't use processes and tools in agile projects.
    - We still need tools and processes, but they shouldn't prevent us from implementing the required features or changes.
    - Instead of enforcing people to follow a rigid process, we implement a process that's adaptive and responds to changes.
  - **Working software** over comprehensive documentation:
    - This doesn't mean that agile projects don't use documentation at all.
    - We should create documentation where it provides value.
    - There's no need to create extensive documentation just for the sake of it.
  - **Customer collaboration** over contract negotiation:
    - Don't get this wrong either.
    - Agile projects also require contracts to manage customer expectations about costs and schedules.
    - Yet, unlike for plan driven projects, there is a spirit of partnership between the development team and the customer.
    - Due to the somewhat uncertain nature of agile projects, both parties acknowledge that some requirements and details may need to be redefined or clarified further as the project progresses.
    - It goes without saying that this kind of partnership requires collaboration and trust.
  - **Responding to change** over following a plan:
    - Agile is different from plan driven approaches and provides more flexibility compared to the **Waterfall model**.
    - The major difference is that agile welcomes changes even at the later phases of the development cycle.
    - Some planning is also required for agile projects.
    - But we don't try to come up with a detailed plan for the entire project before starting any development activities.
    - As a consequence we're not blocked until all the requirements are clarified and each and every question gets answered.

### 1.2.1. How to works

- The main idea behind Agile is that we can provide functional software iteratively instead of delivering the entire project all at once.

### 1.2.2. Sprints

- The work is broken up into shorter chunks called sprints.
- The Sprint is usually two to four weeks long.
- At the end of each sprint the team should deliver a version that's an improvement over the previous sprint's outcome.

![SprintAndReviewsModel](/Images/SprintAndReviewsModel.png)

### 1.2.3. Advantages

- This interactive approach provides an opportunity to frequently review the product that's being developed.
- Stakeholders have a chance to evaluate the software and provide their feedback early on rather than waiting for the final product to be delivered.
- These frequent checkpoints are super useful as they ensure that the project evolves in the right direction.

### 1.2.4. Differences

- Unlike the waterfall, agile methodologies do not separate testing from development.
- Testing is tightly integrated with development and the entire team owns the responsibility for the quality of the product.
- Alsoinvolving the business users in the development process stands at the core of agile approaches.
- There's a strong relationship between the project team and the stakeholders and business users.
- This model works best in situations where the requirements can't be defined upfront.
- Agile is a good fit for software projects that are depending on many uncertain factors and changes are to be expected.
- One of the big benefits of this collaborative model is that it usually leads to higher customer satisfaction.
- Also team members will likely be more motivated by engaging customers directly.
- **Note that Agile is not a methodology but rather a way of thinking defined by the agile manifesto values and principles.**
- **Scrum** and **Kanban** are examples of discrete methodologies that implement the Agile approach.

## 1.3. Waterfall or Agile?

- **Waterfall** is best suited for projects with clear requirements and fixed scope.
- Choose **Agile** if requiriments are unstable and may change frequently.

# 2. Core object orientation concepts

## 2.1. Objects

- While structured programming relies on actions, object oriented programming is organized around objects.
- An object represents a thing. Just like in real life, objects can be simple or complex.

## 2.2. Class

- Building an object oriented system starts by identifying the potential objects, their attributes, and responsibilities. We need to have a class before we can create an object.
- **The class is the blueprint of an object.**
- You can think of a class as a plan, a description of what an object will be.
- An object is a realization of this blueprint.

## 2.3. Abstraction

- Abstraction is a way of describing complex problems in simple terms, by ignoring some details.
- Eliminating the nitty-gritty details let us focus on the bigger picture.
- We can dig deeper once we have a broader understanding.

## 2.4. Encapsulation

- The next fundamental idea to keep in mind when dealing with OOP and classes is called encapsulation.
- We encapsulate something to protect it and keep its parts together.

## 2.5. Inheritance

- Inheritance is a key concept in object oriented programming.
- Without inheritance, we'd end up writing similar code over and over again.
- Inheritance means code reuse.
  - That is, reusing an existing class implementation in new classes.

## 2.6. Polymorphism

- Polymorphism is about working freely with instances of many different classes that share a common superclass.

## 2.7. More about

[C# Intermediate Classes, Interfaces and OOP](https://github.com/jeftegoes/CSharpIntermediateClassesInterfacesOOP)

# 3. Object oriented analysis and design

- Building an object-oriented application requires some preliminary steps.

## 3.1. Collect the requirements

- We answer the following questions:
  - What's the problem we're trying to solve?
  - What does our app or framework need to do to accomplish that functionality?

## 3.2. Description of the software system

- We should describe the app from the user's perspective.
- This step of describing the app may include the creation of visual mockups, wireframes or even prototypes.
- If it helps in communicating your thoughts to the client, then do it.

## 3.3. Identify the things that form our system

- Picking the essential entities won't be challenging if we did a good job at the previous two steps.
- We'll realize that we need a class that represents say an item that has a name, a price, and some other attributes; or a class responsible for securely communicating with a server.
- Another class may manage your local persistence, and so on.

## 3.4. Describe the behavior of our system

- This last step is about creating visual representations of our classes, their attributes and behavior.
- We also model the interaction between the objects.

# 4. Diagrams

- Understanding a software system just by looking at its source code can be very time-consuming.
- And communicating ideas about software design or business processes is even harder if there's no commonly accepted way to do it.

## 4.1. What's UML?

- The Unified Modeling Language - in short UML - was introduced to solve this problem.
- UML is not a textual programming language, but rather a graphical notation; a set of diagrams that help in designing and communicating software systems.
- We can use these diagrams to describe the objects that form a system and their interactions.
- UML has many diagram types: Use case, Class, Sequence, Activity, Statechart most common.

## 4.2. Use Case

- Its purpose is to visualize the functional requirements of the system.
- Use-case diagrams show groups of related use-cases.
- Sometimes they may include all the use-cases.

## 4.3. Class

- Without any doubt, class diagrams are the most frequently used UML diagram types.
- After identifying the entities that form our system, we start creating class diagrams for each of them.

## 4.4. Sequence

- UML provides dynamic diagrams to represent how objects communicate with each other.
- The most common dynamic diagram is the sequence diagram.
- We use the sequence diagram to describe the flow of logic in one particular scenario.

## 4.5. Activity

- Activity diagrams can be used to describe workflows.

## 4.6. Statechart

- The Statechart or State Machine diagram models how an object transitions from one state to another over its lifetime.
