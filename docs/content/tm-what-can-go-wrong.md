<!-- markdownlint-disable MD033 -->

# What can go wrong? </br>💥

---

## Introducing [STRIDE](https://en.wikipedia.org/wiki/STRIDE_(security))/[STRIPED](https://www.youtube.com/watch?v=uzOdpuAhr28)

STRIDE is a model for identifying computer security threats. </br>STRIPED is an extension adding "Privacy" to the model with the following mnemonic: <!-- .element: style="font-size:0.65em"-->

 <table style="font-size:0.45em"">
  <tr>
    <th>Threat</th>
    <th>Security property violated</th>
    <th>Definition</th>
    <th>Example</th>
  </tr>
  <tr>
    <td>Spoofing</td>
    <td>Authentication</td>
    <td>Impersonating someone or something</td>
    <td>Spoof email, spoof ip address, spoof a web site, spoof user, spoof a Python module, spoof a npm package</td>
  </tr>
  <tr>
    <td>Tampering</td>
    <td>Integrity</td>
    <td>Modify data and code</td>
    <td>Modifying a file, changing code in a NPM repo, change a packet as it traverses the network, change a binary, tamper with a physical device, change a log entry</td>
  </tr>
  <tr>
    <td>Repudiation</td>
    <td>Non-repudiation </br>Accountability</td>
    <td>Claiming to not have performed an action</td>
    <td>"I did not send that email", "I did not make that change", "I have not used that system", "I did not agree to this contract", "I did not post this"</td>
  </tr>
  <tr>
    <td>Information disclosure</td>
    <td>Confidentiality</td>
    <td>Exposing information to someone not authorised to see it</td>
    <td>Publish a list of customers to a web site, allowing someone to read source code, eavesdrop network traffic, stolen/lost unencrypted mobile device, insecure cloud storage, storing a secret in your code</td>
  </tr>
  <tr>
    <td>Privacy</br></td>
    <td>Privacy</td>
    <td>Unauthorized collection, use, disclosure, or storage of personal data.</td>
    <td>We have no ide about which PII we have, we collect more PII than we need, we process PII in a cloud service - with no processor agreement, PII is stored indefinitely for no apparent reason, we share no information on what PII we collect, tracking cookies, spyware, public cameras recording, location tracking</td>
  </tr>  
  <tr>
    <td>Elevation of privilege</br>(Expansion of Authority)</td>
    <td>Authorization</td>
    <td>Gain capabilities without proper authorization</td>
    <td>Allowing a remote internet user to run commands, XSS, SQL Injection, RCE, going from limited to admin user, using default passwords, social engineering, phishing attacks, misconfiguration, zero-day's</td>
  </tr>  
  <tr>
    <td>Denial of service</td>
    <td>Availability</td>
    <td>Deny or degrade service to users</td>
    <td>Network flood attacks - consume all resources, eat all memory for a program, route packages to void, DDos </td>
  </tr>
</table>

---

## How to use STRIPED?

<div style="display: grid;grid-column-gap: 1%; grid-auto-columns: 70% 30%;">

<div  style="grid-area: 1 / 1"><!-- .element: style="font-size:0.7em"-->
<hr>

- We use S-T-R-I-P-E-D mnemonic to identify threats to system<!-- .element: class="fragment" data-fragment-index="1" -->
- Approaches to apply:<!-- .element: class="fragment" data-fragment-index="2" -->
  - Trace a user story across the diagram, check for S-T-R-I-P-E-D threats on the way, and refine continuously.<!-- .element: class="fragment" data-fragment-index="3" -->
    - for threat in S-T-R-I-P-E-D <!-- .element: class="fragment" data-fragment-index="4" -->
      - for element in diagram
        - detail the threat interaction.
  - Concentrate on a specific element or part of the system and assess it against S-T-R-I-P-E-D threats.<!-- .element: class="fragment" data-fragment-index="5" -->
    - for element in diagram<!-- .element: class="fragment" data-fragment-index="6" -->
      - for threat in S-T-R-I-P-E-D
        - detail the threat interaction.
