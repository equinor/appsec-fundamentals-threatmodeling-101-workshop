<!-- markdownlint-disable MD033 -->

# What are we going to do about it? </br>🩺

Tactics, Strategies, Alignment, Prioritisation, Documentation<!-- .element: style="font-size:0.7em"-->

---

## Addressing threats

<div style="font-size:0.9em">

- Address each threat - decide on strategy/tactics, document<!-- .element: class="fragment" data-fragment-index="1" -->
- Strategies for identified threats are: mitigate, eliminate, accept or transfer<!-- .element: class="fragment" data-fragment-index="3" -->
  - <!-- .element: class="fragment" data-fragment-index="4" --><a style="color:red">Mitigate</a>, tactic: add controls, policies and procedures<!-- .element: class="fragment" data-fragment-index="4" -->
  - <!-- .element: class="fragment" data-fragment-index="5" --> <a style="color:red">Eliminate</a>, tactic: remove -> example: remove code, component...<!-- .element: class="fragment" data-fragment-index="5" -->
  - <!-- .element: class="fragment" data-fragment-index="6" --> <a style="color:red">Accept</a>, tactic: acknowledge, document acceptance<!-- .element: class="fragment" data-fragment-index="6" -->
  - <!-- .element: class="fragment" data-fragment-index="7" --> <a style="color:red">Transfer</a>, tactic: Insure, share (with customer?), document, track<!-- .element: class="fragment" data-fragment-index="7" -->
- Indicate severity to help prioritizations<!-- .element: class="fragment" data-fragment-index="8" -->
- Check/verify assumptions/issues<!-- .element: class="fragment" data-fragment-index="9" -->

</div>

---

## Mitigation

<div style="font-size:0.8em">

- To mitigate means to add controls, policies or procedures that address the threat<!-- .element: class="fragment" data-fragment-index="1" -->
- Controls are features or technologies<!-- .element: class="fragment" data-fragment-index="2" -->
  - Use technology before people or process!<!-- .element: class="fragment" data-fragment-index="2" -->
  - <!-- .element: class="fragment" data-fragment-index="3" --><a style="color:red">Protect, detect</a> or <a style="color:red"> respond</a> to threats<!-- .element: class="fragment" data-fragment-index="3" -->
- Mitigation tactics could be<!-- .element: class="fragment" data-fragment-index="4" -->
  - Code by developers, Code reviews, Input validation, Add encryption<!-- .element: class="fragment" data-fragment-index="9" -->
  - Provide security training, Implement disaster recovery and backup<!-- .element: class="fragment" data-fragment-index="11" -->
  - Products / services (like fw, waf, proxy, Snyk, ...)<!-- .element: class="fragment" data-fragment-index="12" -->
  - Strong or weak
  (auth only vs. security in depth) <!-- .element: class="fragment" data-fragment-index="13" -->
  (auth w/mfa vs auth without mfa)<!-- .element: class="fragment" data-fragment-index="13" -->
  - Anonymization of PII data for statistics<!-- .element: class="fragment" data-fragment-index="14" -->
