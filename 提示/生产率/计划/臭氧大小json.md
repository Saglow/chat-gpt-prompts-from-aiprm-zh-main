  tags: 
- 提示
- 生产率
- 计划
- prompt复杂

  AuthorName:Fanc

  AuthorURL:https://chat.openai.com/chat?AIPRM_PromptID=1800401891319078912

  Title:臭氧大小json

  Category:Plan

  Teaser:奥致尺寸JSON

  Community:Productivity-b5a49cdd0796137a

  CreationTime:2023-03-12T07:37:14.74Z

  Help:

  ID:1800401891319078912

  PromptHint:"ozonsizejson"cannotbetranslatedintomeaningfulChinesewithoutadditionalcontextorinformation.

  PromptPackageID:0

  ---

  ## Prompt:[TARGETLANGUAGE]
[PROMPT]
请完成下面的步骤,每一步输出信息
1.将数据转换为公制单位（kg，cm），并以表格形式展示数据，表格线使用“|”符号表示
2.将上述数据翻译成俄文并按照json模板的格式转换成json数据,在代码块输出：
json模板:
{
"content":[
{
"widgetName":"tcTable",
"table":{
"title":"Справочныйразмер",
"body":[
{
"data":[
"Российскийразмер",
"56",
"57"
]
}
]
}
},
{
"widgetName":"tcDisclaimer",
"disclaimer":{
"body":"Вышеуказанныеразмерыизмеренывнатуральномвыражении,иможетбытьпогрешностьв1-3см.Соответствующиеданныеприведенытолькодлясправки,иреальныевещиимеютпреимущественнуюсилу."
}
}
],
"version":0.1
}

  ```json
  {
  "id":"1800401891319078912",
    "creationTime":"2023-03-12T07:37:14.74Z",
    "title":"臭氧大小json",
    "prompt":"[TARGETLANGUAGE]\n[PROMPT]\n请完成下面的步骤,
    每一步输出信息\n1.将数据转换为公制单位（kg，cm），并以表格形式展示数据，表格线使用“|”符号表示\n2.将上述数据翻译成俄文并按照json模板的格式转换成json数据,
    在代码块输出：\njson模板:\n{
  \n\"content\":[\n{
  \n\"widgetName\":\"tcTable\",
    \n\"table\":{
  \n\"title\":\"Справочныйразмер\",
    \n\"body\":[\n{
  \n\"data\":[\n\"Российскийразмер\",
    \n\"56\",
    \n\"57\"\n]\n
  }\n]\n
  }\n
  },
    \n{
  \n\"widgetName\":\"tcDisclaimer\",
    \n\"disclaimer\":{
  \n\"body\":\"Вышеуказанныеразмерыизмеренывнатуральномвыражении,
    иможетбытьпогрешностьв1-3см.Соответствующиеданныеприведенытолькодлясправки,
    иреальныевещиимеютпреимущественнуюсилу.\"\n
  }\n
  }\n],
    \n\"version\":0.1\n
  }",
    "teaser":"奥致尺寸JSON",
    "community":"Productivity-b5a49cdd0796137a",
    "authorName":"Fanc",
    "category":"Plan",
    "authorURL":"https://chat.openai.com/chat?AIPRM_PromptID=1800401891319078912",
    "promptPackageID":"0",
    "help":"",
    "promptHint":"\"ozonsizejson\"cannotbetranslatedintomeaningfulChinesewithoutadditionalcontextorinformation."
  }
  ```
