# Jargon Buster

Plain-English explanations of the technical words in this project. The README does not use these words when it can. This file gives the precise words for readers who want them.

**A2A (Agent2Agent)**
An open protocol that agents use to send work to other agents. OAAF checks delegated authority when one agent gives work to another agent.

**Authority grant**
The main object in OAAF. A grant states that a subject can do some actions on some resources, with some limits, for a limited time. A grant is a claim. The enforcement point checks the grant. The enforcement point does not obey it without a check.

**AuthZEN**
An open standard for authorization requests and decisions. OAAF gives verified authority facts to an AuthZEN decision point. OAAF does not replace it.

**Consequential action**
An action with an effect that is difficult to undo. Examples: merge code, send an email, pay money, delete data.

**Credential**
An API key, an OAuth token, or a service account. A credential tells you what a process can access. It does not tell you what the agent has permission to do for one task.

**Delegated authority**
The permission that a person or an agent gives to an agent for a specific task. In OAAF, it is smaller than or equal to the authority of the giver.

**Enforcement point**
The part that sits immediately before a consequential action and checks the authority. Examples: MCP middleware, a tool gateway, an API gateway. If the agent can go around it, it is not an enforcement point.

**Evidence**
A record that connects the subject, the authority, the request, the decision, and the reason. OAAF records evidence for denials and for allows.

**Fail closed**
If OAAF cannot verify the authority, the answer is DENY. This applies to authority that is expired, revoked, unverifiable, or malformed.

**Issuer**
The person or system that can make grants. A verifier trusts an issuer through a configured trust relationship.

**MCP (Model Context Protocol)**
An open protocol that agents use to call tools. OAAF can check authority before an MCP tool call.

**Narrowing (attenuation)**
Each time that authority goes to a new agent, it can stay the same or get smaller. It can never get larger.

**PDP (policy decision point)**
Your own authorization system, for example OPA or Cedar. It decides if your policy permits an action. OAAF sits in front of it.

**Proof of possession**
Proof that the agent that shows a grant holds the private key that the grant is bound to. This stops a different agent from using a copied grant.

**Reason code**
A short name for why OAAF said DENY, for example `tool_not_delegated` or `expired`. Reason codes help a person fix the problem.

**Revocation**
To cancel a grant before its end time. The verifier checks the revocation state before each decision.

**Subject**
The identity that receives authority. It can be an AI agent, a workload, a service account, or a person.

**Verifier**
The logic inside an enforcement point. It uses the grant, the request, and the current state to make a decision.
