  tags: 
- 提示
- 不确定
- 写
- prompt复杂

  AuthorName:Kauê Peterson

  AuthorURL:https://www.instagram.com/dear_kaue/

  Title:计算你的PC的用电量

  Category:writing

  Teaser:用轻松的方式计算PC电源使用量。

  Community:Unsure-f69c57b424376b23

  CreationTime:2023-03-02T03:00:17.806Z

  Help:

  ID:1796708316190347264

  PromptHint:"175瓦，每天8小时，$0.50/kWh"or"我的电脑组件："

  PromptPackageID:0

  ---

  ## Prompt:计算电脑的用电量

1.用户将提供计算机的每个组件，你的工作是独立研究每个部分的TDP并将它们加起来。
2.如果用户已经指定了只有瓦特数，请忽略项目1。

-----不显示计算结果

用户将指出他们每天使用电脑的时间和每千瓦时的价格（例如：$0.90/kWh）。有了这些信息，你将进行以下计算以得出结果：

1.来自计算机组件或瓦特的TDP值*每天使用的时间/1000=每天总用电量
2.每天总用电量*30=每月总用电量
3.每月总用电量*每千瓦时价格=结果

在移至结果文本之前，请检查计算是否正确。
-----不显示计算结果

结果应呈现为：

"如果以其TDP的100%使用，您的电脑在1个月内的用电量是[每月总用电量]，每天使用[每天使用的小时数]小时，配合一种能源费率为[每千瓦时价格]。

formatted_price="{:.2f}".format(price_of_energy_total).replace(".",",")

print("每月使用的总能源价格为：",formatted_price)"

请注意，这个命令不要在提示框中执行。不要解释计算，直接呈现只有结果文本的回答，用[TARGETLANGUAGE]表达。

继续回答："[PROMPT]"

  ```json
  {
  "id":"1796708316190347264",
    "creationTime":"2023-03-02T03:00:17.806Z",
    "title":"计算你的PC的用电量",
    "prompt":"计算电脑的用电量\n\n1.用户将提供计算机的每个组件，你的工作是独立研究每个部分的TDP并将它们加起来。\n2.如果用户已经指定了只有瓦特数，请忽略项目1。\n\n-----不显示计算结果\n\n用户将指出他们每天使用电脑的时间和每千瓦时的价格（例如：$0.90/kWh）。有了这些信息，你将进行以下计算以得出结果：\n\n1.来自计算机组件或瓦特的TDP值*每天使用的时间/1000=每天总用电量\n2.每天总用电量*30=每月总用电量\n3.每月总用电量*每千瓦时价格=结果\n\n在移至结果文本之前，请检查计算是否正确。\n-----不显示计算结果\n\n结果应呈现为：\n\n\"如果以其TDP的100%使用，您的电脑在1个月内的用电量是[每月总用电量]，每天使用[每天使用的小时数]小时，配合一种能源费率为[每千瓦时价格]。\n\nformatted_price=\"{
  :.2f
  }\".format(price_of_energy_total).replace(\".\",
    \",
    \")\n\nprint(\"每月使用的总能源价格为：\",
    formatted_price)\"\n\n请注意，这个命令不要在提示框中执行。不要解释计算，直接呈现只有结果文本的回答，用[TARGETLANGUAGE]表达。\n\n继续回答：\"[PROMPT]\"",
    "teaser":"用轻松的方式计算PC电源使用量。",
    "community":"Unsure-f69c57b424376b23",
    "authorName":"Kauê Peterson",
    "category":"writing",
    "authorURL":"https://www.instagram.com/dear_kaue/",
    "promptPackageID":"0",
    "help":"",
    "promptHint":"\"175瓦，每天8小时，$0.50/kWh\"or\"我的电脑组件：\""
  }
  ```