- Keep improving as you go<!-- .element: class="fragment" data-fragment-index="8" -->
  
</div>

<div  style="grid-area: 1 / 2"><img src="./content/images/dfd-example.png" width="100%" height="auto" display="block" margin-left="auto" margin-right="auto"><!-- .element: class="fragment" data-fragment-index="1" -->
</div>

</div>

<hr>

❗️Plenty of frameworks like STRIDE/STRIPED are out there, but we lean into STRIPED when we're getting teams up to speed on Threat Modeling.<!-- .element: style="font-size:0.5em"--><!-- .element: class="fragment" data-fragment-index="10" -->
Some alternatives: [MITRE ATT&CK](https://attack.mitre.org/), [Attack Tree](https://en.wikipedia.org/wiki/Attack_tree), [PASTA](https://versprite.com/tag/pasta-threat-modeling/), [DREAD](https://en.wikipedia.org/wiki/DREAD_%28risk_assessment_model%29), [LINDDUN](https://www.linddun.org/), [LINDDUNgo](https://www.linddun.org/go), STRIKE .... <!-- .element: style="font-size:0.5em"-->

---

## STRIPED per element

<table><!-- .element: style="font-size:0.8em"-->
    <tr>
        <th>Part</th>
        <th>Spoof</th>
        <th>Tamper</th>
        <th>Repudiation</th>
        <th>Info disclosure</th>
        <th>Privacy</th>
        <th>EoP</th>
        <th>Deny Service</th>
     </tr>
    <tr>
        <td>External entity</td>
        <td align="center">X</td>
        <td align="center"></td>
        <td align="center">X</td>
        <td align="center"></td>
        <td align="center">?</td>
        <td align="center"></td>
        <td align="center"></td>
    </tr>
    <tr>
        <td>Process</td>
        <td align="center">X</td>
        <td align="center">X</td>
        <td align="center">X</td>
        <td align="center">X</td>
        <td align="center">X</td>
        <td align="center">X</td>
        <td align="center">X</td>
    </tr>
    <tr>
        <td>Data store</td>
        <td align="center"></td>
        <td align="center">X</td>
        <td align="center">?</td>
        <td align="center">X</td>
        <td align="center">X</td>
        <td align="center"></td>
        <td align="center">X</td>
    </tr>
    <tr>
        <td>Dataflow</td>
        <td align="center"></td>
        <td align="center">X</td>
        <td align="center"></td>
        <td align="center">X</td>
        <td align="center">X</td>
        <td align="center"></td>
        <td align="center">X</td>
    </tr>

</table>

<hr>

🕵🏻‍♂️ The [Elevation of Privileges game](https://github.com/adamshostack/eop) (EoP) is helpful and fun. The EoP game with the privacy suited added is available.

---

## Tracking threats and assumptions

- Track issues as they are found<!-- .element: class="fragment" data-fragment-index="1" -->
- Track assumptions as they are discoverd<!-- .element: class="fragment" data-fragment-index="2" -->
- Issues and assumptions are input to the next phase - <!-- .element: class="fragment" data-fragment-index="3" --> </br>"What are we going to do about it?"<!-- .element: class="fragment" data-fragment-index="3" -->
- Recommended practice:<!-- .element: class="fragment" data-fragment-index="4" -->
  - <!-- .element: class="fragment" data-fragment-index="5" --><a style="color:red">Appoint a note taker</a><!-- .element: class="fragment" data-fragment-index="5" -->
  - Record meetings / sessions<!-- .element: class="fragment" data-fragment-index="6" -->
  - Create a team strategy for how to </br>document, what to document, where to store ++. </br>Experiment and iterate<!-- .element: class="fragment" data-fragment-index="7" -->

<hr>

❗️The best tools are the one that works for the people involved!<!-- .element: class="fragment" data-fragment-index="8" -->

---

## What could go wrong - brainstorming

(As an alternative to using STRIDE/STRIPED)<!-- .element: style="font-size:0.6em"-->

<div style="font-size:0.9em">

Some useful questions/statements:

- What's the top concern with our system's security? <!-- .element: class="fragment" data-fragment-index="1" -->
- If you were to break into our system, how would you do it? <!-- .element: class="fragment" data-fragment-index="2" -->
- You know that technical or security issue we've been putting off? <!-- .element: class="fragment" data-fragment-index="4" -->
- We rigged up a quick fix last time, didn’t we? <!-- .element: class="fragment" data-fragment-index="5" -->
- So, I was going through the ASVS checklist,</br> how are we doing on that front? <!-- .element: class="fragment" data-fragment-index="6" -->
- Been brushing up on<!-- .element: class="fragment" data-fragment-index="7" --> [GDPR](https://gdpr-info.eu/art-5-gdpr/) — are we in the clear? <!-- .element: class="fragment" data-fragment-index="7" -->

</div>

<hr>

❗️There are many guides and books available discussing the mechanics of threats. There are threats libraries available. It's usually a good idea to augment our threat modeling with these aids〝after〞we have reached a bit of maturity<!-- .element: class="fragment" data-fragment-index="8" style="font-size:0.8em" -->

---

## Exercise 2 - Identifying threats

---

## EX-2: Applying STRIPED

<hr>

<div align="left"><!-- .element: style="font-size:0.7em"-->

Tasks:

For our example system, using your DFD for whats currently implemented:

- Examine the system, use cases, components and requirements
- Apply STRIPED, document issues, assumptions and threats
- <a style="color:red">Team decide scope</a>, iterating as you are learning is smart!
- Document format suggested (👇)
- Take a picture of your documents, share on Slack </br>and prepare to present the model to the class

The person in the group which  <a style="color:magenta">last bought a car</a> becomes group lead for this exercise.

<hr>

⏰ Time boxed schedule (30m):

- Apply STRIPED and document threats

<hr>

💡 Try to avoid 🐰 holes. Stop early. Iterate

</div>

---

## EX-2: Document <u>example</u>

<table style="font-size:0.50em" >
    <tr>
        <th>Threat ID</th>
        <th>Part</th>
        <th>STRIPED</th>
        <th>Threat action</th>
        <th>Impact</th>
    </tr>
    <tr>
        <td>1</td>
        <td>Web app</td>
        <td>Spoof</td>
        <td>Attacker steals session cookie</td>
        <td>Information disclosure, access to all emails</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Token Cache</td>
        <td>Information disclosure</td>
        <td>Attacker is stealing O365 access tokens</td>
        <td>Information disclosure, system integrity, GDPR ...</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Wep app</td>
        <td>Privacy</td>
        <td>Purpose, Minimization: We may not need, but we collect users home county and street address</td>
        <td>Privacy violation, fines, bad press</td>
    </tr>
    <tr>
        <td>4</td>
        <td>Backend</td>
        <td>Privacy</td>
        <td>Lawfulness,purpose,anonymisation++; We collect username, DOB, sex and allergies and store for 10 years to have proper statistics</td>
        <td>Privacy violation, fines, bad press</td>
    </tr>
    <tr>
        <td align="left">5</td>
        <td>..</td>
        <td>..</td>
        <td align="center">..</td>
        <td align="center">..</td>
    </tr>
</table>

<div align="left"><!-- .element: style="font-size:0.6em"-->

Assumptions:

- There are no key-stores used
- Storage - VM discs are not encrypted

Issues:

- Should internal traffic be https as well?
- What about PKI infrastructure for http certs?
  
</div>

---

## EX-2: Presenting threats

Each group present identified

- Threats
- Assumptions
- Issues

Which STRIPED strategy did you use?</br>Did you use the Security Requirements?

<hr>

❓Common Reflections, Observations, Learning