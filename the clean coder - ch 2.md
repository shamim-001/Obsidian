[![Shortform App](https://www.shortform.com/img/logo-dark.70c1b072.svg)](https://www.shortform.com/app)

[Discover](https://www.shortform.com/app)

[Books](https://www.shortform.com/app/books)

[Articles](https://www.shortform.com/app/articles)

[My library](https://www.shortform.com/app/library)

[Search](https://www.shortform.com/app/search)

# The Clean Coder

[Back to Technology](https://www.shortform.com/app/books/category/technology)

## Chapter 2: Quality #2—Practice Discipline

In the last chapter, we learned about the first quality of a professional—a commitment to learning. **The second quality of a professional is discipline—professionals adhere to personal rules and standards around the act of coding.** The rules aren’t always about the actual code; sometimes they’re about attitude and behavior while working.

Everyone’s rules will be different. In this chapter, Martin shares what works for him in case you’d like to adopt it, but he also encourages you to reflect on what else might work for you.

### Rule #1: Avoid Doing Damage

**The first rule is to avoid doing damage, and if you do create damage, to take responsibility for it by apologizing and learning from the mistake**.

A software developer can damage two things:

**1. The working of the software.** You damage the working by making a change that creates a bug that breaks the software. To avoid damage and take responsibility:

- **Personally and regularly test _all_ of your code.** Before you release your code to anyone, including Quality Assurance, make sure you know that it works. (Relying on QA to find problems is expensive, causes delays, and is lazy.) If you feel you don’t have time for testing on this scale, automate the testing. If you feel your code is too hard to test, write code that’s more easily testable. (See Chapter 4 for more on testing.)
- **Learn from bugs** so you can avoid making the same mistake in the future.
- **Reduce your debugging time.** Your employer pays the same for debugging time as coding time, so get it as low as possible by doing things right in the first place.

**2. The structure of the software.** You damage the structure by making the code difficult or expensive to change. To be professional and avoid damaging the structure, mercilessly and regularly refactor (edit) it to improve it.

- (Shortform example: If you notice that a piece of code is redundant, clean it up.)

Many people don’t like refactoring because they’re scared of breaking the code. If you test all of your code (as you need to do to avoid damaging the working), there’s no need to fear breaking anything. If something _does_ go wrong, your tests will catch it.

### Rule #2: Don’t Code While You’re Tired or Worried

The second rule is to avoid coding when you’re tired or worried. **If you’re not in a mental space in which you can concentrate, you’re going to make mistakes and have to throw out most of your work because coding is hard.** You have to do all of the following at the same time:

- Know what problem your code is addressing and how to fix it. You have to keep track of all the solution’s details as well as the mechanics of coding (what language you’re writing in, how the program you’re using works, and so on).
- Give your customer what she needs (which isn’t always what she asks for).
- Fit your code into what already exists. Your code can’t make the whole system more breakable or static, as you learned in rule #1.
- Craft your code so that other people can figure out what it does. This involves more than simply leaving explanatory comments—you need to actually structure the code in a way that a human can follow. (This might be the hardest part of coding.)
- Partition the system. Ideally, you want to divide a system into small pieces that don’t rely on each other, which is hard.

First, we’ll look at how to manage tiredness, and then, worry.

#### Decreasing Tiredness

Here are some techniques to decrease your tiredness levels:

##### Technique #1: Disengage and Recharge

**When you’re tired, you lose your ability to problem-solve and be creative.** Once you’ve used up all your focus (you will probably physically feel it), you need to recharge by disengaging and spending at least an hour doing something that doesn’t require focus. Your unconscious mind will continue to mull over the problem in the background. To disengage, you might:

- **Drive.** Driving doesn’t require creativity, but it requires you to use enough of your mind and body to pull your concentration off your work.
- **Exercise or do something with your hands.** While these activities do require focus (Shortform example: Carpentry requires being careful around sharp things), it’s muscle rather than mental focus. Practicing muscle focus can increase your mental focus.
- **Take a shower.** Martin often gets good ideas in the shower.
- Take a walk.
- Talk to a friend.
- Meditate.
- Nap.
- Read a magazine.
- Listen to a podcast.
- Look out the window.

##### Technique #2: Strategically Arrange Your Life to Make the Most Use of Your Focus

In the previous technique, we looked at what to do when you start to feel tired at work. Now, we’ll look at how to arrange your life so you can make your work time your most energetic time:

- **Sleep enough.** Martin needs seven hours of sleep to work an eight-hour day.
- **Use caffeine in moderation.** Caffeine improves focus, but if you have too much, you’ll get hyperactive and focus on the wrong things. Martin finds a morning cup of coffee and a lunchtime diet coke works most days.
- **Pace yourself.** Don’t use up all your energy at once.
- **Use your focus before it decays.** You lose your focusing abilities throughout the day even if you’re not using them, so code when you have them (as opposed to doing something like attending a meeting). When they’re gone, do something that requires less focus.

#### Decreasing Worry

There’s one technique for decreasing worry:

##### Address Personal Worries

**If you’re worried about something, part of your brain will be occupied with the worry instead of thinking about your code.** You might even physically feel the worry as a tightness in your chest or a sick feeling in your stomach.

- For example, when Martin tries to code while worried, he might be able to write a small amount, but he’ll always revert to concentrating on his worry and staring blankly at his screen.

**To avoid being distracted by worry, devote some time (often an hour) to addressing the worry.** Not all worries are solvable within an hour, but making some progress on them can reduce anxiety enough to let you work.

- For example, when Martin’s child was at home sick and he was worried, he’d call home and ask how the child was feeling.

It’s most professional to schedule worry-addressing time at home so that when you arrive at the office, you’re ready to give your best. But **if you’re unable to address something at home, and you can’t get anything done at work for thinking about it, it’s more productive to take an hour of office time to address the worry.** If you try to push through, you’ll just write garbage.

### Rule #3: Don’t Wallow in Writer’s Block

The third rule is to avoid getting writer’s block. When you’re feeling stuck, try the following techniques to get past the block:

- If the block is caused by exhaustion or worry, use the techniques for addressing these from the previous section.
- **Increase your content consumption.** Consuming creative content (like reading sci-fi novels) will help you output creativity—inspired by someone else’s work, you’ll want to create your own.
- **Pair program.** Working with someone else will nearly always refresh you. Martin feels a physiological change when pair programming.

### Rule #4: Avoid Time Pressure

**The fourth rule is to avoid or at least minimize time pressure—this is the best way to deal with it.** To do this:

**1. Adhere to your rules.** You’ll be most efficient if you don’t break things, don’t get stuck behind writer’s block, and so on.

**2. Use your crisis behaviors all the time.** In a crisis, you’ll use the most effective and efficient method of doing something. To achieve crisis levels of efficiency all the time, use your crisis behaviors in non-crisis times too.

- For example, if you don’t normally pair program except in an emergency, this shows that you think pair programming is the most efficient way to get something done. Pair program more often to be more efficient

**3. Say no to unreasonable deadlines**. See Chapter 3 for more on this.

**4. Watch out for manipulative client behaviors.** If a client does any of the following, they might be gearing up to put unfair pressure on you:

- **Describes the project as simple and easy.** This will put you in the wrong mental state.
- **Fails to discuss all required features.** The client might not _explicitly_ mention all required features. (Shortform example: They might ask for only one feature, but this feature requires other features to work.) If you try to call them on it, they might say you should have realized features were necessary because you’re a programmer.
- **Pushes deadlines.** Some clients will give you a short initial deadline so that you work quickly. Then, they’ll ask for more features and extend the deadline.

**No matter how well you employ the above techniques, you’ve inevitably going to encounter pressure.** For example, someone on your team might quit at an inopportune time. When you _are_ under pressure, you should:

- **Stay calm.** Getting stressed and rushing will only do damage, which will ultimately slow you down because you’ll have to go back and fix things. Instead, look at the big picture of the whole project, make a plan, and then keep up a steady pace toward your goal.
- **Talk to your coworkers.** Tell them you’re under pressure, share your plan to deal with it, and solicit their feedback.
- **Exaggerate your rule-following.** For example, if your normal workflow involves refactoring, refactor more than usual. You already know your discipline works—adhere to it.
- **Pair program.** Pair programming produces higher-quality code faster—your partner will help you focus, stay calm, and see the whole project.

### Rule #5: Avoid the “Zone” When You’re Working

The fifth rule is to avoid the “zone”—a state of mind that makes you feel focused, productive, and invincible. In reality, the zone is just a meditative state—parts of your brain shut off, which skews your sense of time passing and depresses your creativity. Being in the zone is useful when practicing, but not while working because **you’re not actually more productive or on your game when you’re in the zone**. You’ll write more code, but because you’ve got tunnel vision, you’ll probably have to revise what you’ve written so it fits into the larger structures.

If you feel the zone approaching, avoid it by:

- **Stopping work.** Go for a walk, check your email, or take a break.
- **Pair programming.** You can’t get hyper-focused on your code if you have to talk to someone.

### Rule #6: Be Careful With Music

The sixth rule is to deploy music carefully. **Many people think that music helps them concentrate, but this isn’t universally the case.** Sometimes, it even helps people enter the zone, which you learned is detrimental in the previous rule.

- For example, when Martin used to listen to music while coding, when he went back to look at his work later, he realized he’d put some of the lyrics from _The Wall_ into the comments. For him, listening to music uses up a part of his brain, axing that part’s ability to contribute to the code.

**If listening to music _does_ work for you, it’s fine to use it.**

### Rule #7: Finish Properly

**The seventh rule is to completely finish all tasks before declaring them “done” and to define “done” as “passed all tests”** (for more on tests, see Chapter 4). Don’t accept partial completion for any reason, including if you’re short on time.

Breaking this rule leads to a slippery slope—you’ll declare things “done” earlier and earlier in the process. “Done” will become meaningless.

- (Shortform example: If “done” only means that some code has been written, not that it actually works, “done” no longer provides any meaningful status update.)

### Rule #8: Give and Accept Help

**The eighth rule is to give and accept help—programming is so hard it requires more than one brain.** Despite this fact, many programmers have trouble with collaboration—there’s some truth to the stereotype that programmers are big-headed introverts who get into the field because they’d rather talk to a predictable computer than a messy person with emotions. **Even if you find collaboration hard, develop the discipline to follow this rule.**

#### Giving Help

There are two ways to give help:

**1. Respond when asked.** If people have questions, you must answer them. It’s fine to schedule _some_ alone or uninterrupted time, but you need to be available too.

- For example, you might decide that in the morning, no one can interrupt you, but your door is open all afternoon.

**2. Offer to pair program.** If someone seems to be having difficulty, offer to pair program with her even if she hasn’t asked. Expect to spend at least an hour (it may not actually take this long, but if you budget this amount, you won’t make your partner feel rushed). Even if you’re not experienced with whatever she’s working on, you can always offer a fresh perspective.

#### Receiving Help

There are two ways to receive help:

**1. Accept it when it’s offered.** _Always_ accept help, even when you’re under pressure. If the person isn’t helping after half an hour, then thank them and excuse yourself.

**2. Ask for help.** It’s unprofessional to waste time banging your head against the wall when resources are available.

### Rule #9: Deal With Interruptions Efficiently and Gracefully

**The last rule is to come up with a workflow for interruptions.** You’ll inevitably be interrupted, sometimes by people asking for help, and as you learned in the last rule, it’s your responsibility to graciously help them. Therefore, you need to come up with some strategies for quickly getting back into your work after an interruption. Here are some options:

- **Pair program.** When you get interrupted, your partner can keep track of your place and thought process, so that when you return, you can get right back to concentrating on your work.
- **Use a workflow that holds your place for you.** For example, in test-driven development (more in Chapter 4), you alternate writing short tests and short pieces of code. Because these steps are in such a strict order, when you leave and return to your workstation, you can quickly find exactly where you were and what you were in the middle of.

If you don’t like being interrupted because it pulls you out of the zone, remember rule #5: You’re not supposed to be in the zone in the first place.

### Example: How _Not_ to Be a Professional

When Martin was working for a start-up called Clear Communications, **he broke rule #1: Don’t code when you’re tired.** He was working 60-70 hour weeks, and one morning at 3 a.m. after 18 hours straight of work, he wrote an ugly solution to a timing problem. **If he hadn’t been tired, he would have realized it was the wrong solution, but at 3 a.m., it was the only thing he could think of, and it looked good.**

The solution was “sending mail”—Martin’s code sent a message to itself. This caused new timing errors, infinite mail loops, and plagued everyone else who worked on the system with problems for years.

[

Previous

Chapter 1: Quality #1—Commit to Your Professional Development

](https://www.shortform.com/app/book/the-clean-coder/chapter-1)

[

Next

Exercise: Follow Rule #2

](https://www.shortform.com/app/book/the-clean-coder/exercise-follow-rule-2)