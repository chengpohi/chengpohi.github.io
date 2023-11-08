# Smart Query Elasticsearch with Openai Natural Language Completion(ChatGPT models)

## Background

Users often use Elasticsearch Query DSL to help them query data quickly. But when querying with complex DSL syntax,
there are still some problems, such as syntax errors or inaccuracies, leading to countless bugs in the code, and it is a
real headache to find the bugs that have appeared in thousands of codes.

To solve this problem, we innovatively adopt the hottest ChatGPT model now provided by OpenAI in the EDQL plugin, by
combining ChatGPT with Elasticsearch DSL, to help people use natural language in Intellij IDE to query data easily and
improve search efficiency. (In the test GPT3 model is able to convert natural language into most accurate queries)

Install and Try
it: [https://github.com/chengpohi/edql/releases/tag/v1.9.16](https://github.com/chengpohi/edql/releases/tag/v1.9.16)

<figure><img src="../.gitbook/assets/openai-query (1).gif" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/openai-settings.gif" alt=""><figcaption></figcaption></figure>

## What is EDQL

EDQL is a professional query and management tool for Elasticsearch based on the Intellij platform. It is used to manage
Elasticsearch clusters and query data from Elasticsearch with the following features.

1. EDQL is fully compatible with the official Query DSL, and you can directly copy the Query DSL and run it on EDQL
   without any extra effort.
2. EDQL has a visual editor that allows you to quickly write query conditions through an interactive UI.
3. With a powerful scripting engine: support for functions, variables, iterations, etc. Using Smart Intellij, you can
   easily write query DSL (refactoring, extraction, etc.).

## What is the ChatGPT model&#x20;

OpenAI's ChatGPT model is a pre-trained natural language processing model that generates natural language text. It is a
large deep learning model that has been widely used for a variety of natural language processing tasks.

What ChatGPT features are accessed in the EDQL plugin

1. Support custom OpenAI ChatGPT api key Open EDQL plugin, you can set a custom api key, and then you can experience its
   powerful functions at will.
2. Support stop words, prompt prefixes and suffixes Code-DaVinci-002, which we have access to in EDQL, is a chatbot
   model based on OpenAI's GPT-3 technology. The Code-DaVinci-002 model has been rigorously trained and tested to
   provide accurate, timely, and professional knowledgeable answers and advice. In addition, the Code-DaVinci-002 model
   also supports custom dictionaries, stop words, hint prefixes and hint suffixes to improve query efficiency and
   accuracy.
3. Intelligent recommendation of search terms ChatGPT can also intelligently recommend relevant search terms based on
   search history and other related information for faster and more convenient query data.

## What are the benefits of using ChatGPT in EDQL plugin?

1. No need to remember complicated syntax or struggle to understand the characteristics of the language. Have you ever
   encountered a situation where you are writing code and can't think of a certain syntax, making it impossible to
   continue writing? With ChatGPT, you only need a few words to tell it what you need, and it will write the code for
   you without having to memorize the syntax that is always being updated.&#x20;
2. ChatGPT can improve your work efficiency by answering your questions quickly and accurately, reducing the time spent
   on researching and finding information. In addition, using ChatGPT technology allows you to quickly generate code,
   save time on handwritten code, and check and modify code to ensure correctness and quality. chatGPT can also assist
   programmers in performing documentation and project management tasks, further improving productivity.&#x20;
3. Reduce or avoid code bugs. ChatGPT can help you find bugs quickly and provide the right code solution to reduce code
   errors.
