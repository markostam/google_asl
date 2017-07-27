# How Google Does ML
7/10/17

Josh Cagan - Google ML Research Engineer

## Intro

### Stages of ML

+ Define key preformance indicator (KPI's)
+ collecting data
+ building infrastructure
+ optimizing ML algo
+ integration

### Time Breakdown

+ very little time optimizing the algorithm
+ 25% building infra 25% collecting data
+ algorithms have legs, data is sticky

### Secret Sauce:

+ It's not technichal skills, it's how to strategize about ML
+ Technical skills is data and software engineering

### 10 ML Pitfalls

+ you thought training your own ML algo would be faster than writing SW
+ you haven't collected data
+ you haven't lookeda, but assume data is ready for use
+ you forgot to put and keep humans in the loop
  + send a small fraction of test data to humans to verify
+ you launched a product whose initial value-prop was its ML algorithm
+ you made great end to end ML system that optimizes for the wrong thing
+ you forgot to measure if your algo improves things in the real world
+ you confused the ease and value-add of using someone else's pretrained ML algo with building your own
  + how much of a benefit can you get from rebuilding the wheel? may be better to kickstart your work with pretrained algorithms and go from there.
+ you thought after research, production ML were trained only once
+ you want to design your own in-house perception or NLP algo

### What's the good news?
+ Most value comes along the way
+ ML does improve performance of everything once it gets there
+ If the process to build and use ML is hard for your company, it's hard for competitors too.
  + Winner take all markets
  + really powerful network effects because you just keep getting more data

### Value comes along the way
+ spend more time building SYSTEMS rahter than statistical model's we'll follow

###  Path to ML: 5 phases
+ Individual contributor
  + hq receptionist
+ Delegation
  + group of people performing task in parallel e.g. store checkout
+ Digitization
  + computer perform repeatable tasks e.g. ATM
+ Big data analytics
  + Using data to build operational & user insights e.g. Toyota Mfg
+ ML
  + Using data to automatically improve computer processes e.g. music recs
  + no longer a user that looks at the plot and updates the inputs

### Concrete Example

+ bose CEO buys everyone at company a spotify license BUT they can only listen to them thru bose filters
+ you get implicit data ie how long ppl listento music
+ then you also get additional data ie the genres of music ppl listen to which music sounds better thru filter etc

### Individual contributor phase

+ this is basically wizard of oz'ing

+ dangers of skipping
  + inability to get org investment to scale up to effort
  + product heads make big assumtions

### Delegation phase

+ increase number of employees to hundreds or millions
+ allows gentle ramping in investnment

+ dangers of skipping:
  + not forced to formalize the process and define success!
  + inherent diversity in human responses becomes a great testbed for product learning
  + great ML systems need humans in the loop - this is an opportunity to identify them
    + get HR practices in place

+ dangers of lingering too long
  + humnas are expensive
  + more ppl the more voices say automation wont work
  + organizational lock in, more stakeholders, the harder change becomes

### Digitization

+ build computer systems to perform mundane/repetitive parts of the process
  + travel agents etc
+ trades up front investment for lower marginal costs

+ dangers of skipping
  + even with a great ML algo you'll need all the infra of this step to be able to serve ML at scale
  + you've entangled IT projects with ML success and the whole project will fail if either does
+ dangers of staying here too long:
  + your competitors are collecting data and tuning their offers while you're not

### Big Data / Analytics

+ measure everything and MAKE IT EASY TO LOOK AT, if you can't look at it it doesn't exist
+ make it eassy to review summarize and deep dive
+ reiterate your definitioins of succes and tune the SW algorithms above

+ dangers of skipping:
  + you can't train your ML algo bc your data isn't clean
  + if you can't measure success, it's hard to tell if ML algo is improving things
+ dangers of staying here too long:
  + honestly not so big. google stayed here for years.
    + it's a white box, you can see why you are making decisions
  + limit complexity of problems you can solve

### ML Phase

+ measure everything about your internal ops and external users
+ make it easy to review summarize and deep dive
+ reiterate your definitions of success, and tune the SW algo above
+ automate feedback loop between measuring success and tuning sw
+ eventually outpaces humans ability to handle # of inputs and corner cases
+ generally we expect 10% kpi increase on top of human hand tuning
+ escape limitations of human cognition in solving our business problems
  + faster answers
  + mroe nuanced treatment of details
  + one "brain" learning from bns of interactions (one car = all cars)
  + all around mind blowing

### When is ML not the answer?

+ WHEN YOU DONT HAVE DATA
+ NLP has been slow to show promise

+ automating the engineer that's putting the parameters back into the model
+ it's nice to have a human that you can talk to and get answers from - transparancy
+ the human asymptote
