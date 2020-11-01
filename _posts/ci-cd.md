---
date: '2020-01-10'
slug: vuepress-introduction_
tags:
- JAMstack
- VuePress
title: 結合 CI/CD 才是完整的 JAMstack
description: 結合 CI/CD 才是完整的 JAMstack
author: SidStraw
image: https://i.imgur.com/u7De015.png
meta:
  - name: author
    content: SidStraw
  - http-equiv: content-language
    content: zh-TW
featured: true
---

## 何謂 CI/CD

> CI/CD stands for Continuous Integration (CI) and Continuous Deployment or Continuous Delivery (CD).
CI/CD 通常指的是持續集成和持續交付或持續部署的組合實踐。

光看這段引用是不是有點黑人問號呢？

其實簡單來說，就是將程式發布的流程自動化，自動編譯、測試、部署......等等，把重複性操作轉為自動化執行。

如果對 CI/CD 這個議題有興趣，而且也想知道它為什麼這麼重要，我推薦可以去看一本小說，叫做：「鳳凰專案：看IT部門如何讓公司從谷底翻身的傳奇故事」 

~~看完本書就知道什麼是 CI/CD 了，今天就介紹到這邊，我們明天見~~

這本小說非常好看易讀，但書中的案例卻都是在真實環境中很常見的各種災難，閱讀此書不會讓你馬上就知道如何建構屬於你的 CI/CD 模式，但可以讓你知道 CI/CD 的重要性與大致上的概念。

---

## CI - Continuous integration 持續整合

上面提到的自動編譯、測試、部署，其中自動編譯與測試的部分就是包含在 CI 階段進行的，通常會提供一個統一、一次性的編譯與測試環境，透過預先設定好的容器與預先寫好的腳本來達成 CI。

我想 CI 最大的幫助之一，就是將人工操作的比例盡可能的降低，畢竟人工操作不但累人，還要在可靠性上面打一個大大的問號。

而統一環境這一點也是非常重要的環節，因為透過統一的編譯與測試環境，才能有效避免不同開發者之間因為環境的落差而造成不可預期的 BUG。

---

## CD - Continuous Deployment 持續佈署

而 CD 的概念就相對單純一些了，在每次 CI 完成編譯、測試的流程後自動將最新的程式版本部署到伺服器上提供服務，這就是 CD 的概念。

而 CD 的架構通常也包含了服務可靠性的確保，在部署失敗或是服務異常等等的狀況發生時，系統會利用各種方式來通知維運人員進行處理，維運人員也可以在最短的時間內採取必要的行動，像是遇到重大 BUG 時可以快速回退到之前的穩定版本，避免損害擴大。

---

## GitHub Actions

其實本來是要跟你聊聊 GitHub 提供的自動化工具： GitHub Actions 的，不過想想，要聊 GitHub Actions 之前可能要先談談什麼是 `CI / CD` 才行，不然你可能會難以理解 GitHub Actions 的好用之處。

所以 GitHub Actions 就留到明天再來說明吧！