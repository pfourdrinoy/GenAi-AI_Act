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

Since the assistant centers on regulatory compliance, several aspects are critical.
Each response must be both accurate and comprehensive, reflecting the detailed and exhaustive nature required by regulatory guidance. This ensures that the assistant provides not just relevant but also legally sound advice.
For regulatory topics, the length of the response is essential. Responses should be detailed enough to cover all necessary points while remaining digestible, balancing  User feedback should be collected to measure whether responses are clear and actionable. This metric helps ensure the model evolves based on user comprehension and satisfaction, improving the guidance provided.
The model should be strictly designed to support compliance efforts, not to provide information that could circumvent or undermine the EU AI Act’s provisions.

## Important metrics

### Answer quality metrics 
Edit Distance Metrics: The average edit distance measurement between user prompts and among LLM responses and retained content serves as an indicator of prompt refinement and content customization.
Prompt and response length: Average lengths of prompts and responses.Ensures that responses are concise but thorough. For regulatory compliance, overly lengthy or unclear answers can overwhelm users, while short responses may miss critical details.
ROUGE (Recall-Oriented Understudy for Gisting Evaluation): evaluates the quality of machine-generated text by comparing it to reference texts based on overlapping words and phrases. Help assessing how closely the tool's AI-generated compliance advice aligns with expert-written legal guidance, ensuring accuracy and trustworthiness in navigating the EU AI Act.

### User experience metrics
LLM conversation: Average number of LLM conversations per user. Gauges how often users consult the tool for compliance checks, showcasing its usability and importance in AI project development cycles.
User Feedback: Collects direct feedback (e.g., thumbs up/down) to improve the accuracy and relevance of the tool’s AI compliance advice.
Active days: Active days using LLM features per user. Reflects user engagement and long-term value. Regular, active users suggest the tool is valuable for ongoing compliance maintenance, not just one-off checks.

### Performance metrics
Requests per second (Concurrency): Number of requests processed by the LLM per second. Ensures the tool can handle multiple compliance checks from different users concurrently, which is crucial for scalability as more organizations adopt the tool.
Tokens per second: Counts the tokens rendered per second during LLM response streaming. Measures the speed of response generation, ensuring that the legal and regulatory advice is provided promptly.
Reliability: The percentage of successful requests compared to total requests, including those with errors or failures. Ensures high availability and accuracy, as the tool must consistently provide correct guidance to maintain trust and compliance with EU AI regulations.

### Cost metrics
GPU/CPU Utilization: Utilization in terms of total number of tokens. Tracks the resource efficiency of the tool, ensuring that compliance checks are handled in a cost-effective manner without unnecessary overhead for AI model inferences.
Infrastructure cost: Costs from storage, networking, computing resources, etc. Helps monitor the costs of running the tool on cloud infrastructure (storage, networking, computing), ensuring that it remains financially sustainable as usage grows.
Operation cost: Costs from maintenance, support, monitoring, logging, security measures, etc. Tracks the costs associated with supporting the tool (maintenance, support, security), ensuring compliance assistance is provided efficiently and affordably to users.

## Benchmarks for our LLM

### 1. **SuperGLUE**
   - **Purpose**: Tests comprehension of complex text and reasoning, essential for interpreting legal concepts and responding to nuanced questions about the AI Act.

### 2. **MMLU (Massive Multitask Language Understanding)**
   - **Purpose**: Assesses the model’s ability to cover diverse domains like law, ethics, governance, and technology, all crucial for AI regulation.

### 3. **Ethical and Safety Benchmarks (e.g., REAL Toxicity Prompts, Bias Tests)**
   - **Purpose**: Ensures the assistant avoids generating biased, toxic, or unethical responses, especially important for sensitive topics like the AI Act.

### 4. **BIG-bench**
   - **Purpose**: Tests advanced reasoning and creativity, necessary for explaining complex topics or addressing unexpected questions about regulation.

### 5. **SQuAD (Stanford Question Answering Dataset)**
   - **Purpose**: Measures the AI's ability to extract specific information from dense legal texts and respond accurately.

### 6. **Winogrande (Commonsense Reasoning)**
   - **Purpose**: Evaluates the model’s ability to make logical inferences in ambiguous legal scenarios and clarify regulatory implications.

### 7. **HumanEval (Legal Text Generation)**
   - **Purpose**: Verifies the model’s capacity to generate precise legal summaries or provide regulatory advice based on the AI Act.

### 8. **LAMBADA (Contextual Understanding)**
   - **Purpose**: Tests long-text comprehension, allowing the AI to maintain consistency in discussions around lengthy legal documents like the AI Act.

### Key Considerations for the AI Act Assistant
- **Legal accuracy**, **ethical sensitivity**, **robust reasoning**, and **transparency** are crucial to build an assistant that provides clear legal explanations and fosters user trust.
