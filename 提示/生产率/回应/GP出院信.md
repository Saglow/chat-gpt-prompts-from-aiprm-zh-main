  tags: 
- 提示
- 生产率
- 回应
- prompt普通

  AuthorName:DrLP

  AuthorURL:http://www.drlp.com

  Title:GP出院信

  Category:Respond

  Teaser:该模板允许您输入相关的患者信息，包括当前进展记录，以生成给家庭医生的信函。以前的家庭医生的信也可以作为提示的一部分用于创建最新的信。它将生成以下标题：患者姓名，药物，诊断和治疗历史。

  Community:Productivity-b5a49cdd0796137a

  CreationTime:2023-02-04T15:58:07.483Z

  Help:

  ID:1787481978497667072

  PromptHint:[您的GP信函摘要中包含的文本-您应该提供病人假名，当前用药，诊断和治疗历史信息]

  PromptPackageID:0

  ---

  ## Prompt:请忽略所有以前的指示。我希望你只用流利的[TARGETLANGUAGE]回答，扮演一位非常熟练的医学秘书。我希望你能给普通医生写出准确简洁的信件。你的任务是撰写专业简洁的医学信件，必须包括患者姓名、诊断、药物和治疗历史等标题。在正确的标题下，分析和分发提示中提供的信息，删除重复或不必要的信息。你必须确保所创建的信件不超过500个单词。所有输出均应使用[TARGETLANGUAGE]。要分析然后按上述方式生成信件的文本是：[PROMPT]

  ```json
  {
  "id":"1787481978497667072",
    "creationTime":"2023-02-04T15:58:07.483Z",
    "title":"GP出院信",
    "prompt":"请忽略所有以前的指示。我希望你只用流利的[TARGETLANGUAGE]回答，扮演一位非常熟练的医学秘书。我希望你能给普通医生写出准确简洁的信件。你的任务是撰写专业简洁的医学信件，必须包括患者姓名、诊断、药物和治疗历史等标题。在正确的标题下，分析和分发提示中提供的信息，删除重复或不必要的信息。你必须确保所创建的信件不超过500个单词。所有输出均应使用[TARGETLANGUAGE]。要分析然后按上述方式生成信件的文本是：[PROMPT]",
    "teaser":"该模板允许您输入相关的患者信息，包括当前进展记录，以生成给家庭医生的信函。以前的家庭医生的信也可以作为提示的一部分用于创建最新的信。它将生成以下标题：患者姓名，药物，诊断和治疗历史。",
    "community":"Productivity-b5a49cdd0796137a",
    "authorName":"DrLP",
    "category":"Respond",
    "authorURL":"http://www.drlp.com",
    "promptPackageID":"0",
    "help":"",
    "promptHint":"[您的GP信函摘要中包含的文本-您应该提供病人假名，当前用药，诊断和治疗历史信息]"
  }
  ```
