  tags: 
- 提示
- Generative
- 稳定扩散
- prompt普通

  AuthorName:joker

  AuthorURL:https://photolessons.org/

  Title:在稳定扩散中创建AI标志。

  Category:Stable Diffusion

  Teaser:在指定的主题[关键词]上创建标志的详细说明。

  Community:Generative-AI-b983edfcaa490850

  CreationTime:2023-03-09T07:09:18.824Z

  Help:

  ID:1799307698421100544

  PromptHint:使用短文本而非长描述[关键词]

  PromptPackageID:0

  ---

  ## Prompt:您应该充当设计师。对于主题为[关键字]的AI图像生成请求编写详细说明。最后，按照指定格式在[TARGETLANGUAGE]中写下一行最终查询的原始格式：

"/imagineprompt：[KEYWORD]，[Style]，[Background]，[Activity]，[Poses]，[Expression]，[Otherfeatures]"

在查询中，所有字母都应为小写。在[关键字]，[Style]，[Background]，[Activity]，[Poses]，[Expression]，[Otherfeatures]而不是[]中放入每个值的描述，例如结果应为：[关键字]+“：：2.5”，[Style]+“：：1.5”，[背景]+“：：2”，[活动]+“：：1.5”，[姿势]+“：：1”，[表情]+“：：1”，[其他特征]+“：：0.5”。

请删除请求中的[]和""！保留“::”后面的数字！请求应为英语！

  ```json
  {
  "id":"1799307698421100544",
    "creationTime":"2023-03-09T07:09:18.824Z",
    "title":"在稳定扩散中创建AI标志。",
    "prompt":"您应该充当设计师。对于主题为[关键字]的AI图像生成请求编写详细说明。最后，按照指定格式在[TARGETLANGUAGE]中写下一行最终查询的原始格式：\n\n\"/imagineprompt：[KEYWORD]，[Style]，[Background]，[Activity]，[Poses]，[Expression]，[Otherfeatures]\"\n\n在查询中，所有字母都应为小写。在[关键字]，[Style]，[Background]，[Activity]，[Poses]，[Expression]，[Otherfeatures]而不是[]中放入每个值的描述，例如结果应为：[关键字]+“：：2.5”，[Style]+“：：1.5”，[背景]+“：：2”，[活动]+“：：1.5”，[姿势]+“：：1”，[表情]+“：：1”，[其他特征]+“：：0.5”。\n\n请删除请求中的[]和\"\"！保留“::”后面的数字！请求应为英语！",
    "teaser":"在指定的主题[关键词]上创建标志的详细说明。",
    "community":"Generative-AI-b983edfcaa490850",
    "authorName":"joker",
    "category":"Stable Diffusion",
    "authorURL":"https://photolessons.org/",
    "promptPackageID":"0",
    "help":"",
    "promptHint":"使用短文本而非长描述[关键词]"
  }
  ```
