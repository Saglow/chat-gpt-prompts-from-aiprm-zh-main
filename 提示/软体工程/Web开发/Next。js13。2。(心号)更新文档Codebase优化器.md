  tags: 
- 提示
- 软体工程
- Web开发
- prompt复杂

  AuthorName:Preston Jenkins

  AuthorURL:https://google.com

  Title:Next.js13.2.*更新文档Codebase优化器

  Category:Web Development

  Teaser:使用更新的Next.js13.2文档与客户端和服务器端组件进行ChatGPT对话，以及其他一些内容。

  Community:SoftwareEngineering-f1858b980c341d28

  CreationTime:2023-03-20T02:34:21.677Z

  Help:

  ID:1803224770893058048

  PromptHint:请将以下句子翻译成[TARGETLANGUAGE]：只需转换为GitHub存储库zackees/gptrepo制作[output.txt]。不要翻译[]中的单词。

（Note:InEnglish,"GitHubrepo"isoftenusedasshorthandfor"GitHubrepository.")

  PromptPackageID:0

  ---

  ## Prompt:我是一个Next.js专家开发者，但我并不了解Next.js13.2所做的新更改。您为我提供了关于Next.js13.2的相关文档，我将仅用作参考。我将获得一个名为"output.txt"的Git存储库文件，其中包含如何浏览该文件的说明。在做任何其他事情之前，我将首先解析该文件的内容。一旦我能理解该文件的结构，我将使用我当前的知识和提供的参考文献建议对您的Git存储库进行具体更改。

＃您可以用作参考的文档，它与我的Git存储库没有直接关联，除了对此更新的Next.js13.2工作方式的更改＃

数据获取方法的更改：
-先前的Next.js数据获取方法（如getServerSideProps，getStaticProps和getInitialProps）不支持新的应用程序目录。
-相反，新的数据获取系统建立在本机fetch（）WebAPI之上，并在Server组件中使用async/await。
-尽可能使用Server组件获取数据。服务器组件始终在服务器上获取数据。
-动态渲染旨在是服务器端渲染的等效物，例如getServerSideProps（）。使用动态呈现，服务器和客户端组件在请求时在服务器上呈现。工作的结果不被缓存。

Next.js13.2.4中的服务器和客户端组件
-在新的更新中，建议使用React的服务器和客户端组件
-使用服务器和客户端组件，React可以在客户端和服务器上呈现，这意味着您可以在组件级别选择呈现环境。
-默认情况下，应用程序目录使用Server组件，这使得轻松在服务器上呈现组件，并减少发送到客户端的JavaScript量。
-您可以通过将客户端组件导入服务器组件或将服务器组件作为子项或属性传递给客户端组件来交错服务器和客户端组件。在幕后，React会合并两个环境的工作。

客户端组件特定信息：
-在文件顶部（在任何导入之前）使用“useclient”指令时，组件成为客户端组件。
-这些组件（和文件）可以放置在应用程序的任何位置。它们不需要特别放在app/中。
-仅当它们使用客户端钩子（如useState或useEffect）时，才需要将组件标记为"useclient"。最好将不依赖于客户端钩子的组件离开该指令，以便在它们未被另一个客户端组件导入时，可以自动呈现为Server组件。这有助于确保客户端JavaScript的最小化。
-Next.js中的客户端组件是基于服务器端呈现并在客户端上进行hydration，您可以将客户机组件视为Next.js12和早期版本的工作方式（即页面/目录）。

何时使用ServervsClient组件？
-两个组件：
--获取数据（可以在客户端组件中获取数据，建议在服务器组件中获取数据，除非有特定原因需要在客户端获取数据。将数据获取移至服务器可以提高性能和用户体验。）
-服务器组件：
--获取数据
--访问后端资源（直接）
--在服务器上保留敏感信息（访问令牌，API密钥等）
--在服务器上保留大型依赖项/减少客户端JavaScript
-客户端组件：
--添加交互性和事件侦听器（onClick（），onChange（）等）
--使用State和LifecycleEffects（useState（），useReducer（），useEffect（）等）
--使用仅限浏览器的API
--使用依赖于状态，效果或仅限浏览器API的自定义挂钩
--使用ReactClass组件

将服务器组件导入客户端组件：
-服务器和客户端组件可以交错在同一组件树中。在幕后，React会合并两个环境的工作。
-但是，在React中，有一个限制，即在客户端组件中引入服务器组件时，因为服务器组件可能具有仅限于服务器的代码（例如数据库或文件系统实用程序）。
--例如，在客户端组件中导入服务器组件将无法工作。
--相反，您可以将服务器组件作为客户端组件的子项或属性进行传递。您可以通过将两个组件都包装在另一个Server组件中来实现这一点。
-从服务器向客户端组件传递Props（序列化）
--从服务器组件传递给客户端组件的Props需要是可序列化的。这意味着诸如函数，日期等值无法直接传递给客户端组件。

将客户端组件移动到叶子：
-为了改善应用程序的性能，我们建议尽可能将客户端组件移动到组件树的叶子上。
-例如，您可能有一个布局，其中包含静态元素（例如徽标，链接等）和一个使用状态的交互式搜索栏。
-将整个布局变为客户端组件，而不是将交互逻辑移至客户端组件（例如<SearchBar/>），并将布局保留为服务器组件。这意味着您不必将整个组件的JavaScript发送到客户端。

＃结束参考文档＃

所有输出都应为[TARGETLANGUAGE]。

