<!-- markdownlint-disable MD033 -->

# Threat Modeling the SDLC</br>∞

SDLC = Software/System Development Life Cycle<!-- .element: style="font-size:0.8em"-->

---

## Current Threat Modeling effort

- Most of our security work focuses on protecting our systems and developed apps.
- We spend less time on threat modeling our own software development processes.<!-- .element: class="fragment" data-fragment-index="2" -->
- Supply chain attacks are becoming a hot topic.<!-- .element: class="fragment" data-fragment-index="3" -->
- Our SDLC is exposed to various attack vectors.<!-- .element: class="fragment" data-fragment-index="4" -->
- Software developers often have a wide set of permissions and are "high value targets"<!-- .element: class="fragment" data-fragment-index="5" -->

---

## A traditional view of a SDLC

<img src="./content/images/tm-example-sdlc.png">

<hr>

"This looks easy enough"

---

## A more realistic view of a SDLC

<img src="./content/images/tm-example-sdlc-real.png" width="70%" height="auto" display="block" margin-left="auto" margin-right="auto">

<hr>

This example is by no means exhaustive, reality is often much more complex.</br><!-- .element: style="font-size:0.7em"--> *"All models are wrong. Some models are useful"*<!-- .element: style="font-size:0.7em"-->

---

## A DevSecOps reference architecture

<img src="./content/images/DevOps-reference-architecture.jpeg" width="70%" height="auto" display="block" margin-left="auto" margin-right="auto">

according to Sonatype.

<hr>

**What could possibly go wrong?**

---

## Threat Modeling our SDLC

<div style="font-size:0.75em">

- Identify and document security requirements.<!-- .element: class="fragment" data-fragment-index="1" -->
- Document SDLC (How we work, develop, do test, do security++)<!-- .element: class="fragment" data-fragment-index="2" -->
- Document runbook (How we operate)<!-- .element: class="fragment" data-fragment-index="3" -->
- Select threat model strategy<!-- .element: class="fragment" data-fragment-index="4" -->
  - Part(s)/component(s) of the SDLC<!-- .element: class="fragment" data-fragment-index="5" -->
  - Information flow - follow the code<!-- .element: class="fragment" data-fragment-index="6" -->
- Apply STRIPED (what could go wrong?)<!-- .element: class="fragment" data-fragment-index="7" -->
- Discuss & prioritise threats (what are we going to do about it?)<!-- .element: class="fragment" data-fragment-index="8" -->
- Implement (stories,issues etc.  on backlog)<!-- .element: class="fragment" data-fragment-index="9" -->
- Assess approach/results from SDLC threat modeling in team retrospective<!-- .element: class="fragment" data-fragment-index="10" -->

</div>

<hr>

❗️Avoid the "perfect" document/model syndrome. Start small, iterate. This goes for security requirements, the SDLC documentation, the runbook etc. Think life cycle - what documentation do we intend to maintain and keep up to date?<!-- .element: style="font-size:0.8em"--><!-- .element: class="fragment" data-fragment-index="11" -->

<hr>

❓ Common Reflections<!-- .element: class="fragment" data-fragment-index="11" -->

---

## Exercise 4 - Threat modeling a SDLC

---

## EX-4: Example SDLC

<img src="./content/images/tm-example-system-sdlc.png" width="65%" height="auto" display="block" margin-left="auto" margin-right="auto">

---

## EX-4: Doing an <u>end-to-end</u> Threat Model

<hr>

<div align="left"><!-- .element: style="font-size:0.60em"-->

In this exercise we will apply the skills we have acquired in the previous exercises to a fictive SDLC for the example system we presented in exercise 1.

Group tasks:

- Examine the SDLC and the associated assumptions
- Select a <u>flow/part</u> of the example SDLC 👇
- Create a DFD diagram
- Identify threats using STRIPED or brainstorming, suggest severity
- Document assumptions and issues
- For threats, select strategy, identify mitigations, suggest priority
- Take a picture of your DFD and documents, share on Slack </br>and prepare to present the model to the class

The person in the group which  <a style="color:magenta">last joined an Software Development Conference</a> becomes group lead for this exercise.

<hr>

⏰ Time boxed schedule (40m):

- Do an end-to-end threat model of the SDLC

</div>

---

## EX-4: Presentations

Each group present their results

<hr>

❓Common Reflections, Observations, Learning
