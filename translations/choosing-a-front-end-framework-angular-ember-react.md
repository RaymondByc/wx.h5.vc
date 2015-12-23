---
Title: ANGULAR VS. EMBER VS. REACT 如何选择前端框架
date: 2015-12-08 16:11
status: public
title: 'ANGULAR VS. EMBER VS. REACT 如何选择前端框架'
---

**当下最热的Web前端框架概览**
作为前端工程师，我们生在最好的时代。标题中提到的三大前端框架都即将或已经发布了重大更新。Ember 在不到2个月前发布了可以平滑升级的2.0。两周前 [React 发布了 0.14](http://facebook.github.io/react/blog/2015/10/07/react-v0.14.html)，在迈向1.0稳定版的路上迈出了关键的一步。在本周之内，一场名为AngularConnect的技术大会将在伦敦举行，很有可能公布 Angular 2 的时间计划。

是的，还有很多其他的前端框架。也还有很多一些曾经一度很火但是现在已经不那么流行了的库，比如 Backbone 和 Knockout。当然也还有更新更有趣的后起之秀，比如Aurelia。但是如果让你现在做决定选哪个框架来做web app的话，Angular， Ember 或 React 是比较安全的选择，因为他们背后都有长期有效的技术支持和活跃的开发者社区支持。那么哪一个才是最适合你的呢？让我们一起来看一看他们各自的最新版本都带来了些什么更好的新特性。

![](http://7xp3fo.com1.z0.glb.clouddn.com/choosing-a-front-end-framework-angular-ember-react/17-07-41.png)
## ANGULAR 2.0 (一个激动人心的新版本)
Angular 是当下最流行的前端框架不是没有道理的。它是最早发布的一个革命性的前端MVC框架。Angular 也给大家带来了很多实用的功能。

但是所有这些都被 Angular 2.0 打破了。这是一个小小的败笔。和 Ember 的更新方式不同，第二版的 Angular 几乎完全重构了。这意味着：几乎每一行代码都发生了巨大的变化。这让继续重用1.0系列的代码变得几乎不可能了。所以要想直接平滑升级到 Angular 2.0 是根本不现实的。

然后软件开发界的一大奇迹诞生了。Angular 团队发明了一种 [在一个项目中同时运行 Angular 1.X 和 2.0 代码](http://angularjs.blogspot.com/2015/08/angular-1-and-angular-2-coexistence.html) 的方法。采用这种方法你可以渐近升级。但是在我看来这种方式最关键的作用是解决了 Angular 几乎已成定局的停滞不前问题和成千上万历史遗留代码的维护问题。

既然解决了这个难题，那么时下的大多数 Angular 项目可以继续使用 1.X 版本，并可以在 2.0 正式发布之后逐步升级。如果你并不着急在今年之内发布正式版本并且愿意承担新版本的风险的话，那么直接从新版本的框架开始吧。做好API随时会变的心理准备吧，你的项目越复杂就需要越多的时间来修改你的代码以保证在新版本下正常运行。

### ANGULAR 2.0带来了什么让人期待的新特征？
很多，这个框架正在经历自诞生以来最大规模的重构。

开发2.0的主要目的是消除不必要的复杂。他们删除或者替换掉了大家熟悉的 directives, controllers, modules, scopes 等几乎所有 1.X 时代的概念。取而代之的是一个最大程度使用 ES2015 和 ES2016 新特性并采用了不同的架构设计理念的框架，以期变得易于学习，降低上手难度。

除了让框架变得简单，2.0还有几个值得注意的目标：
* 性能优化
* 支持原生应用开发
* 服务器端渲染

这些新特性对 Angular 来说意味着非常大的改动，并且是1.X版本一直一来所面临的挑战。让我们进一步详细谈谈这三个新特性以及这些改动意味着什么。
#### 性能优化
性能优化是所有使用 Angular 的开发者最期待的新特性之一了吧。如果你使用 Angular 做了足够久的开发，那么你一定会被性能问题所困扰。虽然终究是有办法解决这些性能问题的，但是这个框架的坑实在是太多了。

Angular 的性能是被它的状态查询机制拖慢的。每次 digest 循环，框架都会检查整个 APP 里面的成百上千个变量是否改变。它的新数据模型采用了和React一样的机制：不可变的数据结构配合单向数据绑定。基于这一关键性的改变，Angular 现在只在数据变化时更新一次。从之前的监听数据变成了只快速检查数据对象的索引而不是值。

#### 原生应用支持
使用 Angular 开发原生应用是2.0路线图上的一个重大计划。Angular 开发团队曾和 React 团队碰面并讨论了如何实现这一特性。看起来他们打算借助 React Native 的底层技术实现2.0的原生应用支持。这必将引领一个新的时代，一个 hybrid app 拥有原生应用性能但跨终端共享一套逻辑代码的时代。

#### 服务器端渲染
另一个长期被期待的特性是服务器端渲染的能力。服务器端渲染可以缩短首屏呈现时间并解决客户端动态渲染无法被爬虫抓取从而影响SEO的问题。页面渲染的加快将会明显地提升下一代基于 Angular 开发的 web app 的用户体验。

优点 | 缺点 
------------ | ------------- 
性能提升（比1.X系列快3~5倍）| 没有成型的文档（2.0还没正式发布，很多API都还没定型）
服务器端渲染| 有时候比较难找到相关的开发资源（之前的官网、博客、问答社区都没用了）
原生应用支持| 
框架整合（涵盖了做一个App的方方面面，包括一个增强的router）| 
ES2015 支持（使用了大量的新特性）| 
最流行的框架（很有可能在2.0中保持这种势头） |
易于测试 |
### 谁应该选择 ANGULAR？
Angular 很有可能在相当长的时间里保持前端框架里最流行的地位。所以选择 Angular 开发新项目是一个比较保险的方案。2.0 相比第一版意味着一次翻天覆地的革命。事实上，这种革命就像 Ember 之于 SproutCore一样（有趣的是，Ember 原本应该叫做 SproutCore 2.0）。

Angular 2.0 是用 TypeScript 写的，这是一种源自微软的新语言，相比原生的 JavaScript 而言增加了类型检查和一些其他的增强特性。事实上，[在最近一次开发社区投票调查中](http://angularjs.blogspot.com/2015/09/angular-2-survey-results.html)，得票最多的是 TypeScript 。基于此，加上种种该框架的其他特性表明 Angular 的定位依然是大型企业应用。虽然现在就使用2.0版本还有一定的风险，但是相信2.0的正式版本很快就会发布了。

![](http://7xp3fo.com1.z0.glb.clouddn.com/choosing-a-front-end-framework-angular-ember-react/15-13-36.png)
## EMBER 2.0 (悄悄来到我们身边)
Ember 对自己的定位是做酷炫项目的框架。也确实有挺多酷炫的应用是用 Ember 做的，比如 Apple 的iCloud 网页版本， Discourse（由 Jeff Atwood 开源的一个新型论坛程序），还有 Ghost （新一代的开源博客程序）。Ember是由两位业界大神 Yehuda Katz 和 Tom Dale 开发维护的。虽然不像其他两个著名的框架一样有大型互联网公司在背后撑腰。但是它拥有一个活跃且牛逼的开发者社区。

在1.0的时候，Ember也因为随意改动API引起了很多不满。随后，为了维持大家对开发团队的信任，他们已经学会了如何在几乎不改变用户API的情况下做底层的的大规模更新。他们用这种方法在今年初的时候发布了一个名为 Glimmer 的高性能渲染引擎。在2.0里面他们才移除了不支持这个新引擎的部分代码和API。所以使用 Ember 2.X 开发的应用在性能上必将带来一个质的飞跃。

### EMBER 2.X 带来了什么新特征？
* 支持 ES2015 带来的新特性，比如 modules, classes 和 decorators
* 抛弃了 Mustache 模板引擎并 ~~不再~~ 支持尖括号格式的自定义组件引用
* 使用一种名为 pods 的以功能为单位的新方式组织模块儿，取代了之前以文件用途区分的组织方式，现在一个组件就是一个 pods
* Controllers 将被 routable components 取代
* 利用服务器端渲染缩短首屏加载时间并增强对SEO的支持

优点 | 缺点 
------------ | ------------- 
性能提升（某些条件下比1.X系列快10倍）| 离开了典型应用场景之后就很无力
服务器端渲染 | 相比其他两个更小众
约定大于配置 |
框架整合（功能全面，开箱即用，包括最优秀的路由和数据处理工具） |
一流的文档 |
命令行辅助工具 |
### 谁应该选择 EMBER？
Ember 为开发 web app 带来了一个很棒的方案。就像上面提到的一样，有很多酷炫的应用是使用这个框架开发而成的。它赢得了 Ruby 开发者社区的青睐，包括我们 Smashing Boxes 自己的 Ruby 开发团队。如果你是 Ruby 开发者，Ember将会是很好的选择。有成千上万的文档介绍了如何融合这两周技术进行开发。想知道如何将 Ember Cli 和 Rails 集成到一起？没问题，[这里有一个专题连载告诉你怎么做](http://smashingboxes.com/ideas/merging-rails-and-ember-cli)。

Ember 同时也是那些喜欢一站式开发框架的人的最好选择。我们往往浪费了大量的时间去探索、研究，尝试整合那些并那么适合互相搭配的库。Ember 帮你做了大量的决策，这些决策帮你节省了宝贵的时间。这两种方案各有利弊，然而那些崇尚“够用就好”的人会喜欢Ember的。

![](http://7xp3fo.com1.z0.glb.clouddn.com/choosing-a-front-end-framework-angular-ember-react/16-19-39.png)
## REACT 1.0 (应该和0.14大同小异)
React 是3个当中最轻量级的。事实上，它都不能算是框架。它其实只干一件事：渲染UI组件。甚至有人拿它和前面两个搭配。当然了，更普遍的用法是搭配一种名为 FLux 的架构方案。
Flux 有别于传统的 Model-View-Controller。像 React 生态系统里面的其他部分一样，这仅仅是一个功能单一的库。它负责将视图层的变化传输到数据层。它并不包括其他框架常见的与服务器端通信、数据校验或者注入依赖等。当然了，如果你需要的话，你会找到其他库来解决这些问题的。

Facebook 创造 React 是为了解决他们自己希望在不同页面中保持UI一致性的问题。刚发布的时候就因为它出色的性能和服务器端渲染能力引起了轩然大波。而这两个特征正是其他同类竞争对手一直在努力但尚未实现的。让人欣慰的是 Angular 和 Ember 正在新版本中迎头赶上。

React 所带来的革命远不仅仅如此。最著名的要数 React Native。Facebook 在保留一套跨终端逻辑代码的同时获得了原生应用的性能。上月初，[他们开源了安卓版的 React Native](https://code.facebook.com/posts/1189117404435352/react-native-for-android-how-we-built-the-first-cross-platform-react-native-app/)，给原生应用的开发增加了一种靠谱的选择。

### REACT 1.0 的主要目标是什么?
* 官网改版
* 改善文档
* 增强对动画的处理 

所有的这些都围绕着更好的开发者体验。目前最大的功能缺失是一种轻松地创建动画的方式。既然计划中的改动如此之少，想必1.0很快就将要正式发布了吧。

优点 | 缺点 
------------ | ------------- 
性能| Flux 架构打破了大家的习惯（需要一定的上手时间）
服务器端渲染 | 很多人不喜欢JSX（虽然JSX并不是必须的，但是很常见）
原生应用支持 |
简单 |
库的思路（自由组合） |
ES2015语法支持 |

### 谁应该选择React？
React 无论对新项目还是老项目来说都同样是很好的选择。你可以很容易地把UI层的某部分抽出来用React重构。这对于渐进式地改造老项目来说是个好办法。在 Smashing Boxes ，我们的很多前端工程师都越来越喜欢这个库了。React 和 Flux 的组合也让开发 web app 项目中最复杂的部分变得容易了。

React 在过去的两年里引领了客户端MVC发展的进程。其他的框架都在努力模仿很多React已经实现了的东西。技术社区的喜新厌旧也由此可见一斑。大多数的 React 项目都是用 ES2015 写的，尽管浏览器并未完全支持 ES2015。如果你是最新潮技术的追逐者并且喜欢轻量的库胜过框架的话， React会是你的菜。

## 实例对比
已经有人分别用这几个框架开发了功能和界面都一样的 [TodoMVC app](http://todomvc.com/)，我对此有几点看法。首先，这些框架看起来越来越趋同。尽管他们各自都有自己独特的特性，但是在很多好的方面都比较一致。单向数据绑定就是一个很好例子。同样的，他们三个也都将实现以XML节点为基础的组件。

在这三个框架当中，Ember是上手最快的一个。只要一启动，你马上就拥有了一个具备自动更新功能的本地服务器和相关的最佳实践引导。而对于其他两个来说，你还得花时间自己去配置 WebPack 或 Gulp 来让你的项目跑起来。你需要关心项目的文件结构是如何组织的。或者你需要花时间去找一个初始模板。基于约定大于配置的原则，Ember把这些都帮你做了。

是的，于我而言，在这三个框架中，Ember花了我最长的时间去学习。仅仅只是做这个一个小小的试验项目，有一种杀鸡焉用牛刀的感觉。所以呢，Ember有它比较典型的应用场景，不符合这种应用场景的情况下用起来很别扭。这两点对 Rails来说也是一样的。 Ember 给我的感觉比较适合多人开发且周期较长的大型项目。

相比之下，另外两个框架更符合我的预期。Angular 2.0 给了我一点小小的惊喜。因为和 Angular 1.X 完全不同了，但是当我找到了一些例子之后上手很快。

从最终的代码量来看，Angular app 的代码量最少。React次之。怎么说呢，我感觉在写React的时候思路比较清晰，“是的，我应该把这部分逻辑抽象到它自己的组件里去”。虽然这样增加了代码行数但是对未来的维护来说更轻松。在 Angular 和 Ember 里面很容易就会在模板里面写太多逻辑代码或者是给组件增加很多方法。

最终的生产代码流量大概占100K，在本地测试服务器中加载需要300毫秒。这个 TodoMVC 实在太小了所以体现不出来三者的性能差异。尽管如此，我们来看看 [DBMonster 针对3个框架做的评测](https://www.youtube.com/watch?v=z5e7kWSHWTg&feature=youtu.be&t=2m30s) (在墙外) 。 这个 app 成了 Ember 的 Glimmer 引擎的见证。现在我们可以放心地说三者在压力测试中都性能表现良好了。

## 谁是最后的赢家？

 | Angular 2.0（1.0） | Ember 2.0 | React 0.14 
------------ | ------------- | --- | --- 
Github Stars | 5.9k（43.3k）| 14.9k | 29.7k
Github 贡献者 | 158（1,331）| 536 | 531
StackOverflow 提问 | 127k | 16.9k | 6.1k
StackOverflow 粉丝 | 19k | 2.4k | 2.5k
最早发布年份 | 2009 | 2011 | 2013
框架文件大小 | 566KB | 427KB | 132KB

显而易见：这三个框架为什么这么火主要是因为他们都有各自的强项。正因为如此，我建议你三个一起学，就像我们 Smashing Boxes 一样。没有绝对的赢家。不同的框架适用在不同的场景。即使不考虑其他原因，把这三个框架都学习一下也可以帮你写出更好的代码。

于我本人而言，我真心喜欢 React 及其相关的生态。[它的基础概念很容易上手](http://smashingboxes.com/ideas/learn-react-part-1)。基于较少概念的开发很容易，并且哪怕项目变得复杂了也具有良好的扩展性。我没办法量化这一点，但是它的理念有助于让我写出正确、零bug的代码。如果我现在要开始一个新项目的话，我会选择React。

话虽如此，这三个框架的前途都是光明的。他们的下一代正式版本都将显著提升性能并支持服务器端渲染。Angular 和 React 都将支持iOS和Android平台的原生应用开发。我们可以借助这些框架做很多以前做不到的事了。已经熟悉了这些框架并希望在有趣工作中深入实践？ [点这里加入我们](http://smashingboxes.com/jobs)

翻译自 [http://smashingboxes.com/ideas/choosing-a-front-end-framework-angular-ember-react](http://smashingboxes.com/ideas/choosing-a-front-end-framework-angular-ember-react)