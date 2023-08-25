#design-pattern #article 
https://blog.bitsrc.io/my-9-favorite-design-patterns-in-javascript-9d2a09651d08

Design patterns are reusable solutions for common problems that occur during software development. Every JavaScript programmer has encountered the same problems you have and the same solution have been used over and over again. Those solutions are the design patterns.

Every programming language has a lot of those solutions created by its community. This combined experience from several developers makes design patterns so useful. They help us write code that is optimized and solves our problems. Another great advantage is that being so common, different developers can easily understand each other code.

The greatest benefits from design patterns are:

- **Solutions that work:** Because they are used by a lot of developers, you can be sure that they work. And not just that, but as the patterns have been used a lot of times, several optimizations were made.
- **Easily reusable:** Design patterns are reusable by definition and even though they are very generic, they can be easily adapted to particular problems.
- **They are expressive:** Design patterns can describe a complex solution in an elegant format.
- **Reduce the need for refactoring:** When you write an application with design patterns in mind, it is easier to get to a clean code faster. This way we make less refactors. Specially in JavaScript, a language that allows for so many ways to write the same thing.
- **Makes your code smaller:** As design patterns are usually optimized, they need less code to be implemented, and less code means less bugs.

With all that being said you should be already willing to start using design patterns on your projects. I will give a brief overview on the history of JavaScript, glance over some important features and then we will dive deeper onto the design patterns.

# A Brief History of JavaScript

Nowadays JavaScript is the most popular language for web development, but at its inception it was just a “glue” between HTML elements. JavaScript was devised as a scripting language for the Netscape browser. By that time, all that browsers could do was render static HTML pages, the appearance of JavaScript lead to the a war between the big ones of the time, Netscape and Microsoft.

The large companies of the early 90’s wanted to use their own script language, Netscape with JavaScript (created by Brendan Eich in 1995) and Microsoft with JScript.

