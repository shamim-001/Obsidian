[![Shortform App](https://www.shortform.com/img/logo-dark.70c1b072.svg)](https://www.shortform.com/app)

[Discover](https://www.shortform.com/app)

[Books](https://www.shortform.com/app/books)

[Articles](https://www.shortform.com/app/articles)

[My library](https://www.shortform.com/app/library)

[Search](https://www.shortform.com/app/search)

# The Clean Coder

[Back to Technology](https://www.shortform.com/app/books/category/technology)

## Chapter 4: Quality #4—Communicate via Testing

In the previous chapter, we looked at the third quality of professionals: honesty. Next, we’ll look at the fourth: communication, which is best done via testing.

Tests ensure that a system works, but that’s a happy bonus, not their main purpose. **The most important purpose of a test is to communicate, specify, and document how a system is supposed to work and how it actually works.**

In this chapter, we’ll first look at acceptance testing, which is the main type of testing used for communication. Then, we’ll look at how acceptance tests fit into the broader discipline of testing.

### How to Communicate Effectively

**When clients speak with programmers, there are often miscommunications, especially about system requirements.** This is because the businesses describe to programmers what they want (sometimes ambiguously), and the programmers estimate and build what they understand from the description (sometimes incorrectly). Ambiguity comes from two sources:

1. **Business stakeholder disagreements.** If stakeholders can’t agree on how something should work, sometimes, instead of addressing this, they’ll write a vague description that everyone can agree on. Then, a programmer has to interpret this description.
2. **Assumptions.** Sometimes stakeholders assume anyone reading their descriptions will understand what they meant.

For example, a stakeholder might tell a programmer that log files need to be backed up but not provide information about when and how often they should be backed up, where they should be saved, or how long they should be kept. A programmer might think to ask some of these questions (and as a professional it’s your responsibility to make sure requirements are as clear as possible), but the conversation isn’t foolproof.

First, we’ll look at what _doesn’t_ resolve ambiguity. Then, we’ll look at what _does_.

#### The Wrong Solution: Demanding Precision

**Both programmers and businesses often try to eliminate ambiguity by being more precise about requirements, but this doesn’t work because descriptions never match reality.** When clients see a finished product, it provides them with new information. They often realize what they initially described wasn’t actually what they wanted, or what they see inspires a better idea.

**As a programmer, you should avoid being precise until the last possible moment—until you’re just about to build it.**

#### The Right Solution: Acceptance Tests

The only way to eliminate ambiguity is to create acceptance tests. **Acceptance tests determine whether the system behaves the way the business wants it to**—in other words, these tests specify what the system is supposed to do.

- For example, if a client requires that an operation completes in under two seconds so a user doesn’t experience a delay, the test checks whether the operation completes fast enough.

**Acceptance tests are co-written by clients and testers or QA**. Sometimes the clients can write the tests themselves, otherwise, QA should work with them to gather requirements and turn these into acceptance tests. The client will usually come up with the happy-path test (checking that default usage doesn’t throw errors) and QA will write the unhappy-path tests that cover unusual scenarios. The developer only gets involved after the test is written to add it to the system. There are two things to keep in mind with these relationships:

- **Developers and testers shouldn’t be adversarial.** Testers are smart, determined, and it’s their job to find problems, so while you should strive to produce work they can’t find fault with, don’t get upset if they do find problems.
- **If someone writes a bad test, you should speak with them about it.** It’s unprofessional to make something ugly that will technically pass the test but isn’t actually useful.

To avoid the trap of premature precision, **developers shouldn’t start on a feature until the test is ready.** The first acceptance tests should be ready the day work starts, and all the tests should be completed by the halfway point.

**Perhaps writing these tests seems like extra work, but in fact, they’ll save both money and time**:

- **Money.** Manual testing is far more expensive than automated testing. For example, each one of a large Internet company’s manual tests cost over $1 million.
- **Time.** Because acceptance tests specify how the system needs to work, they have to be unambiguous. Therefore, it will be impossible for the client to ask for the wrong feature, or for the programmer to misunderstand. This will save revision time.

##### Acceptance Tests for Graphic User Interfaces (GUIs)

There are two things you’re testing when it comes to the GUI:

1. **The actual GUI.** Clients will want to make lots of changes to this, including colors, fonts, and so on.
    - (Shortform example: A client might go back and forth on the _color and shading_ of a “contact us” button.)
2. **How the GUI works.** This doesn’t change nearly as often.
    - (Shortform example: Clients rarely change their mind about whether or not to _include_ a “contact button.”)

**As much as possible, test these two things separately.** Otherwise, changes to one might break the tests to the others, which could become so frustrating you ignore your tests or stop changing the GUI, both of which are unprofessional. Keep in mind the single responsibility principle (SRP), which involves grouping elements by _why_ they change.

- For example, instead of grouping a collection of buttons together because they’re all buttons, group the buttons by what they do.

**To test the workings, test via an API instead of via the GUI** (but use the same API that GUI uses).

**To test the GUI, use stubs, or pieces of code to stand in for the business rules.** Since the GUI changes a lot, don’t test it too much, or you run the risk of getting annoying and abandoning the tests altogether.

### The Pyramid of Tests

In the previous section, we learned about testing for communication. Now, we’ll learn about how acceptance testing fits into the other testing that ensures the system behaves properly.

Testing occurs at multiple levels and is arranged in a pyramid based on how much of the code and what level of detail it covers. We’ll start at the bottom and move up:

#### Level #1: Unit Tests

Unit tests test “units”—small sections of code. Their purpose is to specify the system and they:

- **Cover as much of the code as possible** (at least 90%).
- **Run continuously (continuous integration).** They’re triggered whenever someone finishes a piece of the system and integrates it into the whole system (for example, when someone commits a model). If the tests fail, everyone on the project should stop their work and help get the system passing the tests again.
- **Are written by developers** in the same programming language as the system.
- **Are written _before_ the code is written,** using a workflow called test-driven development, which we’ll look at next.

##### Test-Driven Development (TDD)

**Test-driven development (TDD) is a workflow in which you write the tests you’ll use on your code before you actually write the code.**

There are three rules to TDD:

1. You can’t write code until you write a unit test that fails. (The test will fail because it needs code to evaluate, and the code isn’t written yet.)
    - For example, if you plan to write a function, you’ll have to mention its name in the test. The test will fail because the function doesn’t exist yet.
2. You can’t write any more of the test beyond the first failure. (Not compiling counts as a failure.)
3. You can’t write more code than you need to pass the test.

TDD comes with several advantages:

- **The cycle time is fast.** Since you test and write only a little bit of code at a time, you regularly execute the code. This is very productive because you get through each cycle quickly.
- **You know your code works.** In TDD, you test every single time you make a change, so you have confirmation that what you’ve written will work.
- **You can update the code with confidence.** You (and other programmers) can make changes to the code later, worry-free, because you already have tests designed specifically for it. (If there _weren’t_ tests, and you edited something and broke it, it would become your problem).
- **There are fewer bugs.**
    - For example, Martin uses TDD on a project called FitNesse, and FitNesse only had 17 bugs after he added 20,000 lines of code.
- **They facilitate good (decoupled) design**. Decoupled code is easier to work with because when a test identifies a problem, you can quickly find it—there aren’t layers of code the wade through.
- **Tests double as documentation.** The TDD unit tests act as instructions for how to use the program because they cover every piece of the system. (If you write tests later, they won’t be as comprehensive).

A couple of caveats:

- **TDD isn’t infallible.** It’s possible to write bad tests and to write bad code that passes good tests.
- **There are some exceptional situations in which TDD isn’t appropriate.** To evaluate if you’re in one of these, consider your rules—will using TDD do harm? If yes, don’t use it.

##### Tools of the Trade

Unit testing tools vary by language, but whichever tool you choose should have the following features:

- **There must be a fast and easy way to run the rest.** For example, all you should have to do is press a button or hit a shortcut key.
- **It must be immediately obvious whether the test passed or failed.** For example, the test might show a green bar or a single line of text that says the test passes. (It _shouldn’t_ require you to read a long report or compare files.
- **It must show testing progress so you can confirm the test hasn’t stalled.** For example, there might be a bar that shows what percentage of the test is complete.
- **There should be a way to keep the tests independent** (they don’t rely on each other). For example, the tool might run the tests in a different order every time.

Martin likes CPPUTest for C and C++, RSPEC for Ruby, NUNIT for .Net, Midje for Clojure, and JUNIT for Java.

**For the continuous build, Martin uses Jenkins—**it’s easy to learn, simple, and doesn’t take a lot of processing power.

#### Level #2: Component Tests (Including Acceptance Tests)

**The second level of the pyramid is component tests, which include acceptance tests.** Component tests test individual components and business rules. Their purpose is to test whether the software does what the client wants it to and they:

- **Cover 50% of the system.** They’re mostly happy path tests because the unhappy-path cases were already tested by the unit tests.
- **Run continuously,** just like unit tests.
- **Are written by QA and the client,** with help from programmers if necessary. (But the test-writer should never be the same person who builds the feature).

##### Tools of the Trade

You might want to use some of the following tools to test at the API level:

- **FitNesse** is wiki-based and lets test-writers write in a tabular format. It can test in almost any language. (Martin built FitNesse and it’s his favorite.)
- **Green Pepper** uses a wiki and is similar to FitNesse.
- **RobotFX** runs on flat files (like Excel sheets) and can test in any language.
- **Cucumber** uses plain text and can test many different platforms.
- **JBehave** is like Cucumber.

#### Level #3: Integration Tests

The third level is integration tests. **Their purpose is to assess how well different components communicate** (they’re only relevant in multi-component systems). They:

- **Cover 20% of the system.**
- **Execute periodically,** rather than continuously, because they take more time to evaluate.
- **Are written by the system’s lead designer or system architect**, usually in the same programming language and platform as the component tests.
- **Include throughput and performance tests.**

##### Tools of the Trade

You can often use the component testing tools for integration testing, but not when it comes to UI tests or end-to-end tests. **Martin likes Watir and Selenium for integration testing.**

#### Level #4: System Tests

The fourth level is system tests, which are the highest form of integration tests. **The purpose is to evaluate the whole system.** They:

- **Cover 10% of the system.**
- **Execute infrequently** because they take a long time to evaluate. (But the more often you run them, the better.)
- **Are written by the technical leads or system architects,** usually in the same programming language and platform as the UI (user interface) integration tests.
- **Include throughput and performance tests.**

#### Level #5: Manual Exploratory Tests

The highest level of the pyramid is manual exploratory tests—tests in which people (sometimes specialists, sometimes anyone in the company) use the system. **Their purpose is to confirm that the system operates, note bugs that come up, and report how the system _actually_ works.** They:

- **Cover 5% of the system.**
- **Are executed infrequently** because they’re expensive.
- **Aren’t written at all.** People explore the system however they like and try to break it.

### Example: How _Not_ to Be a Professional

While Martin was working at test-supplier company Teradyne, Tom, the manager of field service and installation, asked Martin to work with him on creating a trouble-ticket system. Initially, Tom just wanted Martin to teach him to use a text editor so Tom could build it himself, but both of them quickly realized this was too complicated, so Martin became the developer and Tom the client.

**They didn’t use user acceptance tests**—instead, Tom would _describe_ what he wanted and Martin would build it in front of him. Sometimes, Martin would suggest doing something else that was easier and _describe_ that. Tom might agree, but **when Tom actually saw the feature, he’d reject it.** It took a whole day to finish the simple application because the communication was ineffective.

[

Previous

Exercise: Estimate Using the PERT Method

](https://www.shortform.com/app/book/the-clean-coder/exercise-estimate-using-the-pert-method)

[

Next

Chapter 5: Quality #5—Manage Your Time Well

](https://www.shortform.com/app/book/the-clean-coder/chapter-5)