## webcomponents中文文档  翻译自MDN


#### Web Components 是什么  

Web Components是一个浏览器的新功能，提供了一个面向web包括下面几个方面标准的组件模型。    

你可以认为Web Components是一个可复用的用户接口部件，  
属于浏览器的一部分，所以不需要一些额外的例如jQuery或者Dojo之类的工具库。  
一个存在的Web Components的使用完全不需要写代码，  
仅仅需要在HTML中加一个import 语句就可以了。   
Web Components使用了一些新颖并且在开发中的浏览器功能。  

The description above works fairly well at this moment in time, but it leaves out many other things that Web Components could be created for. With a Web Component, you can do almost anything that can be done with HTML, CSS and JavaScript, and it can be a portable component that can be re-used easily.

Sometimes there is some confusion regarding Web Components and Google Polymer. Polymer is a framework that is based on Web Components technologies. You can make and use Web Components without Polymer.

上面提到的部分当前在浏览器中可以正常的运行，但是有好多Web Components可以用来创造的部分没有被提及。  
使用Web Components 你几乎可以来做任何可以使用HTML,CSS,JS能做到的事情，并且可以更便捷的被复用。  

有时候关于Web Components和谷歌的plymer之间可能会存在一些困惑   
简介而论，Polymer是基于Web Components技术的一个框架，你当然可以在不适用其的情况下开发Web Components    

Web Components are not fully implemented in all browsers yet, and so to use them right now in most browsers (January 2015) you will probably need to use polyfills to fill in the gaps in browser coverage. Polyfills are available in the Google Polymer project. To find out which browsers implement Web Components, see Are We Componentized Yet?   

Web Components并没有被所有浏览器来实现(截止2017年chrome已经完全支持，其他浏览器还在投票表决中),因此如果在不支持的浏览器上使用Web Components， 
应该使用由google polymer开发的 polyfills来达到目的。使用之前最好通过[Are We Componentized Yet](http://jonrimmer.github.io/are-we-componentized-yet/)查看浏览器兼容性。  


Web Components consists of these four technologies (although each can be used separately):
Web Components 包括以下四种技术(每种都可以被单独使用)  

*  Custom Elements   
*  HTML Templates  
*  Shadow DOM  
*  HTML Imports  

明确的文档定义如下：   

*   一种新的html元素: <template>    
*   关于<template> 的接口： HTMLTemplateElement, HTMLContentElement (removed from spec) and HTMLShadowElement   
*   HTMLLinkElement接口和 <link> 元素的扩展  
*   注册custom elements的接口：Document.registerElement()和对Document.createElement() and Document.createElementNS()的更新    
*   对html元素原型对象新增的生命周期回调   
*   默认为元素对象增加的新的css的伪类：:unresolved   
*   The Shadow DOM：ShadowRoot and Element.createShadowRoot(), Element.getDestinationInsertionPoints(), Element.shadowRoot   
*   Event接口的扩展、Event.path  
*   Document 接口的一些扩展  
*   Web Components样式应用新的伪类：:host, :host(), :host-context()
 


#### Shadow DOM
===========