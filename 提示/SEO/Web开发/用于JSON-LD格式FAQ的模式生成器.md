  tags: 
- 提示
- SEO
- Web开发
- prompt普通

  AuthorName:Andrew Sheshunov

  AuthorURL:https://www.linkedin.com/in/andrii-sheshunov-a20236a2/

  Title:用于JSON-LD格式FAQ的模式生成器

  Category:Web Development

  Teaser:请用JSON格式撰写带有答案的问题，并获得简单的标记代码。

  Community:SEO-84c5d6a7b8e9f0c1

  CreationTime:2023-02-23T10:37:32.415Z

  Help:

  ID:1794286670221402112

  PromptHint:写出一行问题，然后每行回答一个。

  PromptPackageID:0

  ---

  ## Prompt:我希望你能够作为一名网页开发人员，根据schema.org文档，有经验地编写json-ld格式的模式标记代码。你需要在type="application/ld+json"中提供代码schemaFAQPage，其中包含下一个问题和答案：
[PROMPT]
将用户提供的问题和答案的文本输出到标记代码中，以[TARGETLANGUAGE]为目标语言。

  ```json
  {
  "id":"1794286670221402112",
    "creationTime":"2023-02-23T10:37:32.415Z",
    "title":"用于JSON-LD格式FAQ的模式生成器",
    "prompt":"我希望你能够作为一名网页开发人员，根据schema.org文档，有经验地编写json-ld格式的模式标记代码。你需要在type=\"application/ld+json\"中提供代码schemaFAQPage，其中包含下一个问题和答案：\n[PROMPT]\n将用户提供的问题和答案的文本输出到标记代码中，以[TARGETLANGUAGE]为目标语言。",
    "teaser":"请用JSON格式撰写带有答案的问题，并获得简单的标记代码。",
    "community":"SEO-84c5d6a7b8e9f0c1",
    "authorName":"Andrew Sheshunov",
    "category":"Web Development",
    "authorURL":"https://www.linkedin.com/in/andrii-sheshunov-a20236a2/",
    "promptPackageID":"0",
    "help":"",
    "promptHint":"写出一行问题，然后每行回答一个。"
  }
  ```
