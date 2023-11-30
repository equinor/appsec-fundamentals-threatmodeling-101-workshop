<!-- markdownlint-disable MD033 -->

# What are we working on? </br>🏭

---

## Exercise 0

❓ What pops into your head when you hear "Cookies"? <!-- .element: class="fragment" data-fragment-index="1" -->

- Write it down silently (1 minute) <!-- .element: class="fragment" data-fragment-index="1" -->
- What did you write down? <!-- .element: class="fragment" data-fragment-index="2" -->

<hr>

The mix of your past, your feels, and your headspace plays a big part in how you view things. We need some neat strategies to help us sync up 👇 <!-- .element: class="fragment" data-fragment-index="3" -->

---

## Purpose of ™️Models / Diagrams

<div style="font-size:0.8em">

- Clarify Ideas: Simplify and clarify complex concepts. Expose thinking<!-- .element: class="fragment" data-fragment-index="1" -->
- Scoping tools: What's in, out, boundaries<!-- .element: class="fragment" data-fragment-index="2" -->
- Enhance Teamwork: Improve collaboration and understanding across teams<!-- .element: class="fragment" data-fragment-index="3" -->
- Identify Issues: Spot problems early and plan solutions<!-- .element: class="fragment" data-fragment-index="4" -->
- Serve as Reference: Act as a documentation of processes for future reference<!-- .element: class="fragment" data-fragment-index="5" -->
- Forecast Outcomes: Predict the effects of changes and decisions<!-- .element: class="fragment" data-fragment-index="6" -->

</div>

<hr>

🏁 Grab a pen and map out the story, chart the data flows, and define the perimeters<!-- .element: class="fragment" data-fragment-index="7" -->

---

## DFD (Data Flow Diagrams)

