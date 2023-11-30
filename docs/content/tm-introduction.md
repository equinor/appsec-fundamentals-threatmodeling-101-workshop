<!-- markdownlint-disable MD033 -->

# Threat Modeling Fundamentals</br>🖖

---

## What is threat modeling?

From the [Threat Modeling Manifesto](https://www.threatmodelingmanifesto.org/):<!-- .element: style="font-size:0.8em"-->
> Threat modeling is analyzing representations of a system to highlight concerns about security and privacy characteristics.

---

## Privacy vs Security

### Privacy

Privacy refers to any rights you have to control your personal information and how it is used. Privacy requires security.

### Security

Security refers to how information is protected. Security defends privacy.

---

## Why Threat modeling (1/2)?

<div style="font-size:0.9em">

- Develop more secure systems (what we develop)<!-- .element: class="fragment" data-fragment-index="1" -->
- Develop more securely (how we develop)<!-- .element: class="fragment" data-fragment-index="2" -->
- Operate more securely (how we operate)<!-- .element: class="fragment" data-fragment-index="3" -->
- Identify potential vulnerabilities within our systems.<!-- .element: class="fragment" data-fragment-index="4" -->
- Detect design and implementation issues<!-- .element: class="fragment" data-fragment-index="5" -->

</div>

---

## Why Threat modeling (2/2)?

<div style="font-size:0.9em">

- Cost reduction by fixing issues before they occur<!-- .element: class="fragment" data-fragment-index="6" -->
- Enable informed decisions on threats and mitigations<!-- .element: class="fragment" data-fragment-index="7" -->
- Provide evidence that security and privacy are integrated into our designs.<!-- .element: class="fragment" data-fragment-index="8" -->
- Cultivate a collective understanding of the system among team members.<!-- .element: class="fragment" data-fragment-index="9" -->
- Raise awareness and educate about security and privacy importance.<!-- .element: class="fragment" data-fragment-index="10" -->
- Implement a systematic and uniform approach to security and privacy concerns.<!-- .element: class="fragment" data-fragment-index="11" -->

</div>

<hr>

❗️Threat modeling will guide our designs </br>and help us make decisions with our eyes open.<!-- .element: class="fragment" data-fragment-index="11" -->

---

## The 4 Key Questions of Threat modeling

- What are we working on?<!-- .element: class="fragment" data-fragment-index="1" -->
- What can go wrong?<!-- .element: class="fragment" data-fragment-index="2" -->
- What are we going to do about it?<!-- .element: class="fragment" data-fragment-index="3" -->
- Did we do a good job?<!-- .element: class="fragment" data-fragment-index="4" -->

<hr>

🕵🏻‍♂️ <!-- .element: class="fragment" data-fragment-index="5" -->[The Threat modeling Manifesto](https://www.threatmodelingmanifesto.org/) 🔗</br>Review Values, Principles and Patterns<!-- .element: class="fragment" data-fragment-index="5" -->

---

## On models

> "All models are wrong, some models are useful"</br> - [George E.P. Box, 1979](https://en.wikipedia.org/wiki/All_models_are_wrong).

Box was emphasizing the point that while (statistical) models can never perfectly represent reality, they can still provide valuable insights and have practical applications.

---

## It starts with security & privacy requirements

<div><!-- .element: style="font-size:0.75em"-->

- All systems must have documented security requirements (SR)<!-- .element: class="fragment" data-fragment-index="1" -->
- All systems must have documented privacy requirements (PR)<!-- .element: class="fragment" data-fragment-index="1" -->
- SR/PR will guide and inform the security work we do - including threat modeling<!-- .element: class="fragment" data-fragment-index="2" -->
- In all/most organisations the governance</br> will be a good starting point for identifying SR<!-- .element: class="fragment" data-fragment-index="3" -->
- Legal and governmental requirements will also provide SR/PR<!-- .element: class="fragment" data-fragment-index="3" -->
- Threat modeling will often trigger update of SR/PR requirements<!-- .element: class="fragment" data-fragment-index="4" -->
- External sources for SR/PR "inspiration"<!-- .element: class="fragment" data-fragment-index="5" -->
  - [OWASP ASVS](https://owasp.org/www-project-application-security-verification-standard/), [OpenSSF Scorecard](https://securityscorecards.dev/), [GDPR](https://gdpr-info.eu/)

</div>

<hr>

❓ What are typical security/privacy requirements in<!-- .element: class="fragment" data-fragment-index="7" --> <u>your context</u> ?<!-- .element: class="fragment" data-fragment-index="7" -->

---

## When to threat model?

<div style="display: grid;grid-column-gap: 1%; grid-auto-columns: 50% 50%;">

<div  style="grid-area: 1 / 1"><!-- .element: style="font-size:0.8em"-->

<hr>

- Typically, we begin threat modeling for a system during the early stages of the SDLC (Software Development Life Cycle) in DevOps.
- It's important that threat modeling encompasses both the system itself and the entire SDLC process.
- Consistency is key with threat modeling—it should be an ongoing effort, not just a single event.

</div>

<div  style="grid-area: 1 / 2"><img src="./content/images/devops.png" width="100%" height="auto" display="block" margin-left="auto" margin-right="auto">
</div>

</div>

<hr>

<div><!-- .element: style="font-size:0.75em"-->

When to threat model? Like using a compass during a hike, frequent threat modeling helps you stay on the right path towards your security goals.

</div>

---

## Some basic terminology

- **Weakness**: A system flaw that can be a security risk</br>([CWE, Common Weakness Enumeration](https://cwe.mitre.org/), weakness types)
- **Exploitability**: How easily a weakness can be abused
- **Vulnerability**: A weakness that can be exploited</br>([CVE, Common Vulnerability Enumeration](https://cve.mitre.org/)) 
- **Severity**: The potential damage a vulnerability could cause </br>([CVSS, Common Vulnerability Scoring System](https://www.first.org/cvss/))
- **Threat**: The potential dangers or circumstance that can exploit vulnerabilities.
- **Risk**: The likelihood of a threat occurring and the impact it would have.

---

## Myths

- "I have never done threat modeling!"</br> => You're actually doing it more often than you think!!<!-- .element: class="fragment" data-fragment-index="1" -->
- "Threat modeling is a breeze"</br> => Not quite; it takes regular, systematic work to get it right.!<!-- .element: class="fragment" data-fragment-index="2" -->
- "Threat modeling is for security people - hero threat modeler"</br> => Nope, it's a team sport; everyone's got a role to play.!<!-- .element: class="fragment" data-fragment-index="3" -->

<hr>

❓ Discuss examples of every-day threat modeling (crossing the road, read and review ratings, check web site's legitimacy)<!-- .element: class="fragment" data-fragment-index="3" -->

---

## Keep Threat Modeling Real and Practical

- "Overthinking the threat modeling methodology?"</br>=> Dive in! Value team skills and "Just do it!".<!-- .element: class="fragment" data-fragment-index="1" -->
- "Getting caught up in the weeds?"</br>=> Keep your eyes on the prize. Don't get too fixated on the nitty-gritty details.<!-- .element: class="fragment" data-fragment-index="2" -->
- "Hunting for the flawless model?"</br>=> Forget perfection; it's a myth. Aim for various mini-models that give you different perspectives.<!-- .element: class="fragment" data-fragment-index="3" -->

<hr>

❗️Threat modeling can be the most effective way to drive security through a product, service or system.<!-- .element: class="fragment" data-fragment-index="4" -->
