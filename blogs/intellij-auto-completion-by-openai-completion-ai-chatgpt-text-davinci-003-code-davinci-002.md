# Intellij Smart Completion by OpenAI NLP Completion(ChatGPT: text-davinci-003, code-davinci-002)

## Background

Intellij is a very powerful development tool that is widely used for software development. As ChatGPT models trained by OpenAI become smarter and smarter, we have developed an Intellij plugin called EDQL. This plugin translates ChatGPT's ability to write code intelligently into code

Install and Try: [https://github.com/chengpohi/edql/releases/tag/v1.9.16](https://github.com/chengpohi/edql/releases/tag/v1.9.16)

## EDQL's capabilities: natural language to code conversion

<figure><img src="/.gitbook/assets/java-code-generation.gif" alt=""><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/openai-query.gif" alt=""><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/filetype-settings.gif" alt=""><figcaption></figcaption></figure>

EDQL is a plugin for Intellij platform, which integrates Intellij and ChatGPT's capabilities, and brings ChatGPT's intelligent complementary capabilities to Intellij, helping developers to realize the ability to generate executable code based on transforming natural language in annotations, in order to also try to introduce more capabilities, such as contextual analysis, test generation, code interpretation and more.&#x20;

Also, EDQL supports users to configure their own OpenAI api key, stop words, prompt, etc., and use prompt to achieve more accurate code generation or completion. Usage:&#x20;

* When the cursor is in the comment, use the shortcut **ALT + BACK\_SLASH** to request code generation, then after getting the completion, the editor will show the suggested completion&#x20;
* if it meets the current completion, use the **TAB** key to apply the code to insert the code block&#x20;
* if not use **ESC** to cancel the completion, then modify the comment to continue to request the completion.&#x20;

The default complement model for the current language configuration is GPT3 (text-davinci-003).

## Privacy: safe and secure code generation

EDQL plugin has a built-in default OpenAI key, which can only be implemented using the code-davinci-002 model, because at this stage the model is free, while for the smarter chatgpt model: text-davinci-003 requires users to fill in their own api key manually. For sending requests: Currently Only the content of the caret where the editor cursor is located will be sent to openai, of course for privacy, it is strongly recommended to use your own openai key.

## Future plans: smarter and better features

We plan to keep improving the EDQL plugin in the future to make it smarter and better. We will add new features such as smarter context and completion, and test code generation. We will continue to work hard to meet the needs of our users for better, more useful and convenient code generation tools. We hope that EDQL will become a great tool for developers, helping them to be more productive and save more time, so that they can focus more on the logic and implementation of the code. The future EDQL will definitely be smarter and better, and become an indispensable tool for developers.

Translated with www.DeepL.com/Translator (free version)
