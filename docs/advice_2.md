# Project Advice: Rangr Compass CRM

This document contains the strategic advice for the Rangr Data work sample project. While `plan.md` covers the *what* and *when*, this file covers the *why* and *how*. Review this file periodically to ensure you are focused on the things that will make the biggest impact.

---

## 1. The Core Mindset: Think Like a Consultant

Your primary goal is to demonstrate that you can solve a business problem with a new tool. The technology is the medium, but the problem-solving is the skill being tested.

* **Embrace Your Persona:** "Alex the Sales Rep" is your most important stakeholder. Before you build any feature, ask: "Does this help Alex do his job better?" This simple question will guide every decision you make.
* **Tell a Story:** People connect with stories, not features. Your presentation should be a narrative.
    * **Don't say:** "Here is a table of people linked to a company."
    * **Do say:** "To help Alex quickly see all his contacts for a specific account, I created this detailed view. Now, with one click, he can see everyone he needs to talk to."
* **Your Project Name Has a Purpose:** "Rangr Compass CRM" isn't just a name. It's part of the story. It was chosen because it provides *direction* for a sales rep—a core business value.

## 2. Execution Strategy: How to Win the Build Phase

* **Prioritize Ruthlessly:** Use the "Scope Sweet Spot" defined in your plan. The single biggest technical risk is over-engineering. A fully working MVP with two features is infinitely better than a half-finished "everything machine." Ugly but working > beautiful but broken.
* **Work in Parallel:** The data pipeline and the Ontology are two halves of the same whole. Develop them simultaneously. Bouncing between Pipeline Builder and the Ontology Manager is not a sign of disorganization; it is the correct, iterative workflow.
* **Focus on Function, Not Flash:** The prompt explicitly values **robust functionality (Actions, Links)** over visualization. A simple, powerful "Log Interaction" Action is worth more than ten complex but meaningless charts.

## 3. The Presentation: How to Stand Out

The 5-minute presentation is your chance to frame your work and demonstrate your communication skills.

* **Master the Flow:** Structure your demo logically. The suggested flow is highly effective:
    1.  **(30 sec) The Problem:** "I built a CRM for Alex, who needs to..."
    2.  **(2 min) The Technical Solution:** Briefly show the end-to-end data flow: Pipeline → Ontology → Workshop. This shows you understand the whole system.
    3.  **(2 min) The User's Reality:** Demo the UI from Alex's perspective. Show how the features solve his problems.
    4.  **(30 sec) The Value:** "The power of this is that Alex can now..."
* **Speak the Foundry Language:** Confidently use the platform's terminology. Saying "I configured an Action in the Ontology that writes back to the dataset" sounds much more professional than "I made a button that saves the data." It proves you've learned their ecosystem.

## 4. The Live Edit: The Make-or-Break Moment

**This is the most important part of the evaluation.** Many candidates can build a simple app by following tutorials. Very few can adapt and modify it under pressure. This is where you differentiate yourself.

* **It's a Test of Your Process, Not Just Your Speed:** They want to see how you think. Are you calm? Do you approach the problem logically? Do you communicate effectively?
* **Narrate Everything You Do:** When they give you a request, repeat it back to confirm you understand. Then, talk through your plan *before* you start clicking.
    > "Okay, you want to add a 'Status' property. To do that, I'll first go to the Ontology Manager, find the Person object, and add the new property. Then, I'll have to expose it in the Workshop application so it appears in the table."
* **Stay Calm if You Get Stuck:** It's okay to not know something instantly. Your response is what matters.
    > "Hmm, that's an interesting request. My first instinct is to look at the widget's styling properties in Workshop. Let me try that..."
* **Practice is Everything:** Do not go into the presentation without having completed the practice scenarios in `plan.md` multiple times. The muscle memory and confidence you build here will be invaluable.

## 5. Final Touches: The 10% That Makes 90% of the Impression

* **Have "Next Steps" in Your Back Pocket:** When they ask, "What would you do next?" be ready with a thoughtful answer (e.g., "I'd build out an 'Opportunity' object to track the sales pipeline, which would provide even more value to Alex and his manager."). This shows vision.
* **A Polished README is Your Digital Handshake:** A clean, well-structured `README.md` shows professionalism and pride in your work. It's the first thing they might see. Make it count.

You have a solid plan and a winning strategy. Stay focused on these principles, and you'll be in a great position to succeed.