- Threats often follow data => Data Flow Diagrams </br>[DFD on Wikipedia](https://en.wikipedia.org/wiki/Data-flow_diagram)
- DFD are simple, easy to learn and sketch
- Traditional whiteboards are fantastic tools 😀

<hr>

❗️We utilize data flow diagrams as they offer </br>a simple and clear illustration of how data,</br> and therefore potential threats, move within a system.

---

## DFD components

<img src="./content/images/dfd.png">

<hr>

<div style="font-size:0.6em">

[More on DFD's at Lucidchart](https://www.lucidchart.com/pages/data-flow-diagram) & [WikipediA](https://en.wikipedia.org/wiki/Data-flow_diagram)

</div>
---

## DFD - An Example

<img src="./content/images/dfd-example.png">

---

## Trust boundaries (1/2)

<div style="font-size:0.9em">

- A boundary that separates two systems, components, or entities with different levels of trust.<!-- .element: class="fragment" data-fragment-index="1" -->  
- Trust boundaries are often security decision points<!-- .element: class="fragment" data-fragment-index="2" -->
- They are conceptual boundaries that defines the extent to which one system can trust another system, and vice versa.<!-- .element: class="fragment" data-fragment-index="3" -->
- Trust boundaries is where entities/principals<!-- .element: class="fragment" data-fragment-index="4" --> <a style="color:red">with different privileges</a> interact. It's where the "responsibility for security" changes.<!-- .element: class="fragment" data-fragment-index="4" -->

---

## Trust boundaries (2/2)

<div style="font-size:0.9em">

- A<!-- .element: class="fragment" data-fragment-index="4" --> [principal](https://en.wikipedia.org/wiki/Principal_(commercial_law)<!-- .element: class="fragment" data-fragment-index="2" --> (a noun): Someone, something that is authorized to act as an agent/representative. It could be users, UID's, apps, service principals, devices, deployment instances, physical data centers .... <!-- .element: class="fragment" data-fragment-index="4" -->
- A principal is often the smallest unit you can name in a policy</br> (iam object in access policies, UID's on a desktop/server) <!-- .element: class="fragment" data-fragment-index="4" -->
- Trust boundaries needs info/agreements on the mechanism that isolates them, on how to enforce, configure and test them <!-- .element: class="fragment" data-fragment-index="5" -->
- Trust boundaries should be labeled <!-- .element: class="fragment" data-fragment-index="6" -->

<hr>

💡 Examples: Network perimeters (public, internals), authentication points, processes running with diff privilege levels, physical (on-prem, cloud), api gateways, corporate vs. personal devices, application tiers (webserver, database, ...) <!-- .element: class="fragment" data-fragment-index="7" -->


---

## What artifacts/models do we record/store?

<div><!-- .element: style="font-size:0.7em"-->

- Consider the lifecycle and upkeep of models and documentation<!-- .element: class="fragment" data-fragment-index="1" -->
- Archive certain documents for historical reference, and regularly update others<!-- .element: class="fragment" data-fragment-index="2" -->
- Organize storage— alongside code, in distinct repositories, or platforms like SharePoint<!-- .element: class="fragment" data-fragment-index="3" -->
- Investigate storage solutions, mindful of data sensitivity<!-- .element: class="fragment" data-fragment-index="4" -->
- Be aware that formalization can increase effort (legal obligations, GDPR, ++)<!-- .element: class="fragment" data-fragment-index="5" -->
  
<hr>

Examples:<!-- .element: class="fragment" data-fragment-index="6" -->

- Whiteboard => Pictures or Drawings (draw.io) stored with project<!-- .element: class="fragment" data-fragment-index="7" -->
- Collaborative tools like Miro could be ok<!-- .element: class="fragment" data-fragment-index="8" -->
  - Don't underestimate the learning curve and the "tool trap"!
  - Provide some Miro training before starting to TM
  - Remember information classification/sensitivity/GDPR!
- Other solutions like<!-- .element: class="fragment" data-fragment-index="9" --> [Irus Risk](https://www.iriusrisk.com/)<!-- .element: class="fragment" data-fragment-index="9" -->, [OWASP Threat Dragon](https://owasp.org/www-project-threat-dragon/)<!-- .element: class="fragment" data-fragment-index="9" -->, [Draw.io](https://draw.io)<!-- .element: class="fragment" data-fragment-index="9" -->

</div>

---

## Organizing groups and work

<div><!-- .element: style="font-size:0.9em"-->

- We form 4-5 groups
- The group will stay together for all exercises
- The exercises build on each other
- We draw on A3 sheets (boards, flip-overs or similar)
- We use thick-✏️ when drawing (it's easier to read) 
- We make notes on paper
- Groups take a picture of drawings and notes and share in Slack channel [#appsec-threatmodeling-workshop](https://equinor.slack.com/archives/C046T5B84P4) before presenting
  - We will delete most of these posts from the Slack channel after the workshop
- Make sure to take a short round of introduction in the groups 🤝

<hr>

🎪 Organize yourself now 🎪<!-- .element: class="fragment" data-fragment-index="1" -->

</div>

---

## Exercise 1 - Creating a model

---

## Our example system

<img src="./content/images/tm-example-system.png">

---

## EX-1: Drawing a data flow diagram

<div><!-- .element: style="font-size:0.6em;text-align:left"-->

<hr>

Tasks:

For our [example system](content/images/tm-example-system.png)

- Examine the system, use cases and components
- <a style="color:red">Draw a DFD for the system</a>
- <a style="color:red">Document any assumptions you make</a>
- Take a picture of your DFD, share on Slack </br>and prepare to present the model to the class

The person in the group which has the  <a style="color:magenta">next birthday</a> becomes group lead for this exercise.

<hr>

⏰ Time boxed schedule (20m):

- Discuss and clarify system
- Create one common DFD for group
- Prepare to present
- Take picture and share on Slack

<hr>

Remember: "All models are wrong. Some models are useful"

</div>

Note:

Inform on group leaders responsibilities, things such as;
- Being a servant to the group
- Provide sufficient stream of snack energy (when available)
- Time keeper
- Appoint notetaker
- Decide who presents on behalf of team
- Share snapshops on Slack

---

## EX1: Presenting models

Each group present their DFD along with assumptions

<hr>

❓Common Reflections, Observations, Learning
