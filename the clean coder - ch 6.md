[![Shortform App](https://www.shortform.com/img/logo-dark.70c1b072.svg)](https://www.shortform.com/app)

[Discover](https://www.shortform.com/app)

[Books](https://www.shortform.com/app/books)

[Articles](https://www.shortform.com/app/articles)

[My library](https://www.shortform.com/app/library)

[Search](https://www.shortform.com/app/search)

# The Clean Coder

[Back to Technology](https://www.shortform.com/app/books/category/technology)

## Chapter 6: Quality #6—Collaborate

In the previous chapter, we looked at the fifth quality professionals possess: time-management skills. Now, we’ll look at the final quality: the ability to work with others. First, we’ll look at teamwork, then mentoring.

### Teamwork

**Professionalism involves doing whatever produces the best possible work, and the best work is achieved via collaboration.** (Even if you’re one of the rare people who works best alone, you hamstring your team’s work—and as a result, hurt your employer—when you refuse to collaborate.)

#### Putting Together a Team

There are two approaches to putting together teams:

**1. Build the team around a project.** Assign programmers, analysts, testers, and a project manager to work on a project for a percentage of their time. The members can belong to other teams working on other projects at the same time.

**2. Start with the team.** Create a team of programmers, analysts, testers, and a project manager, and then assign the team to work on multiple projects together. Usually, this kind of team consists of 12 people: one project manager, two testers, two analysts, and seven programmers. Here are their jobs:

- **The project manager** keeps track of and communicates the schedule and priorities.
- **Analysts** come up with business requirements and write acceptance tests (usually, testing for how it’s supposed to work).
- **Testers** come up with technical requirements and write acceptance tests (usually, what will go wrong).
- Someone might additionally take on the role of **coach** to keep the team adhering to discipline.

**Approach #2, starting with a team, is the better option** because:

- **It takes time for a team to become effective.** It can take six months to a year for a group of people to gel (learn how to work together by leveraging strengths and weaknesses, supporting each other, and so on).
- **Teams that work on multiple projects can better allocate strengths and weaknesses.** (Shortform example: People who are good at debugging can work on the debugging aspects of all the projects.)
- **The team can quickly adjust priorities.** If one of the team’s projects goes into crisis, the team can pause on their other projects and focus on that one. (Pausing a team created using approach #1 would be expensive and chaotic because management would have to pull everyone on the team off all their other projects.)

#### Working as a Team

Once a team is assembled, here are some techniques for effective collaboration:

**1. Share code.** Anyone should be able to make improvements to any part of the code. That way, people can work with each other and learn from each other.

**2. Pair program.** Pair programming is not only efficient, but also allows people to share knowledge about both the system and the business; familiarity with other people’s work allows team members to take over for each other in emergencies. Additionally, pair programming is the most efficient way to review code.

**3. Work physically close to each other.** Face each other when you’re sitting around a table, and be close enough to talk and read body language.

#### Exceptions to Teamwork

There are a few times when working alone is most appropriate:

- You need to reflect on a problem.
- A task is short or unimportant, so getting help would be a waste of resources.

### Mentoring

In the previous section we discussed the importance of teamwork. Next, we’ll discuss another aspect of collaboration—mentoring. **It’s the professional and ethical duty of experienced programmers to mentor newbies, and it’s newbies’ duty to ask for mentorship.** This is because inexperienced coders can cost a company a lot of money and do a lot of damage.

- For example, software controls some high-stakes systems such as banking systems.

**Mentoring teaches technical skills and professionalism, and instills craftsmanship**—the mindset of attitudes, techniques, values, and disciplines required for coding. (Craftsmanship is contagious, so when mentors lead by example, mentees pick it up.) **Mentoring is the only way to learn many of these skills—school and courses can teach theory but not practice.**

Martin’s ideal mentoring system includes the following roles and responsibilities.

- **Masters** have over 10 years of experience with various systems and languages, have led at least one important project, and are skilled coders, architects, and designers. They might be managers or have been offered management jobs, but they’re up-to-date, _technical_ experts. (General managers or project leads who don’t know how to code shouldn’t act as masters.) Masters mentor journeypeople.
- **Journeymen and women** have around five years of experience with one system and language. They’re learning about additional systems and languages, and about teamwork. They mentor less experienced people.
- **Apprentices** have less than a year of experience. They don’t have their own tasks—they help journeymen and women and regularly participate in pair programming to learn professionalism and skills such as TDD. If apprentices do well, a journeywoman will recommend promotion and a master will approve or deny the recommendation.

**The level of mentorship required depends on experience.** The less experienced an apprentice or journeywoman, the more supervision they need. Apprentices should have no autonomy, and very experienced journeymen and women should be peer-reviewed.

### Example: How _Not_ to Be a Professional

When Martin was consulting for a company that made printers, each programmer worked on a separate part of the device (feeder, stapler, and so on). **The programmers were possessive of their code and never shared it with their coworkers—they didn’t embrace teamwork.** As a result, there was wasteful duplication in everyone’s code.

[

Previous

Exercise: Reflect on Meetings

](https://www.shortform.com/app/book/the-clean-coder/exercise-reflect-on-meetings)

[

Next

Appendix: Programming Tools

](https://www.shortform.com/app/book/the-clean-coder/appendix)