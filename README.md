Abby - Career Coach & Certifications Assistant for PeopleCert

(Read this in Raw mode)
📌 Overview

Abby is an AI Agent designed to assist users in exploring and pursuing certifications offered by PeopleCert. 
Built as a Proof of Concept (PoC) during the 2025 Hackathon, Abby demonstrates how a digital persona can transform
the customer experience by offering dynamic, personalized guidance throughout a certification journey.

🛠️ Built with Copilot Studio (Classic Orchestration Mode)

Abby is developed using Microsoft Copilot Studio, utilizing the classic orchestration mode (not the generative orchestration preview), 
which ensures greater customization, predictability, and control over the conversational flow. 
This decision reflects our intent to move towards a production-grade AI solution that can be reliably extended,  
tested, and deployed to external users after further development and UAT phases.

🧠 Key Architecture & Functionality
AI Engine: Every customer message triggers an AI prompt powered by GPT-4o-mini, 
allowing Abby to process user input, extract relevant context, and generate highly contextual responses.

Flows & Logic: 
The bot uses three Power Automate flows to support its operations, including:
--- Storing and managing data (e.g., contact info, preferences)
--- Sending personalized emails
--- Interfacing with backend services (like Dataverse & Dynamics 365)

Variable Framework:
Abby uses over 70 global variables to capture and maintain contextual information throughout the conversation.
These variables include user profile data (e.g., age, company, experience), preferences, and selected certifications.
Variables are both used in real-time (to power the generative Answers nodes) and stored externally for downstream actions.

🧩 Personalized Experience Engine
Abby goes beyond simple FAQ-style interactions. When a user provides consent, Abby:
--- Begins collecting personal and professional context.
--- Dynamically compares the user’s profile to a set of pre-modeled personas.
--- Offers tailored certificate suggestions using generative AI instructions.
--- Generates unique call-to-action buttons, relevant resources, and discount codes.
--- Automatically triggers backend actions like:

-Sending personalized follow-up emails
-Creating/updating records in Dynamics 365 (e.g., Contacts, Leads)
-Logging user preferences for future use

Instead, if the user does not provide consent, Abby:
-Operates in a limited mode, offering only generic certification information pulled from public sources.
-Does not save any user data or offer personalized guidance.

🔐 Data Consent & Privacy Handling
Consent management is a core part of Abby's logic:
--- Users are explicitly shown PeopleCert’s Terms of Service and must opt-in before Abby activates any personalized features.

Without consent:
--- No variables are saved.
--- Very limited context is tracked during the chat, and can be discarded afterwards 
(not built in this PoC, but we can run a flow based on the consent variable, to delete from the OOB Transcript tables in Dataverse)

The AI agent functions in a read-only, informational capacity.

🎯 Vision & Next Steps
This solution is built as a robust and scalable PoC with clear pathways for extension:
We deliberately avoided using preview features to ensure long-term reliability.

After the Hackathon, we aim to:
--- Expand the range of certifications Abby can recommend.
--- There is currently about 90% multilingual support as almost everything is said with a Gen AI answers node. 
We aim to bring this to 100% so that we can utilize Generative Answers' OOB support of ~27 languages.
--- Refine and extend persona matching logic.
--- Deepen CRM integration with further actions.
--- Conduct User Acceptance Testing (UAT) before making Abby available to external users.

Ultimately, our goal is to evolve Abby into a trusted digital career assistant, capable of understanding each user’s unique goals and guiding them toward their next professional milestone with PeopleCert.

📩 Contact
For more information or collaboration inquiries, please contact the PeopleCert MSFT Business Application team at MicrosoftApplicationTeam@peoplecert.org.
