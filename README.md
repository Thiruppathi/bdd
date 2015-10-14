# Behaviour Driven Development

## Introduction

Behavior-Driven Development (BDD) is an agile process designed to keep the focus on stakeholder value throughout the whole project. The premise of BDD is that the requirement has to be written in a way that everyone understands it – business representative, analyst, developer, tester, manager, etc. The key is to have a unique set of artifacts that are understood and used by everyone. A BDD story is written by the whole team and used as both requirements and executable test cases. It is a way to perform test-driven development (TDD) with a clarity that can not be accomplished with unit testing. It is a way to describe and test functionality in (almost) natural language.

##BDD Story Format

Even though there are different variations of the BDD story template, they all have two common elements:

1. **Narrative**
2. **Scenario**

Each Narrative is followed by one or more Scenarios.

The BDD story format looks like this:

````
Narrative:
In order to [benefit]
As a [role]
I want to [feature]

Scenario: [description]
Given [context or precondition]
When [event or action]
Then [outcome validation]
````

##Narrative

A narrative is a short, simple description of a feature told from the perspective of a person or role that requires the new functionality. 

The intention of the narrative is NOT to provide a complete description of what is to be developed but to provide a basis for communication between all interested parties (business, analysts, developers, testers, etc.) 

The narrative shifts the focus from writing features to discussing them.

Even though it is usually very short, it tries to answer three basic questions that are often overlooked in traditional requirements. 

1. What is the benefit or value that should be produced (In order to) ? 
2. Who needs it (As a) ? 
3. What is a feature or goal (I want to) ?

With these questions answered, the team can start defining the best solution in collaboration with the stakeholders. 

The narrative is further defined through scenarios that provide a definition of done, and acceptance criteria that confirm that narrative that was developed fulfills expectations.

````
Narrative:
In order to pay bills online
As a customer
I want to be able to save my card details
````

**Note:**
The written part of a BDD story is incomplete until discussions about that narrative occur and scenarios are written.

For More information narratives can point to a diagram, workflow, spreadsheet, or any other external document.

### How Narrative is Different From Requirement
Two most important differences between Narrative and Traditional Requirements are 

1. Precision
2. Planning

#### Precision

Narratives favor verbal communication. Written language is very imprecise, and team members and stakeholders might interpret the requirement in a different way.



#### Planning
IEEE 830 style requirements (“The system shall…”) often consist of hundreds or even thousands of statements. Planning such a large number of statements is extremely difficult. There are too many of them to be prioritized and estimated, and it is hard to understand which functionalities should be developed. 
Consider the following requirements:

- The product shall have 4 wheels.
- The product shall have a steering wheel.
- The product shall be powered by electricity.
- The product shall be produced in different colors.

Each of those statements can be developed and tested independently and assembled at the end of the process. 

The first image in someone’s head might be an electric-powered car. 
That image is incorrect. 

It is a car, it has four wheels, it is powered by electrically-powered (rechargeable batteries) and it can be purchased in different colors. 

It is a car I bought for my 3-year-old daughter. That is probably not what you would think from reading those statements. 

A better description would be:

```
Narrative:
In order to provide entertainment for children
As a parent
I want a small-sized car
```

By looking at this narrative, it is clear what the purpose is (entertainment for children), who needs it (parents), and what it is (a small-sized car). It does not provide all the details since the main purpose is to establish the communication that will result in more information and understanding of someone’s needs. 

That process might end with one narrative being split into many. Further on, scenarios produced from that narrative act as acceptance criteria, tests, and definition of done.

####Who can write narratives?

Anyone can write narratives. Each member of the team can write BDD stories or parts of them (narrative or scenario). Whether all the narratives are written by one person (customer, business analyst, or product owner) or anyone can write them (developers, testers, etc) usually depends on the type of organization and customers. 

####Good Story

A good BDD narrative uses the “**INVEST**” model:

- Independent. Reduced dependencies = easier to plan.
- Negotiable. Details added via collaboration.
- Valuable. Provides value to the customer.
- Estimable. Too big or too vague = not estimable.
- Small. Can be done in less than a week by the team.
- Testable. Good acceptance criteria defined as scenarios.

The actual work being done is accomplished through collaboration revolving around the narrative that becomes more detailed through scenarios as the development progresses. Narratives are at higher level than IEEE 830 requirements. Narratives are followed by collaboratively developed scenarios which define when the BDD story meets the expectations.

##Scenario

Scenarios describe interactions between user roles and the system. They are written in plain language with minimal technical details so that all stakeholders (customer, developers, testers, designers, marketing managers, etc) can have a common base for use in discussions, development, and testing.

Scenarios are the acceptance criteria of the narrative. They represent the definition of done. Once all scenarios have been implemented, the story is considered finished. Scenarios can be written by anyone, with testers leading the effort.

The whole process should be iterative within the sprint; as the development of the BDD story progresses, new scenarios can be written to cover cases not thought of before. The initial set of scenarios should cover the “happy path”. Alternative paths should be added progressively during the duration of the sprint.

### Format

Scenarios consist of the following steps.

1. Description - No Details; Should be less than 10 words
2. Given - Precondition to be fullfilled
3. When - Action or Event
4. Then - Outcome of the Action

Any number of Given,When & Then steps can be combined; but atleast one of each must be present.

### Process
The following process should be followed.

1. Write and discuss narrative.
2. Write and discuss short descriptions of scenarios.
3. Write steps for each scenario.
4. Repeat steps 2 and 3 during the development of the narrative.

### Sample Scenarios

Let us write scenarios for following Narrative.

````
Narrative:
In order to have a customized experience
As a site visitor
I want to be able to login
````

Once this feature has been discussed with representatives of the role (in this case a site visitor) the following initial conclusions can be drawn.

Visitors should be able to register.
Existing users should be able to log in.
There should be an option to retrieve a password.
These conclusions should be written as scenario descriptions.

````
Scenario: Visitors are able to register
Scenario: Users are able to log in
Scenario: Users are able to retrieve their password
````

Let us take the 1st scenario.

```
Scenario: Visitors are able to register
```
The Steps go as follows

```
Given the visitor is on the home screen
When the visitor clicks the register button
Then login screen is loaded
When the visitor types his email
When the visitor types his password
When the visitor clicks the register button
Then confirmation screen is loaded
```

Even though this scenario provides solid base, several steps are still missing. This situation is fairly common, because many steps are not obvious from the start.

Further thoughts & Discussion on the steps can help in introducing following additional steps.

```
Given the Visitor is NOT LOGGED IN
```

````
When the visitor RE-TYPES the password
````

Further discussion and deep thinking will add a step

````
Then Welcome Text with FirstName is displayed
````

Through Several iterations, we can cover 
- Happy Day Flow
- Negative Scenarios
- Validation Scenarios
- Confirmation Scenarios, etc.,


