# AI2Apps

## 新闻

- **[2024-04-14]** 我们在arXiv上发布了论文“[AI2Apps: A Visual IDE for Building LLM-based AI Agent Applications](https://arxiv.org/abs/2404.04902)”!
- **[2023-0x-0x]** 我们发布了xxx!

传统LLM-based AI agent运维平台在大幅降低用户开发门槛的同时，往往难以兼顾对专业开发者的需求支持，从而制约了设计、编码、调试的灵活性，不利于未来发展更复杂的AI agent应用。AI2Apps作为首个面向LLM-based AI agent应用的可视化集成开发环境（Virtual IDE），覆盖了从原型设计、代码编写、Agent调试以及最终打包发布的完整开发周期，可帮助开发者高效地构建AI Agent应用。

AI2Apps 基于便捷高效的[Tab-OS](assets/tab_os.md)操作系统，提供了完整的网页化的可视化开发工具。
AI2Apps 拥有很多强大易用的 AI 控件，开发者可以在几分钟内通过拖拽迅速构建自己的 AI Agent，并直接生成可以发布的App。 

![home](assets/ai2apps_framework.png)

### 使用特点
AI2Apps集成了工程级的开发工具，以及覆盖前后端的全栈式可视化组件，使得开发者能够通过组件拖拽与代码编程并行的方式在一套“画布”GUI上进行一站式的agent应用构建，开发效率大大提升。
- #### 设计即开发
通过拖拽绘制拓扑图，快速设计Agent逻辑，拓扑图自动同步为Agent代码，节省大量编程时间。
传统开发模式无法保证代码与原始设计的同步，导致设计文档在维护时常常无效。而AI2Apps的"设计即开发"模式确保了代码与设计的实时同步，避免设计与实现脱节。
相比逐行阅读晦涩代码，包含拓扑图的AI Agent代码在后期维护中具有巨大优势，不仅能清晰掌握原有设计思路，还能更快速定位代码问题。

- #### 跨系统使用
开发完成的 AI Agent 可以打包输出为独立的网页/移动App（目前支持iOS和安卓系统）。也可以作为 AI 扩展集成入
现有的网页/App，仅需几行代码就可以完成整合。  

- #### 添加新插件
AI2Apps 可以通过 Add-On 方便的进行功能扩展，开发者可以根据需要引入自己的工具包和插件。如[RAG](axamples/rag.md) 

### 使用优势

#### 团队协作
AI2Apps借鉴了知名协作设计工具Figma的理念，支持开发者通过二维码链接向协作者实时共享其创作进度，并通过内置的版本控制功能实现协作开发。
#### 实际部署
AI2Apps具备Web-IDE特性，并且自带浏览器沙盒环境，将每个agent项目低消耗地安全隔离在独立的浏览器Tab页面，无需在端侧配置Docker等容器环境。
#### 拓展应用
任何领域任何类型的LLM-based AI agent应用开发。就像VScode等通用IDE一样，AI2Apps具有完全开放的扩展性，开发者可以将外部代码封装成微服务的形式，插入AI2Apps作为新的可视化组件使用。AI2Apps既可以单独作为Web-IDE使用，也便于被集成进大语言模型运维平台。

如果您觉得我们的工作对您有帮助，请引用我们的[AI2apps](https://arxiv.org/abs/2404.04902)。



  




## 快速开始
AI2Apps可以直接在网页中使用，也可以用本项目部署在本地使用。

### 1. 直接使用网页版
用桌面浏览器访问： [https://www.ai2apps.com](https://www.ai2apps.com)  
第一次打开网页会进行开发环境安装与配置，根据浏览器以及网络的不同，大概需要几秒到1分钟的时间。  
测试期间，要访问 AI 模型，需要注册并登录 Tab-OS（注册 Tab-OS 账号完全免费）。成功注册/登录后，
就可以使用项目向导就创建 AI Agent 项目了。

### 2. 部署本地环境
在本地环境下载本项目：
```
git clone https://github.com/Avdpro/ai2apps.git
```
**在ai2apps目录下：**  
编辑 `.env` 文件，配置正确的OpenAI Key以及服务端口，默认的端口是3015：
```
APIROOT=https://www.ai2apps.com/ws/
OPENAI_API_KEY=sk-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
PORT=3015
```

安装依赖：
```
nmp install
```

启动服务：
```
node ./start.js
```

假设指定的端口是3015，则用浏览器打开:
`http://localhost:3015/`
与直接使用ai2apps.com一样，第一次访问会进行安装配置。  
  
<p align="center">
<img src="assets/aahome_cn.png" alt="home" width="600" height="400" />
</p>
这是成功启动后的AI2Apps桌面状态。点击左侧 Dock 中的"项目向导"开始创建 AI Agent项目。当前版本有几个可以选择的 AI Agent 项目模版。要创建最简单的 AI Agent，可以选择第一个模版："简单的 AI Agent 应用"开始。  
输入项目名称路径（例如：MyAgent）后，点击创建按钮，系统会创建并打开项目开发环境。  
  
<p align="center">
<img src="assets/aaide_01_cn.png" alt="home" width="600" height="400" />
</p>

## 如何编写 Agent
在AI2Apps中，每个 Agent 是一个独立的js文件，拓扑图信息以注释的形式保存在文件末尾，
从而保证了设计与实现随时同步。  
Agent文件编辑界面有"代码"和"画布"两种模式，打开 Agent 后默认进入画布模式。
下面展示了一些 Agent 案例
- ## RAG ##
- ## xxx ##
- ## xxx ##

## 引用
如果您觉得我们的工作对您的研究或应用有帮助，请引用我们的论文[AI2Apps](https://arxiv.org/abs/2404.04902)
```
@article{pang2024ai2apps,
  title={AI2Apps: A Visual IDE for Building LLM-based AI Agent Applications},
  author={Pang, Xin and Li, Zhucong and Chen, Jiaxiang and Cheng, Yuan and Xu, Yinghui and Qi, Yuan},
  journal={arXiv preprint arXiv:2404.04902},
  year={2024}
}
```