- The right tactics will always be situational/context dependent<!-- .element: class="fragment" data-fragment-index="15" -->
- Explore standard as the first choice<!-- .element: class="fragment" data-fragment-index="17" -->
  - 💡<!-- .element: class="fragment" data-fragment-index="17" --> [OWASP Proactive Controls](https://owasp.org/www-project-proactive-controls/)<!-- .element: class="fragment" data-fragment-index="17" -->

</div>
---

## Managing</br> "What are we going to do about it"

<div style="font-size:0.8em">

- <!-- .element: class="fragment" data-fragment-index="2" --><a style="color:red">Document</a><!-- .element: class="fragment" data-fragment-index="2" -->
  - Write down and track threats (use teams tool chain)
  - Indicate severity (using risk ranking?)
  - Track as bugs, features, security stories, security debt
- <!-- .element: class="fragment" data-fragment-index="3" --><a style="color:red">Prioritize</a><!-- .element: class="fragment" data-fragment-index="3" -->
  - Align with your team context and reality
  - Business (PO) should be involved
  - Use agreed severity categories
- <!-- .element: class="fragment" data-fragment-index="4" --><a style="color:red">Implement</a><!-- .element: class="fragment" data-fragment-index="4" -->
  - Add to product/iteration backlog
  - Assessing implementation will be a lot easier if</br> a larger part of team participate in threat modeling

</div>

---

An introduction to
### Risk Ranking

<div style="font-size:0.6em">

> Likelihood * Impact = Risk Rating

(Skills on Risk Ranking will become very handy when your threat model practices mature,</br> it may be a bit much in the beginning of your journey)
</div>
---

## OWASP _Simplified_ Risk Rating

<div style="font-size:0.6em">

The [methodology](https://owasp.org/www-project-top-ten/2017/Note_About_Risks.html) takes the average of three likelihood factors which is multiplied with a technical impact factor. </br>  Scores from 1 (best case) to 3 (wost case)

<hr>

rr = ((exploitability + commonality + detectability) / 3) * impact

<hr>

</div>

<div style="font-size:0.6em">

- **exploitability**
  - ease of exploit of the *attack vector*
  - _How hard is it to exploit this?_
  - (1 - difficult, 3 = easy)
- **commonality** of the weakness
  - _Is this a common weakness?_
  - (1 = uncommon, 3 widespread)
- **detectability** of the weakness from the attacker's point of view
  - _How easy is it for the attacker to discover that this vulnerability exists?_
  - (1 = difficult, 3 easy)
- **technical impact**  
  - The technical impact in the system
  - Impact on <a style="color:red">C</a>onfidentiality, <a style="color:red">I</a>ntegrity, <a style="color:red">A</a>vailability
  - (1 = minor, 3 = severe)

</div>

Note:

- The risk rating used for 2017 OWASP Top 10
- Useful to have _some_ reasoning behind the severity
- Not an exact science, the "correct" values do not exist
- Base this of what you know today, tune in on security related news, get your hands dirty with security testing, lean on lists like OWASP Top 10, mitre attack

---

<img src="./content/images/owasp-simplified-rr.png">

---

## Example risk ranking

<img src="./content/images/tm-diagrams-risk-ranking-doc-ex.png">

Note:

- https://owasp.org/www-project-top-ten/2017/Note_About_Risks.html
- Calculated Risk Ranking by multiplying the average of likelihood with the impact

---

## Exercise 3 - Managing Threats

---

## EX-3: Threat management

<div align="left" style="font-size:0.8em">

<hr>

Tasks:

For **some** of the threats identified in the previous exercise:

- Select strategies (at least a few should be "mitigation")
- Discuss realistic fix'es and document them (controls)
- Suggest severity category
  - (Optionally) use OWASP Simplified Risk Rating
- Document format suggested (👇)
- Take a picture of your documents, share on Slack </br>and prepare to present the model to the class

The person in the group which  <a style="color:magenta">last went to the movies</a> becomes group lead for this exercise.

<hr>

⏰ Time boxed schedule (20m):

</div>

---

## EX-3: Document <u>example</u>

<div align="left" style="font-size:0.65em">

<table style="font-size:0.7em">
    <tr>
        <th>TID</th>
        <th>AID</th>
        <th>Threat #</th>
        <th>Threat summary</th>
        <th>Strategy</th>
        <th>Fix idea</th>
        <th>Pros/Cons</th>
        <th>Severity</th>
    </tr>
    <tr>
        <td>1</td>
        <td>1</td>
        <td>Stolen session cookie from front end</td>
        <td>An attacker is able to steal the session cookie of a valid user session</td>
        <th>Mitigate</th>
        <td>Assess terminating session if sudden change in access ip. Assess using browser fingerprinting</td>
        <td>Pro: Could fix the problem</br>Con:May introduce errors if user is access from multiple clients</td>
        <td>Critical</td>
    </tr>
    <tr>
        <td>2</td>
        <td>2</td>
        <td>Token cache exposure</td>
        <td>An attacker is able to access token cache on the back-end and thus access service impersonation a user/service</td>
        <th>Mitigate</th>
        <td>Move token cache to external service, encrypt, add logging of all access, lock down permissions</td>
        <td>Pro: Would reduce the risk</br>Con: Adds complexity, cost and skills need in team</td>
        <td>Moderate</d>
    </tr>
    <tr>
        <td>3</td>
        <td>3</td>
        <td>We collect users home county and street address</td>
        <td>We collect PII that we do not need</td>
        <th>Eliminate</th>
        <td>Remove data collection</td>
        <td>Pro: Easy fix, Reduce privacy risk</br>Con: Take some work to refactor app</td>
        <td>High</d>
    </tr>
    <tr>
        <td>3</td>
        <td>4</td>
        <td align="center">..</td>
        <td align="center">..</td>
        <td align="center">Transfer</td>
        <td align="center">..</td>
        <td align="center">..</td>
        <td align="center">..</td>
    </tr>
    <tr>
        <td>-</td>
        <td>5</td>
        <td align="center">..</td>
        <td align="center">..</td>
        <td align="center">..</td>
        <td align="center">..</td>
        <td align="center">..</td>
        <td align="center">..</td>
    </tr>
</table>

</div>

<hr>

<div style="text-align:left; font-size:0.5em">

- TID, Threat Id, referring to the list of threats (from ex-2)
- AID, Threat Action Id
- Suggested severity categories: Critical, Important, Moderate, Low

</div>

---

## EX-3: Presentations

Each group present:

- Threats
  - Strategies
  - Fix ideas
  - Pros/Cons
  - Severity
- How were the Security Requirements used?

<hr>

❓Common Reflections, Observations, Learning

---

## Prioritizing threats (1/2)

<a style="color:red">Include</a> the Product Owner (PO) in your threat modeling!

<div style="text-align:left; font-size:0.9em">

- The PO is part of the team
- Include in all or selected TM sessions?
  
<hr>

- Prioritizations will always include context and system considerations</br> - your reality<!-- .element: class="fragment" data-fragment-index="0" -->
  - Find guidance in the security requirements
- Agree on prioritization levels up-front,</br> and re-visit in retrospectives as you learn<!-- .element: class="fragment" data-fragment-index="1" -->
  - Severity, as a measure of potential harm or damage if exploited
  - Risk, as in probability * impact (CIA, cost, reputation, ++)
  - Simplified Risk Ranking may be a good option for severity

</div>

---

## Prioritizing threats (2/2)

<div style="text-align:left; font-size:0.9em">

- Find inspiration in the Microsoft Bug Bar for prioritisation guidelines</br>(<!-- .element: class="fragment" data-fragment-index="2" -->
[SDLC](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/cc307404(v=msdn.10)?redirectedfrom=MSDN),<!-- .element: class="fragment" data-fragment-index="2" -->
[Privacy](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/cc307403(v=msdn.10)?redirectedfrom=MSDN))<!-- .element: class="fragment" data-fragment-index="2" -->
- Some threats MUST involve the business/product owner in prioritising<!-- .element: class="fragment" data-fragment-index="3" -->
- Some threats should be prioritized by the team (a team decision)<!-- .element: class="fragment" data-fragment-index="4" -->
- Agree with PO to spend a certain amount on security work in each iteration (20%)?<!-- .element: class="fragment" data-fragment-index="6" -->

<hr>

- Important to know "who owns the risk and can accept it on behalf of the business?"<!-- .element: class="fragment" data-fragment-index="7" -->

❓ Common Reflections<!-- .element: class="fragment" data-fragment-index="7" -->

</div>