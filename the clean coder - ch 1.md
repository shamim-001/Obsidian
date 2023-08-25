[![Shortform App](https://www.shortform.com/img/logo-dark.70c1b072.svg)](https://www.shortform.com/app)

[Discover](https://www.shortform.com/app)

[Books](https://www.shortform.com/app/books)

[Articles](https://www.shortform.com/app/articles)

[My library](https://www.shortform.com/app/library)

[Search](https://www.shortform.com/app/search)

# The Clean Coder

[Back to Technology](https://www.shortform.com/app/books/category/technology)

## Chapter 1: Quality #1—Commit to Your Professional Development

In _The Clean Coder_, expert developer Robert C. Martin explains how to be a programming **professional—an honorable, reliable employee who produces quality work (or takes responsibility for the rare times she doesn’t).** Professionals’ most important responsibility is to meet their employer’s needs.

Many people (including developers) don’t consider developers professionals, and this is partly because developers don’t act like professionals. Martin certainly didn’t, when he started his career—he missed deadlines, didn’t test code before releasing it, and was such a bad leader he got two people working under him fired. In this book, he shares the lessons learned the hard way, in the hopes that he can help you avoid making some of the same mistakes.

He’ll teach you about the six qualities and skills of a professional and how to develop them:

1. Commitment to professional development
2. Discipline
3. Honesty (around estimates and deadlines)
4. Communication (via testing)
5. Time management
6. Collaboration

And at the end, in an appendix, you’ll learn about some of the tools and programs that will help you master the skills and qualities.

Note: _The Clean Coder_ isn’t a how-to-code book; it’s a manual about how to behave on the job. While the book was written in 2011, its principles still apply—the tools of coding might have changed, but the actual work is largely the same.

### Shortform Note

_The Clean Coder_ was originally organized in 14 chapters and an appendix. We've reorganized the chapters to be more concise and logical. As a reference, here's a mapping of our chapter numbers to the original book:

- Chapter 1: Quality #1—Commit to Your Professional Development → Introductory matter and Chapters 1 and 6
- Chapter 2: Quality #2—Practice Discipline → Original Chapters 4, 11
- Chapter 3: Quality #3—Be Honest About Deadlines → Original Chapters 2, 3, 10
- Chapter 4: Quality #4—Communicate via Testing → Original Chapters 5, 7 and 8 and Appendix
- Chapter 5: Quality #5—Manage Your Time Well → Original Chapter 9
- Chapter 6: Quality #6—Collaborate → Original Chapters 12, 13, and 14
- Appendix → Appendix

Because the book is written for coders who want to be more successful, the author assumes a certain level of knowledge about coding and doesn't define terms. This summary mostly follows the author's lead.

### Commitment to Professional Development

**The first quality of a professional is a commitment to professional development.** The tech industry moves quickly, and professionals realize that if they aren’t continually improving their existing skills and learning new ones, they’ll lose touch with the cutting edge, be unprepared for change, and narrow their resumes.

#### Professional Development Is _Your_ Responsibility

The hours you put into your day job rarely contribute to your professional development because at work, you often perform tasks and skills you already know how to do. Therefore, to be a professional, **you should spend 20 hours per week of personal time on improving your programming skills and learning new ones.**

- (Shortform example: If you’re a front-end web developer by day, you won’t have any opportunity to practice working the back end, so you’ll need to learn those skills on your own time.)

**Sometimes, your employer will contribute to your development, but you should consider this a _favor_**, not something you’re entitled to.

- For example, your employer might provide you with a book or send you to a training conference.

Similarly, **sometimes you need to learn something that would also benefit your employer. In this case, it’s reasonable to dedicate part or all of your 20 hours to it.**

- (Shortform example: If you need to learn a new programming language for a project your employer assigned you to, knowing this language will open new career avenues for you, so it’s worth learning in your spare time.)

**Putting in these extra hours won’t cause burnout**—if you’re a software developer, you’re probably passionate about coding, so 20 hours of practice will feel like doing a fun hobby. (If you don’t want to put in this time, don’t call yourself a professional.)

#### Improving Existing Skills

**A large part of improving your existing skills involves practicing them so you can perform them quickly and instinctively.** The goal is to get the unconscious part of your mind to recognize a problem and your body to instinctively react to it (for example, by hitting a particular combination of keys). Then, the rest of your mind is free to focus on strategy and problem-solving.

**Speed is particularly important these days.** Decades ago, programmers didn’t need to be fast with their keystrokes or mouse movements because computers were the limiting factor—they took a long time to compile (transform human-readable code into machine-readable code) and debug. Today, computers are fast, and programmers are the holdup.

There are two venues for practicing:

##### Venue #1: The “Coding Dojo”

The “coding dojo” is a collection of practice exercises that are inspired by martial arts (in martial arts, a dojo is a training space). Here are some of the exercises:

**Exercise #1: Kata.** In martial arts, a kata is a choreographed sequence of moves that would be one person’s side of a fight. The goal is to make the movements instinctive so that if you do get into a fight, your body does the sequence automatically.

Programming katas are similar—**they're choreographed sequences of keystrokes and mouse movements that solve a particular coding problem.** The goal isn’t to practice solving the problem (for most katas, you’ll already know the solution). Instead, it’s to practice the physical movements required for the solution and to train your mind to trigger the appropriate muscle memory when it identifies a specific problem.

- (Shortform example: For example, a kata might be to write a function that prints out the numbers 1-100 and replaces any numbers divisible by three with the word “fizz,” any numbers divisible by five with the words “buzz,” and any numbers divisible by both three and five with the word “fizzbuzz.”)

Katas are good for learning:

- Navigation idioms and hot keys
- Problem and solution pairs
- Test-driven development (we’ll look at this in Chapter 4)

**You should do one kata in the morning and one in the evening,** and each should take around 10 minutes to complete. You should vary which ones you practice to keep them all sharp and you can find many katas at [Code Kata](https://katas.softwarecraftsmanship.org/). When you get really comfortable, try setting a kata to music.

**Exercise #2: Wasa.** In jujitsu, wasa is a two-person drill in which one partner acts as the attacker and the other as the defender. Each person performs choreographed movements, and then they switch parts.

The programming version is ping-pong—**two programmers practice together. One programmer writes a test, and the other writes code that will pass it.** Then, they switch jobs.

This can be done with a kata or a new programming problem. If using a kata, the partners can critique each other’s memorization and execution of the physical movements. If it’s a new problem, the test writer can control the difficulty level.

- For example, the test writer can write into the test that it needs to be completed within a time limit. The code writer will have to come up with a solution that doesn’t take the computer too long to execute.

**Exercise #3: Randori.** In jujitsu, randori is unchoreographed combat practice.

The coding version is more like group wasa. **The first person writes a test. The next person writes code that will pass the test and writes a new test. And so on.** This will help you learn about other people’s problem-solving methods.

##### Venue #2: Open Source

Open-source projects provide a great opportunity for practice because they have real stakes. The project has a real-world application and someone else cares about it.

#### Learning New Skills

##### How to Learn

Once you’ve learned to improve your existing skills, it’s time to learn new ones. The best two ways to learn, in order of effectiveness, are:

**1. Teaching.** Teaching forces you to translate your knowledge into something you can communicate (like words), which in turn forces you to internalize the information. (For more on teaching, see Chapter 6.)

**2. Collaborating.** Collaborating means programming and practicing with another developer. You’ll learn from her and she’ll help you notice your mistakes. (For more on collaborating, also see Chapter 6.)

You can also learn by reading, attending conferences, and interviewing people.

##### What to Learn

Now that you know how to learn, what topics should you tackle? You should learn:

**1. Industry history.** You should learn all the techniques, ideas, jargon, tools, and niches of the last 50 years (almost all of which are still relevant). At a minimum, you should be familiar with:

- Methods, such as Waterfall
- Design patterns, such as GOF and POSA
- Design principles, such as SOLID
- Disciplines, such as pair programming (when two people work together on the same computer)
- Artifacts, such as flow charts and Petri Nets

**2. New developments.** Keep on top of the cutting edge of the industry. Learn new programming languages.

**3. Your employer or customer’s business and field.** When you’re programming a tool for a business in a particular field, you should know about the field yourself. (Shortform example: If you’re building a system for a law firm, then you need to learn something about law.) That way, if the business, unaware of the nitty-gritty of technology, requests a specification that doesn’t make sense or will be ineffective, you can advise. Think of the business’s problems as your problems—your goal is to come up with whatever solution will actually help, not just to follow instructions.

**4. Humility.** Programming comes with some inherent arrogance—when you create something, you’re playing god. You should take pride in your work and be confident, but also know that you’ll inevitably make mistakes because everyone does. If you fail, accept the consequences and laugh at yourself. Never attack other people for making mistakes.

**5. Error sense.** Error sense is becoming aware of when you make a mistake. The faster you can notice your errors, the faster you can learn from them.

- For example, when Martin was learning to type blind (without looking at the keyboard), he started by typing up programs onto cards. Once he finished each card, he’d look at it for mistakes and if he found one, throw it out. After a few hours of practice, he could feel when he hit the wrong key, immediately throw out the card, and start fresh.

#### Example: How to Be a Professional

Martin has practiced a 30-minute kata called _The Bowling Game_ for years. **He’s run through it so many times he “could do it in his sleep.”** Over the years, he’s streamlined the exercise so he doesn’t use any more keystrokes than necessary and has finessed the algorithm structure and variable.

[

Previous

1-Page Summary

](https://www.shortform.com/app/book/the-clean-coder/1-page-summary)

[

Next

Chapter 2: Quality #2—Practice Discipline

](https://www.shortform.com/app/book/the-clean-coder/chapter-2)