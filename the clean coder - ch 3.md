[![Shortform App](https://www.shortform.com/img/logo-dark.70c1b072.svg)](https://www.shortform.com/app)

[Discover](https://www.shortform.com/app)

[Books](https://www.shortform.com/app/books)

[Articles](https://www.shortform.com/app/articles)

[My library](https://www.shortform.com/app/library)

[Search](https://www.shortform.com/app/search)

# The Clean Coder

[Back to Technology](https://www.shortform.com/app/books/category/technology)

## Chapter 3: Quality #3—Be Honest About Deadlines

In the last chapter, we looked at the discipline and rules all professionals adopt. **The next quality of a professional is honesty**, especially about estimates and deadlines.

Whenever you’re programming something for someone, they always want to know when it will be done. **Most of the time, you won’t know exactly how long something will take, so you’ll provide an estimate instead of a commitment** (guarantee). Estimates have the following qualities:

**1. They aren’t promises** (though businesses often interpret them as such, which is why there’s often conflict between programmers and businesspeople).

**2. They aren’t single numbers—they’re probability distributions.** They factor in the following _three_ numbers:

- **Best-case.** If _everything_ goes right, you’ll be finished in this amount of time. This number should be _very_ optimistic—there’s only a 1% chance that you’ll make this number.
- **Nominal.** This is the amount of time you think is most likely.
- **Worst-case.** If _everything_ goes wrong, you’ll be finished in this amount of time. This number should be _very_ pessimistic—there’s only a 1% chance that this is how long the task will take you.

Missing an estimate _isn’t_ unprofessional because estimates aren’t guarantees. However, **professionals make their estimates as accurate as possible using well-tested estimation methods.**

### Estimation Methods

There are many methods you can use to give your managers and clients an estimation, and we’ll cover three of the options.

#### Method #1: Wideband Delphi

The first estimation method is called wideband delphi and uses consensus to make estimations by pooling the experience and knowledge of several people.

Here are the steps:

**1. Everyone discusses a task**—what it involves, how to do it, and possible delays or hiccups.

**2. Individually and privately, everyone estimates the nominal time.** Be objective and honest about these dates—don’t factor in hope or miracles. Hope is dangerous because it leads people to create unrealistic schedules and then when things don’t work out, people’s reputations suffer.

**3. Everyone reveals their estimate at the same time.** This is so that no one’s estimate influences anyone else’s.

- Example #1: Everyone might represent their estimate by flashing a count on their hands, with each finger held up representing a day. (If the estimate is a longer time frame than days, each finger could represent multiple days.)
- Example #2: Everyone might reveal their estimate by flipping a card that shows how long they think a task will take. (This method is called planning poker.)

If there are any major discrepancies, the conversation continues.

- For example, if everyone holds up three or four fingers, that’s essentially consensus. If everyone holds up five and one person holds up zero, there needs to be a conversation.

**4. After the discussion, repeat steps 2 and 3 until everyone reaches a consensus.**

**5. To determine the best-case estimate, repeat only steps #2 and #3. Take the lowest estimate.**

**6. To determine the worst-case estimate, repeat only steps #2 and #3 and take the highest estimate.**

##### A Variation on Wideband Delphi

There’s another version of wideband delphi you might find useful for estimations:

**1. Write all the tasks onto cards and spread the cards out randomly on a surface.**

**2.** As a group (but without talking), **everyone arranges the cards in order of how long they think each of the tasks will take.** Anyone can move any card, and once a card has been moved a certain predetermined amount of times, it’s taken off the table and the group will discuss the task until they agree on an estimated time.

**3. Sort the cards into approximate time frames.** Usually, the buckets are 1, 2, 3, 5, 8, and these numbers can represent weeks, days, or points (units of complexity). (Shortform example: One complicated feature might be assigned 10 points, while a simpler feature would only be worth one).

#### Method #2: Program Evaluation and Review Technique (PERT)

**The second estimation method is the program evaluation and review technique (PERT).** While it doesn’t formally involve consulting others like wideband delphi, feel free to ask your teammates and the people around you to weigh in because their perspective might improve the accuracy.

Here are the steps:

**1. Create your distribution** by coming up with the best case, nominal, and worst-case numbers.

**2. Describe the probability distribution using the following formula**: (Best + (nominal*4) + worst)/6

- For example, if your best-case number is 3, your nominal is 5, and your worst is 10: (3+(5*4)+10)/6=5.5

Most of the time, this calculation will return a pessimistic-ish number because the right side of the distribution curve will be longer than the left.

**3. Calculate the standard deviation (how much uncertainty there is)** using this formula: (Worst - best)/6

- For example, continuing to use the numbers above, (10-3)/6=1.1666…

**4. Express the estimate as a range.** The task will take the probability distribution amount of time plus or minus the standard deviation.

- For example, the task will take 5.5 days ± 1.2 (rounded) days. Therefore, it will take between 4.3 and 7.2 days.

##### Using PERT to Estimate Time Required for Multiple Tasks

You’re rarely working on just one task at a time. You could estimate how long doing all your tasks would take by adding up all the nominal estimates, but there's a more accurate way that takes into account the uncertainty surrounding doing multiple tasks at once.

To do the calculation:

**1. Follow steps 1-3 above for each of the individual tasks.**

**2. Add the probability distributions (calculated in step #2 of PERT) together.**

- For example, if Task A has a probability of 4, Task B has 5, and Task C has 6, the calculation is: 4+5+6=15.

**3. Use the following formula to calculate the standard deviation of the group of tasks:** √(Task A standard deviation^2 + Task B standard deviation^2 Task C standard deviation^2 …)

- For example, if all the tasks have a standard deviation of 0.5, the calculation is: √(0.5^2 + 0.5^2 +0.5^2)=0.87 (rounded)

**4. Express the estimate as the step #2 number plus or minus the step #3 number.**

- For example, doing the group of tasks will take 15 days plus or minus just under a day, so between 14-16 days.

#### Method #3: Law of Large Numbers

The law of large numbers states that **if you break a big task into smaller chunks and estimate how long each chunk will take, adding up the chunk times will give you a more accurate estimate than simply estimating the big task as a whole.** This is because the errors in small tasks compound when you do the math, which is more realistic, because uncertainty also compounds in real life.

### Sharing Your Estimates

Once you’ve calculated your estimates, it’s time to share them. Once you do, **there’s always the possibility that people won’t like them and will want something done faster.** If this happens, you have three options, not all of which are professional:

#### Option #1: Saying “No” (Professional)

Saying no has a bad rap, but it’s the most professional thing to do in many situations. **If it’s impossible to get something done properly (adhering to discipline) by a certain deadline, and you say anything other than no, you’re essentially lying.**

Here are some of the situations where you might think you can’t say no, but in reality, it’s the right thing to do:

**1. When it’s technically _possible_ to get the job done, but only if you do it badly.** Doing damage is unprofessional—remember, your first commitment should be to your standards. (Martin’s experience shows that breaking discipline is always less productive—when a hurried developer writes messy code, all the other developers are slowed down too as they navigate the mess.) If the only way to get something done is to skip testing or write messy code, say no.

**2. When the adversary is your manager.** Your job isn’t to follow your manager’s orders; it’s to defend your objective, which is to have enough time to do a professional job. Your manager expects defense from you.

**3. When you want to be a team player.** Being a team player means doing your part of the work well, helping others, and communicating truthfully. It doesn’t help your team to agree to do something impossible on their behalf. It also doesn’t help your team to let them fail because they’ve ignored your “no”—if they refuse to acknowledge your answer, speak to someone higher up.

- (Shortform example: When programmer Fred told his manager Annalise that meeting a project deadline was impossible, Annalise ignored him and told the CEO that the deadline was fine. Fred has copies of the multiple emails in which he explained the situation to Annalise, so when the deadline comes and the project isn’t done, he could cite these to the CEO to show Annalise was the problem. Instead, as a professional, what he should do is force Annalise to tell the CEO the truth. Fred might do this by threatening to talk to the CEO himself.)

**4. When someone begs, cajoles, or casts you as a hero.** Accolades and glory are tempting. You don’t have to swear off heroism, just swear off working unsustainable overtime. If you really want to be a hero, do the job properly—meet both a _reasonable_ deadline and the budget.

**5. When you’ve already said yes.** Sometimes, you’ll say yes to a project that has hidden complications. Once you discover that the complications will affect your ability to do a job well, you can say no in light of the new information, even though you’d previously agreed.

**It’s especially important to say no in high-stakes situations** (such as if your company will fail if the software doesn’t work). This is because high-stakes situations are when managers most need accurate information and honesty.

##### Explaining Yourself

**You don’t need to explain why you’ve said no.** What’s important and relevant is that something is impossible—your manager doesn’t need to know why to make decisions or rearrange a schedule. If your manager is reasonable and has a lot of technical knowledge, you can explain if you want to, which will usually produce one of the following reactions:

- **The manager, knowing the reasoning, will be better able to accept the answer.**
- **The manager will disagree with your conclusion.** She might tell you to skip a time-consuming step such as testing (which you can’t do because it would be unprofessional) or otherwise micro-manage.

#### Option #2: Saying You’ll “Try” (Unprofessional)

**Never agree to “try” to do something in a time period shorter than your estimation.** The word “try” has multiple definitions and implications, none of which is honest:

**1. You will apply extra effort.** If you agree to try to get something done faster, it implies that you haven’t been giving the project your full effort up until this point. You have an extra energy reserve, or a new plan, or a behavioral change you’ve been holding back. If you’re a professional, you’ve _already_ been throwing everything you have at the project. Therefore, there is nothing else _to_ try, so by promising to do so, you’re lying and making a commitment you won’t be able to keep.

**2. You really mean “maybe.”** If this is the case, you should be honest about your uncertainty. If someone insists on a yes or no, and you’re not sure, say no.

**3. You really mean “yes.”** The person who’s saying “try” rarely means “yes,” but it’s often what the listener hears.

#### Option #3: Saying “Yes” (either professional or unprofessional)

**If you say yes, you’re committing to getting something done by the date you promised, no matter what it takes** (overtime, skipping family vacations, and so on). It’s unprofessional to say yes to something you’re not sure you can achieve because other people are going to plan around you. If you miss a commitment, it’s a huge blow to your reputation.

On the other hand, **it _is_ professional to ask to change the parameters of the task so that you _can_ say yes.** (You cannot say yes without something changing because you already considered every factor during your estimation.)

- For example, you might ask to reduce the scope of the project so that there’s less to do and you can finish in a shorter amount of time.

One of the parameters you _might_ change is your working hours, but working overtime will tire you, so it has limitations:

- What you get done won’t be proportional to how much time you throw at it—for example, if you work 25% more hours, you won’t get 25% more work done.
- If overtime would be required for more than two to three weeks, it won’t work.

Therefore, don’t agree to work overtime unless:

- It won’t significantly impact your personal life.
- It’s required for no more than two weeks.
- There’s a backup plan. Your boss must have a plan for what to do if working overtime isn’t enough to get the project done.

##### How to Say Yes

According to consultant Roy Oshervoe, there are three stages to saying yes and committing:

1. **Saying yes.** Many people _say_ yes, but don’t mean it. (Shortform example: People often say things like, “I really need to eat more vegetables.” They probably don’t even want to eat more vegetables.)
2. **Meaning the yes.** Few people get to this stage, often because they think the commitment is impossible or depends on someone else.
3. **Carrying out the yes.** Only professionals get to this stage.

You can help yourself reach the last stage by paying attention to the language you use. Say “I will” instead of should, need, wish, hope, let’s (all of these words abdicate responsibility). Once you’ve said “I will,” you’re accountable—whoever you said it to will know that if it doesn’t happen, it’s your fault. Fault feels bad, so you’ll be motivated to do what you said you would.

**Don’t commit to things you can’t control.** If you can’t get something done without the help of someone else, don’t commit because you have no way of following through. Instead, commit to something that will get you _closer_ to getting something done.

- (Shortform example: If you’re building a website and you can’t finish until the design department gives you the color palette, instead of committing to finish the website, commit to meeting with the design team about the color palette for an hour.)

### Breaking a Commitment

There will be times when you can’t make a commitment because life gets in the way. **Everyone is late at some point in their lives, and the best way to manage this is to regularly assess and communicate:**

**1. Update your estimates every day and share them.**

**2. As soon as you realize you can’t make a commitment, tell everyone** who’s depending on you. The earlier you tell them, the more time they have to come up with a backup plan. Someone else might be able to take over the commitment, the team might be able to reassess priorities, or you can make a new commitment.

- For example, if you’re going to be late for a team meeting because your car broke down, call your team right away so they can reschedule, someone else can do your part of the presentation, or they can cancel the meeting and work on something else instead.

**However, if someone makes a commitment on your _behalf_** (for example, your employer promises a customer something without talking to you about it first), **professionalism requires you to help the promiser meet the commitment, but professionalism _doesn’t_ require you to take ownership of the commitment.** If you can’t meet the commitment, _you’re_ not breaking it, the promiser is. _She_ must take responsibility.

### Example: How _Not_ to Be a Professional

John worked for an employer that won a bid to make an app for a major retailer in two weeks. **John said yes even though he knew two weeks wasn’t long enough to do the job properly.** **He broke discipline to try to get the project done faster**—his code was messy and he didn’t test it because errors would demotivate him. **He worked 20-hour days and “finished” the app by the deadline, but he’d done damage**—the structure of the code was rigid and hard to change. When the client extended the deadline and requested a new feature, it was very hard to implement.

[

Previous

Exercise: Follow Rule #2

](https://www.shortform.com/app/book/the-clean-coder/exercise-follow-rule-2)

[

Next

Exercise: Estimate Using the PERT Method

](https://www.shortform.com/app/book/the-clean-coder/exercise-estimate-using-the-pert-method)