As you can imagine, there were a lot of differences between then and each website had to be done for a specific browser, always with a signal for “best viewed in …”. Soon was clear that we needed a standard, a cross-browser language to unify the development process e simplify the creation of web pages. The result was [ECMAScript](https://www.ecma-international.org/publications/standards/Ecma-262.htm).

ECMAScript is a specification for a script language that all browsers try to support. There are several ECMAScript implementations, but the most popular is JavaScript. Since its launch, ECMAScript has standardized a lot of important things — for the curious there is a list on [Wikipedia](https://en.wikipedia.org/wiki/ECMAScript). So, when people say things like ES6, they are referring to JavaScript's implementation of ECMAScript specification version 6.

# Some Important Features of JavaScript

We need to take a closer look at some aspects of the language that help us implementing the design patterns. We can define JavaScript like this:

> ==JavaScript is a light language, interpreted, object oriented with functions as first class citizens, that is mostly known as the language for web pages==

That definition is to say that JavaScript has a small footprint on the system’s memory, it is easy to use, easy to learn and has a syntax similar to other popular languages. Originally JavaScript was a interpreted language, but now it uses a JIT (just in time) compiler. Has support for procedural programming, object oriented programming and functional programming, what makes it very flexible (and also causes a lot of problems).

Now that we know what JavaScript is and it's main characteristics let's see some features.

## JavaScript supports first class functions

That is something that may be harder to grasp if you are coming from languages like C or C++. To say that JavaScript treats functions as first class citizens is to say that you can pass functions as parameters to other functions as a common argument. Almost like if they were objects.

## JavaScript is based on prototypes

As any other object oriented language, JavaScript supports objects, and when we say objects we immediately think of classes and inheritance. This is where things get weird, originally JavaScript had no support for classes, and still uses an inheritance based on prototypes.

Prototype based programming is a style that builds the reuse of features (the inheritance) by reusing already existing objects that are extended and not implemented. We will see this better on the design patterns examples. This characteristic is really important on a lot of patterns.

## Event loops on JavaScript

If you have ever programmed on JavaScript, for sure you are familiar with term **callback**. For those that are not, callback is a function passed as parameter that will be executed when a event is fired. They are usually used to listen for events as mouse click or button press.

Every time an event that has a listener is fired, a message is sent to a queue that is processed synchronously, on a FIFO (first-in-first-out) manner. This is called the event loop.

Each message in the queue has a function related to it. Every time a message leaves the queue, the function is completely executed before any other message is processed. It means that if a function contains other calls to other functions, they are all made before a new message from the queue is processed. This is called run-to-completion.

The `queue.processNextMessage()` waits for new messages in a synchronous manner. Each one of the messages being processed has its own stack and is processed until the stack is empty. Once all the process are finished, a new message is read from the queue, this goes on while there are messages on the queue.

You may have also heard that JavaScript is non blocking. When an asynchronous operation is being processed, the program can go on processing other things, like new inputs, without blocking the main thread. This JavaScript property is very useful, in fact, that’s the reason a lot of people opt for the language outside the browser. This is a very interesting topic and deserves a post for himself.

# What are Design Patterns?

Design patterns are commonly used solutions to common software development problems.

## Proto-pattern

How a pattern is created? Say you recognized a recurring problem and you have a unique solution for this problem, one that has not been documented anywhere yet, not even on Stack Overflow. You use this solution every time you find this problem and believe that it is reusable and that all the development community would benefit from it.

Does your solution immediately becomes a pattern? Luckily, no. It is normal for someone with good development practices to mistake something that looks like a pattern, with something that actually is a pattern.

How can you know if what you have found is really a design pattern?

By sharing it with other developers, programming is a team sport playing by a large community. There is a phase trough which every pattern must pass before being know as a design pattern, the proto-pattern.

A proto-pattern needs to be used and tested by several developers before becoming a real pattern. There is a huge work of documentation to be done for a pattern to be recognized and used by the community.

## Anti-pattern

Just as a design pattern stands for a good practice, an anti-pattern stands for a bad practice.

A good example of anti-pattern in JavaScript is to change the `Object` prototype. Practically all objects in JavaScript inherit from `Object` (remember, JavaScript uses a prototype based inheritance) so imagine that you have changed this prototype. The changes to `Object` would be seen in every object that inherits from it — **which would be almost all objects from JavaScript**. A disaster waiting to happen!

Another example is to change objects you don’t know. A small modification on a method from an object used all around the application could cause a huge mess, the bigger the team the bigger the mess. You would have naming collision, incompatible implementations and a nightmare for maintenance. With luck your tests would save you before anything happens.

In the same way that is important to know good practices, it is also a good idea to know the bad ones. This is a good way to realize the errors and avoid them before it is too late.

# Design Patterns Categories

Design patterns can be categorized on several ways, here are the most popular:

- **Creational** design patterns
- **Structural** design patterns
- **Behavioral** design patterns
- **Concurrency** design patterns
- **Architectural** design patterns

## **Creational Design Patterns**

This patterns deal with object creation on a more optimized way than the basic object creation. When the regular object creation manner would cause more complexity or bring problems to the code, creational patterns can solve the problem.

## **Structural Design Patterns**

These patterns work with relations between objects. They guarantee that if a system’s part change, nothing else has to change with it.

## **Behavioral Design Patterns**

This kind of pattern acknowledge, implement and improve communication between objects of the system. They help to guarantee that unrelated parts of the application have a synchronized information.

## **Concurrency Design Patterns**

When you are dealing with multi threading programming these are the patterns that you will want to use.

## **Architectural Design Patterns**

Design patterns that are used on the system’s architecture, like MVC or MVVM.

On the next section we will take a look at some of these patterns, with examples for better understanding.

# Examples of My 9 Favorite Design Patterns

Each design pattern represents a solution for a given problem. There is no universal set of patterns that will solve every problem that you will encounter. We need to understand when a given pattern will be useful and how it will actually deliver value. Once we are familiar with design patterns and the cases on which they fit, we will be able to determine which pattern we can use and if it solves the problem at hand.

Remember, using the wrong pattern can lead to unwanted effects, unnecessary complexity, and performance loss.

This are all important things to be considered when we are thinking on applying a design pattern to our code. Let’s see some patterns that are more useful on JavaScript and every senior JavaScript developer should know.

## 1. Constructor Pattern

When we think on the classic implementation of object oriented languages, a constructor is a special function that initializes the class’s values on default or with input from the caller.

Three common ways to create an object in JavaScript are:

After our object is created we have four ways to add properties to it. They are:

The most usual way for object creation is using `{}` and to add properties the dot notation or `[]`. That is why I recommend that you use these methods, it will make a lot easier for other programmers to understand your code and even your future self.

We mentioned earlier that JavaScript does not support native classes, but it supports constructors trough the keyword `new` prefixed to a function call. This way we can use a function as constructor and initialize properties on the same we would on a more traditional language.

We can still improve this code. The problem is that the method _writesCode_ is redefined for every instance of _Person_. Because JavaScript is prototype based we can avoid that by adding the method to the prototype.

Now, both instances of Person can access the same shared instance of `writesCode()`.

It is as if on the first example we had a **different method** for each object of type `Person`, each `Person` points to their own function definition. On the second example, all `Person`s will point to the same function, the same piece of code.

## 2. Module Pattern

Despite being object oriented, JavaScript does that on it’s own peculiar way. Because it does not have proper classes, it also can not limit access to a class’s components. On a language as Java or C++ you can define the access rights for a class’s members (private, protected, public, etc.), but being the clever little thing it is, JavaScript has a way to emulate this behavior.

Before we get into the details about module pattern, let’s take a better look at **closures**. A closure is a function with access to it’s parent’s scope, even after the parent has finished. They will help us emulate the behavior of access limiters. Let’s see an example:

As you can see, we tied the variable _counter_ to a function that was called and closed, but we still can access it trough the child function that increments counter. Note that the inner function is returned from `counterIncrementer()`. We can not access counter from outside the function, essentialy, we created a private variable in vanilla JavaScript trough scope manipulation.

Using closures we can even create objects with public and private parts. This is very helpful when we want to hide some parts of an object and only present a nice interface for the module’s user. The example:

The greatest utility of this pattern is to make a clear separation between the public and private parts of an object.

Not everything is happiness, this pattern has some problems. When we want to change the visibility of a member, we must change that on every caller as well, because the access is different for public and private parts. Another problem is that methods added after the object is created can not access private methods (but we don't want to add new methods anyways).

## 3. Revealing Module Pattern

This is an evolution of the module pattern described above. The main difference being that we write all object’s logic on the private scope and then expose what we want trough an anonymous object. We can also change the private member's names when we map then to the public ones.

The revealing module pattern is one of the ways we can implement a module pattern. The differences between the revealing module pattern and the other variants is mainly the way we reference the public modules. As a result, the revealing module pattern is a lot easier to be used and changed. It can still prove to be fragile in certain scenarios, when we will use the objects on a inheritance chain, for example. The most problematic situations are:

1. If we have a private function referencing a public function, we can’t overwrite the public function. The private function will keep pointing private implementation and it will lead to bugs.
2. When we have a public member pointing to a private member and we try to overwrite the public member from outside the module, all other functions will still be referencing the private value, introducing bugs.

## 4. Singleton Pattern

When we want to allow a single instance of a class, we use the singleton pattern. For example, when we have a configurations object, we don’t want to create a new object each time it is called, it must always be the same, otherwise we could have different settings each time.

The random number generated is always the same, just as the values from config.

## 5. Observer Pattern

The observer pattern is very useful when we want to optimize the communication between separated parts of the system. It promotes an integration of the parts without making then too coupled.

you will find several different ways to implement this pattern, but the simpler case is when we have one emitter and lots of observers.

The emitter will execute all the operations to which the observers are subscribed. Those operations can be, subscribe to a topic, unsubscribe from a topic and notify subscribers every time something is published to a topic.

One variant to this pattern is the **publisher/subscriber pattern**, which is the one we will see on this text.

On the observer pattern, the emitter keeps all the references to the observers and call the methods directly on these objects. On the other hand, the publisher/subscriber pattern has channels that work as communication layer between the publisher and the subscribers. The publisher fires an event and just executes the callback sent to this event.

Here is a small example of the publisher/subscriber pattern.

This design pattern is specially useful when we want to respond to a single event on different places. Imagine you need to make several requests to an API and depending on the responses you will make other calls. You would have to nest several callbacks and this might be difficult to manage. Using the publisher/subscriber pattern you solve this situation in a much simpler way.

The problem with this pattern are the tests. It might get hard to test the behavior of the publisher and listeners.

## 6. Mediator Pattern

A pattern that is used a lot on decoupled system is the mediator. When we have different parts of a system that need to communicate on a coordinated manner, a mediator can be the best option.

The same way as real life, a mediator is an object that will be the focal point of communication between other objects.

At first sight the mediator and publisher/subscriber pattern look very similar. And, in fact, they are both used to manage the communication between elements. The difference is that the publisher/subscriber throws the events to the wind and forget about it, while the mediator will take care of each subscriber and be sure they deal with the message.

A good use case for the mediator pattern is the wizard. Say you have a long process of sign up on your system. Usually, large forms are broken into steps.

This is a way to make easier to do maintenance on the code and at the same time the user won’t be overwhelmed by a gigantic form. A mediator could manage the whole wizard, showing the use of different steps in tandem with the input from each step.

The obvious benefit from this pattern is the improvement in communication between the parts of the system. On the same way it happens on a debate, the mediator assures that each person has its time to speak and no one speaks out of order.

The mediator becomes a single point of failure, if it stops, everything stops. That is the main problems with this pattern.

## 7. Prototype Pattern

you must be getting tired of reading this, but JavaScript doesn’t support classes on its native form. Inheritance is made trough prototypes.

We can create objects that will be used as prototypes for other objects to be created. The prototype is a blueprint for objects that the constructor makes. Almost like we differentiate classes and objects in Java.

Let’s see an example for this pattern.

Note that inheritance by prototypes ends up bringing a improvement in performance as well, because both objects have a reference to the same method that is implemented on the prototype, instead of being implemented on each one of them.

## 8. Command Pattern

The command pattern is used when we want to encapsulate a call as an object. It is a way to keep separated the caller's context from the called.

Let’s say your JavaScript application has several calls to an API. Imagine now that the API changes. We don't want to change every place that interacts with the API.

That is where an abstraction layer to separate the objects that call the API from the objects that determine **when** to call it comes in. This way we don’t need to do a big change on the application, because we just have to change the call to the API on a single place.

A problem that arises with this pattern is that it creates an additional abstraction layer, and it may impact the performance of an app. It is important to know how to balance performance and code legibility.

## 9. Facade Pattern

The facade design pattern is used when we want to create an abstraction layer between what is show publicly and the internal implementation. It is used when we want to have a simpler interface.

This pattern is used, for example, on the DOM selectors of libraries as JQuery, Dojo and D3. These frameworks have powerful selectors that allow us to write complex queries on a very simple way. Something like `jQuery(".parent .child div.span")` seems simple, but it hides a complex query logic underneath.

Here again, every time we create an abstraction layer above the code, we might end up having a loss of performance. Mostly this loss is irrelevant, but is always good to be considered.

# Conclusion

Design patterns are fundamental tools for every JavaScript developer. They collaborate a lot when it’s time do maintenance on the code by making everything simpler and easier to understand.

This post is getting really long, if you want to know more about design patterns I recommend the classic book Design Patterns: [Elements of Reusable Object-Oriented Software](https://amzn.to/2XoLBSA) from the Gang of four and also the more modern [Learning JavaScript Design Patterns](https://amzn.to/2XBMZBs) from Addy Osmani. Both books are really good and worth the reading (links are not affiliated).

**_This is was a long article, if you read this far, please follow me here on Medium and consider sharing with your friends!_**