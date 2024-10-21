# GenAi-AI_Act

## Instruction

EU AI Act Compliance Assistant
•	Description: Create a tool that assists companies or developers in ensuring compliance with the new EU AI Act, based on relevant legal documents, official guidelines, and regulatory frameworks.
•	Use Case: Support organizations in navigating the AI Act’s requirements, such as transparency, risk management, and data governance, offering tailored advice based on the specifics of their AI systems.
•	Challenges: Navigating complex regulatory language, providing real-time updates on evolving regulations, adapting to different industries’ needs, and clarifying legal terminology for non-specialists.
Reference data
EU law is publicly available and accessible in multiple languages.
•	AI Act Overview
•	EU Regulation - 2024/1689
•	AI Act Q&A
There are some deterministic compliance checkers online that can help building a relevant validation methodology.
•	EU AI Act Compliance Checker | EU Artificial Intelligence Act from futureoflife.org
•	EU AI Act Compliance Checker from trail-ml.com


## Exploratory evaluation 

Does your current chatbot provide an answer? How credible is it? Is it factually accurate?

- Problems using different languages. When asking in spanish what is the IA act, simply answering me some information about what is an IA but no providing law information.
- Seems like the Llama3.2 doesn't know about the AI act, he only knows about RGPD and the 2009/136/CE's directive.
- Les données ne sont disponibles que jusqu'à decembre 2023.

What if you include in your prompt the relevant info from your documentation (by copy-pasting)? Does it give you a better answer?

- By copy-pasting the documentation in our prompt, it gives better answers. 

### Example without giving the documentation

Prompt : How does the AI Act regulate biometric identification?
Answer : The AI Act regulates biometric identification in several ways:

Transparency requirements : Biometric identification systems must provide clear and concise information about how they work, including the types of data they collect, how they are used, and who is responsible for them.
Consent requirements : Individuals must give explicit consent before their biometric data is collected and processed. Consent must be informed, unambiguous, and freely given.
Data minimization : Biometric identification systems must only collect and process the minimum amount of data necessary to achieve their purpose. This means that unnecessary data collection and storage are prohibited.
Anonymization and pseud anonymization : The AI Act allows for the use of anonymized or pseudonimized biometric data, which is data that cannot be linked back to an individual. However, this is only permitted if the data is properly secured and can be easily re-identified.
Data protection : Biometric identification systems must comply with EU data protection laws, including the General Data Protection Regulation (GDPR).
Regular security audits : Biometric identification systems must undergo regular security audits to ensure that they are not vulnerable to cyber attacks or other security breaches.
Access controls : Biometric identification systems must have robust access controls in place to prevent unauthorized access to the data.
Data retention and deletion : Biometric identification systems must establish clear guidelines for data retention and deletion, including how long biometric data will be stored and under what circumstances it will be deleted.
The AI Act also establishes specific requirements for the use of biometric data in certain contexts, such as:

Law enforcement : Biometric data can only be used by law enforcement agencies with a warrant or other legal authority.
Border control : Biometric data can only be used by border control authorities for the purpose of identifying individuals crossing borders.
Employment : Biometric data can only be used by employers to verify an individual's identity and check their employment status.
The AI Act also includes provisions for the protection of vulnerable populations, such as children and individuals with disabilities, who may be disproportionately affected by biometric identification systems.

Overall, the AI Act aims to ensure that biometric identification systems are designed and used in a way that respects individuals' rights and freedoms, while also promoting innovation and economic growth.

### Example by giving the documentation to the model

Prompt: The use of real-time remote biometric identification in publicly accessible spaces (i.e. facial recognition using CCTV) for law enforcement purposes is prohibited. Member States can introduce exceptions by law that would allow the use of real-time remote biometric identification in the following cases:

Law enforcement activities related to 16 specified very serious crimes;
Targeted search for specific victims, abduction, trafficking and sexual exploitation of human beings, and missing persons; or
The prevention of threat to the life or physical safety of persons or response to the present or foreseeable threat of a terror attack.
Any exceptional use would be subject to prior authorisation by a judicial or independent administrative authority whose decision is binding. In case of urgency, approval can be granted within 24 hours; if the authorisation is rejected all data and output must be deleted.

It would need to be preceded by prior fundamental rights impact assessment and should be notified to the relevant market surveillance authority and the data protection authority. In case of urgency, the use of the system may be commenced without registration.
How does the AI Act regulate biometric identification?

Answer: The AI Act regulates biometric identification in several ways:

Prohibition on real-time remote biometric identification : The use of real-time remote biometric identification, such as facial recognition using CCTV, for law enforcement purposes is prohibited in publicly accessible spaces.
Exceptions allowed by law : Member States can introduce exceptions by law that would allow the use of real-time remote biometric identification in specific cases, including:
Law enforcement activities related to 16 specified very serious crimes
Targeted search for specific victims, abduction, trafficking and sexual exploitation of human beings, and missing persons
Prevention of threat to the life or physical safety of persons or response to the present or foreseeable threat of a terror attack
Prior authorisation required : Any exceptional use of real-time remote biometric identification must be subject to prior authorisation by a judicial or independent administrative authority whose decision is binding.
Urgent approval possible : In cases of urgency, approval can be granted within 24 hours, but if the authorisation is rejected, all data and output must be deleted.
Prior fundamental rights impact assessment required : Any exceptional use of real-time remote biometric identification must precede a prior fundamental rights impact assessment to ensure that it does not infringe on individuals' rights and freedoms.
Notification to relevant authorities : The use of the system must be notified to the relevant market surveillance authority and the data protection authority.
Urgent use possible without registration : In cases of urgency, the use of the system may be commenced without registration.
Overall, the AI Act aims to balance the need for law enforcement to use biometric identification with the need to protect individuals' rights and freedoms. The provisions above ensure that any exceptional use of real-time remote biometric identification is subject to rigorous oversight and approval processes to prevent abuse and ensure transparency.

It's worth noting that the AI Act also includes other provisions related to biometric identification, such as:

Data minimization : Biometric data should only be collected and processed to the minimum extent necessary to achieve its purpose.
Anonymization and pseud anonymization : Biometric data can be anonymized or pseudonimized if it is properly secured and can be easily re-identified.
Security requirements : Biometric identification systems must meet specific security requirements to prevent unauthorized access and cyber attacks.
These provisions aim to ensure that biometric identification is used in a way that respects individuals' rights and freedoms, while also promoting innovation and economic growth.


## Main criteria to be satisfied by our LLM assistant

Since it is about regulation, we want to focus on the quality of the answer.
The length of the answer is an important metric, knowing that we want exhaustive and detailed answers.
Of course the reliability of the answer is a major part of a successful model.
Also, we need to be sure that the user understood, so the user's feedback is an essential metric to ensure a good improvement.

The model should not help to bypass the EU AI Act.