"output.txt"将有如何解析其结构的说明，但无论如何，这是由“output.txt”表示的完整Git存储库：

  ```json
  {
  "id":"1803224770893058048",
    "creationTime":"2023-03-20T02:34:21.677Z",
    "title":"Next.js13.2.*更新文档Codebase优化器",
    "prompt":"我是一个Next.js专家开发者，但我并不了解Next.js13.2所做的新更改。您为我提供了关于Next.js13.2的相关文档，我将仅用作参考。我将获得一个名为\"output.txt\"的Git存储库文件，其中包含如何浏览该文件的说明。在做任何其他事情之前，我将首先解析该文件的内容。一旦我能理解该文件的结构，我将使用我当前的知识和提供的参考文献建议对您的Git存储库进行具体更改。\n\n＃您可以用作参考的文档，它与我的Git存储库没有直接关联，除了对此更新的Next.js13.2工作方式的更改＃\n\n数据获取方法的更改：\n-先前的Next.js数据获取方法（如getServerSideProps，getStaticProps和getInitialProps）不支持新的应用程序目录。\n-相反，新的数据获取系统建立在本机fetch（）WebAPI之上，并在Server组件中使用async/await。\n-尽可能使用Server组件获取数据。服务器组件始终在服务器上获取数据。\n-动态渲染旨在是服务器端渲染的等效物，例如getServerSideProps（）。使用动态呈现，服务器和客户端组件在请求时在服务器上呈现。工作的结果不被缓存。\n\nNext.js13.2.4中的服务器和客户端组件\n-在新的更新中，建议使用React的服务器和客户端组件\n-使用服务器和客户端组件，React可以在客户端和服务器上呈现，这意味着您可以在组件级别选择呈现环境。\n-默认情况下，应用程序目录使用Server组件，这使得轻松在服务器上呈现组件，并减少发送到客户端的JavaScript量。\n-您可以通过将客户端组件导入服务器组件或将服务器组件作为子项或属性传递给客户端组件来交错服务器和客户端组件。在幕后，React会合并两个环境的工作。\n\n客户端组件特定信息：\n-在文件顶部（在任何导入之前）使用“useclient”指令时，组件成为客户端组件。\n-这些组件（和文件）可以放置在应用程序的任何位置。它们不需要特别放在app/中。\n-仅当它们使用客户端钩子（如useState或useEffect）时，才需要将组件标记为\"useclient\"。最好将不依赖于客户端钩子的组件离开该指令，以便在它们未被另一个客户端组件导入时，可以自动呈现为Server组件。这有助于确保客户端JavaScript的最小化。\n-Next.js中的客户端组件是基于服务器端呈现并在客户端上进行hydration，您可以将客户机组件视为Next.js12和早期版本的工作方式（即页面/目录）。\n\n何时使用ServervsClient组件？\n-两个组件：\n--获取数据（可以在客户端组件中获取数据，建议在服务器组件中获取数据，除非有特定原因需要在客户端获取数据。将数据获取移至服务器可以提高性能和用户体验。）\n-服务器组件：\n--获取数据\n--访问后端资源（直接）\n--在服务器上保留敏感信息（访问令牌，API密钥等）\n--在服务器上保留大型依赖项/减少客户端JavaScript\n-客户端组件：\n--添加交互性和事件侦听器（onClick（），onChange（）等）\n--使用State和LifecycleEffects（useState（），useReducer（），useEffect（）等）\n--使用仅限浏览器的API\n--使用依赖于状态，效果或仅限浏览器API的自定义挂钩\n--使用ReactClass组件\n\n将服务器组件导入客户端组件：\n-服务器和客户端组件可以交错在同一组件树中。在幕后，React会合并两个环境的工作。\n-但是，在React中，有一个限制，即在客户端组件中引入服务器组件时，因为服务器组件可能具有仅限于服务器的代码（例如数据库或文件系统实用程序）。\n--例如，在客户端组件中导入服务器组件将无法工作。\n--相反，您可以将服务器组件作为客户端组件的子项或属性进行传递。您可以通过将两个组件都包装在另一个Server组件中来实现这一点。\n-从服务器向客户端组件传递Props（序列化）\n--从服务器组件传递给客户端组件的Props需要是可序列化的。这意味着诸如函数，日期等值无法直接传递给客户端组件。\n\n将客户端组件移动到叶子：\n-为了改善应用程序的性能，我们建议尽可能将客户端组件移动到组件树的叶子上。\n-例如，您可能有一个布局，其中包含静态元素（例如徽标，链接等）和一个使用状态的交互式搜索栏。\n-将整个布局变为客户端组件，而不是将交互逻辑移至客户端组件（例如<SearchBar/>），并将布局保留为服务器组件。这意味着您不必将整个组件的JavaScript发送到客户端。\n\n＃结束参考文档＃\n\n所有输出都应为[TARGETLANGUAGE]。\n\n\"output.txt\"将有如何解析其结构的说明，但无论如何，这是由“output.txt”表示的完整Git存储库：",
    "teaser":"使用更新的Next.js13.2文档与客户端和服务器端组件进行ChatGPT对话，以及其他一些内容。",
    "community":"SoftwareEngineering-f1858b980c341d28",
    "authorName":"Preston Jenkins",
    "category":"Web Development",
    "authorURL":"https://google.com",
    "promptPackageID":"0",
    "help":"",
    "promptHint":"请将以下句子翻译成[TARGETLANGUAGE]：只需转换为GitHub存储库zackees/gptrepo制作[output.txt]。不要翻译[]中的单词。\n\n（Note:InEnglish,
    \"GitHubrepo\"isoftenusedasshorthandfor\"GitHubrepository.\")"
  }
  ```
