# Ethan's Meeting Memo: Thursday, 2025 October 16

(I think Allie will be posting hers in the Discord server soon?
This will be mine anyways.  I'm putting something down and hopefully
by the end of this weekend we can all have something to look at.
**Edit October 21**: I think everyone will just have to look at
mine then, oh welp... :x)


## Survey and Logistics

The plan is to meet bi-weekly.  And I think Allie will be booking
the room next week as well since she is the leader and has done it
and therefore she is likely the one to do it next time?

The following members are confirmed to be in Team 17 according
to [Allie's finalized roster of the team emailed to the club](https://discord.com/channels/1428212879026552872/1428212880184184854/1430371438048710759):

 - Allie
 - me (ethan :P)
 - Bridget
 - Rose
 - Madhav
 - Saksham (Agent),

For the people who showed up at the meeting: I recall there was one
Master's student in computer science, me as a sophomore/2nd year,
and the leader a junior/3rd year; then the rest are freshmen/1st year.
(Most people are freshmen.)

In terms of programming experience I can't say I recall much... except
hearing a lot of Python and Java; and from the Wednesday club meeting
I think people said they knew React.js.  So for applications I was
thinking we'd go with [Electron](https://www.electronjs.org/), and
for web services we'd go with some JS framework (Vue.js, Nuxt.js, Next.js)
or Svelte over MySQL and possibly a Python API backend.  (I myself don't
understand Django that well and I think the learning curve can be a bit steep.)

The primary means of communication would still be Discord.


## Project Brainstorm

![](whiteboard.jpg)

We looked at a few existing projects students at UW had made.

*   [MadHousing.com](https://www.madhousing.com/): Housing info site.
    Made at **SDC Club** Spring 2022 ([source](https://www.madhousing.com/about)).
    Looks like Next.js + Tailwind CSS (judging from the HTML source code),
    hosted on Vercel.
*   [wisc.AlexT.se](http://wisc.alext.se/): Grading distribution site.
    Made by one person ([Alexander Tse](https://www.linkedin.com/in/alex-tse/),
    from which we know the site is built with Python and React.)
    *Maybe* open source but I couldn't find the source code.
    Active to present.
*   [MadGrades.com](https://madgrades.com/):  Yet another grading distribution site.
    [Open source](https://github.com/Madgrades/madgrades.com).  Looks like Next.js
    to me (I can't read code).
*   [UWCourses.com](https://uwcourses.com/): Course-selection website
    made at CheeseHacks Fall 2024, active to present.  Built with
    [SvelteKit](https://svelte.dev/docs/kit/introduction) (among other things
    I definitely don't understand like how they made the graph).
    [Open source](https://github.com/twangodev/uw-coursemap) and AGPL.
*   [UWMatch.com](https://www.uwmatch.com/): made by a few people
    from the end of December 2024 to present.  Build with Svelte backed by
    [FastAPI](https://fastapi.tiangolo.com/) + NoSQL [MongoDB](https://www.mongodb.com/),
    (with an non-negligible amount of help from Cursor), also hosted on Vercel.
    Closed source.  **Has had the desire to expand to a centralized club
    (student org) hub.**

Apparently doing something UW-related is pretty trendy.
