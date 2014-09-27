# Why changing just a field can take long time? #

This is one of the questions UI developers get when the development on particular story is going on, especially in Agile.

So let me tell you the story of UI development...

A Sprint is planned and the the task is assigned to create two screens. The notable thing is, each screen have a same looking form having multiple complex fields and other details specific to each screen.

Developer gets this requirement and starts the work.

After 2 days, there is a change anticipated. It has occurred to business that a particular field is to be displayed only for one screen and not in other screen.

Developer gets this, says OK and accommodates his timeline accordingly.

Now again two days later one more requirement pops in that another field is to be displayed as a multi-select box in one screen and read-only field in other screen.

When these kind of things happen, nobody thinks about the state of our beloved developer's coding environment and it's structure.

**Lets see the developer's side...**

Looking at the basic design and architecture of application, it is normally ambitious, lets say MVC. Now to maintain the soul application as whole and being a good developer, he/she strives to maintain this so as to improve the overall quality. Note that this is continuous process and not a one time task.

When first time developer captures the requirements, he plans out something.

So if there are two screens, there will be model, view and controller for each screen and there will be a reusable form that can be used by both the screens and form in-turn having model, view controller.

Yes. Now this is cool. this is a good design and I know exactly what to do.. (developer thinks)

After two days, when developer has not even scratched the ground, our first change is revealed. But to confirm this with 100% surety, developer calls out a meeting; all the participants gather and discuss. Finally its confirmed that the change is to be made.(Note that at least half of the day is wasted in these activities)

OK, so there is only one field that is differentiating. That means I can have a configuration option for reusable form and still can make this happen without extending too much time and maintaining the design-soul of application. (...again thinks the developer).

*[Note that outer world doesn't know about whats going on in developer's mind]*

But when further changes are thrown in, the developers code structure starts breaking.

It appears to him/her that the re-usable form that was planned on the first day is no more reusable and had to broken into two separate things (each having m-v-c). There appears some cleanup to be done and some changes to be reverted and again some thing else is to be planned out.

Holy cow! I am screwed now.. (thinks the developer-in-pain).

He/She shouts, do not bring in those changes. But nobody listens...

And the people come with the question.....

**Why changing just a field is taking (long) time?**

Developer can not explain all these things every time. Every time scenario can be different. There are too many things a developer has to take care of.

Its not "just" what you see on screen. There is a soul behind that screen which makes that alive. This is similar to the difference between a dead man and an living man. Both will look same but there is a difference of soul. Think of UI/screens in the same way. A User-Interface without the background architecture and code is as good as dead.

**And its not just about changing the field its about changing the soul.**

Now question is then why don't developers strike back.

Because developers are not business people. They are enthusiasts. They strive to make things work. They are always positive about building new things. So giving the business arguments is not part of their integral mechanism. And explaining technical difficulties is always a difficult thing to do.

**So, in my opinion, best thing to practice in projects is to give developers a clear and almost-constant line-of-sight. This only thing can boost a lot of productivity**  

----------
*Note:*

*The views are personal and based on my experience in the field of Front-end development. Any comments / suggestions are welcome.*

*This article is also present on,*  
[https://www.linkedin.com/pulse/article/20140927154524-186305264-why-changing-just-a-field-can-take-long-time](https://www.linkedin.com/pulse/article/20140927154524-186305264-why-changing-just-a-field-can-take-long-time)