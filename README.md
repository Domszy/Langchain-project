#### Financial Sentiment Analysis with LangChain and OpenAI API
This project is designed to perform financial sentiment analysis on news headlines using LangChain with OpenAI's API. It explores various key concepts, including prompt templates, language model (LLM) chains, agents and tools, and techniques like few-shot learning and moderation.

#### Key Learning Points
1. Completion Model

* A completion model generates a response based on a given prompt, designed to "complete" a task or input by producing a relevant output. It’s crucial for natural language generation tasks.
* Key Concepts: Prompt and Response/Output

2. Prompt Templates
* LangChain supports two types of prompt templates that structure the input prompts based on the context of the interaction:

* PromptTemplate:
   * Purpose: For standard, single-turn prompts.
   * Use Case: Text-based prompts where conversational context isn’t required.

* ChatPromptTemplate:
   * Purpose: For chat-based, multi-turn conversations, maintaining context between exchanges.
   * Use Case: Chatbot or dialogue applications needing a back-and-forth interaction.

3. Setting Up LLM Chains
* LangChain simplifies interactions with large language models (LLMs) by managing workflows, chaining prompts, tools, and models. It enables the creation of dynamic, multi-step applications. Two common model types used here are:

   * OpenAI: For completion-based prompts.
   * ChatOpenAI: For chat-based prompts that support conversational exchanges.

4. Output Parsers
* Purpose: Output parsers help structure and format responses from the model into a useful format like lists, tables, or JSON, ensuring outputs align with the desired structure.

5. Agents and Tools
* Agents: Act as decision-makers, breaking down complex tasks into actionable steps and choosing the right tools to use. They apply the MRKL (Modular Reasoning, Knowledge, and Language) approach to effectively prompt the LLM.

* Tools: Functional components such as APIs or specific code execution functions. For example, agents might call Python tools for calculations or a search API to fetch information.

Additional Configurations:
* `max_token`: Limits response length, controlling computation costs.
* `verbose=True`: Enables visibility of the agent’s actions, aiding debugging and transparency.

6. Few-Shot Learning
Purpose: To improve model accuracy on specific, nuanced tasks by providing examples that help guide the model’s responses.
* How It Works: A few example input-output pairs (1-5) are embedded within the prompt, helping the model generalize from these examples for new inputs. Alternatively, providing clear guidelines can tailor model behavior.

7. OpenAI Moderation - Predicting Offensive Content
The moderation feature evaluates and flags inappropriate or harmful content. The OpenAI Moderation API reviews the input text and returns feedback on whether it meets safety standards, ensuring that content aligns with acceptable use policies.

#### Usage Instructions
1. Installation:

* Download the repo onto your local device and use your favourite IDE in assessing the codebase. 
* Configure your OpenAI API keys and insert it into your `.env` file as such:
```
OPENAI_API_KEY = "YOUR OPEN AI API KEY" 
```
* Ensure that you have set up a payment method for your OpenAI developer account. Additional information on how you can set up your openAI account and set a payment method can be found in [getting-started.ipynb](./getting-started.ipynb). 

2. Run the `notebook.ipynb` file. 

#### Conclusion

This project demonstrates a structured, modular approach to financial sentiment analysis using LangChain and OpenAI. Key techniques like prompt templates, LLM chains, agents, few-shot learning, and moderation enhance the model's ability to process and analyze financial data dynamically.


