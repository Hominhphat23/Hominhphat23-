
ECMAScript
====

## This repo

This repository contains the source for the current draft of ECMA-262,
the ECMAScript® Language Specification.

This source is processed to obtain a human-readable version,
which you can view [here](https://tc39.es/ecma262/).

If you want to explore how the specification was written, you can also view the source with its history in [searchfox](https://searchfox.org/ecma262/source/spec.html).

## Current Proposals

Proposals follow [the TC39 process](https://tc39.es/process-document/) and are tracked in the [proposals repository](https://github.com/tc39/proposals).

* [Finished Proposals](https://github.com/tc39/proposals/blob/HEAD/finished-proposals.md)
* [Active Proposals](https://github.com/tc39/proposals)
* [Stage 1 Proposals](https://github.com/tc39/proposals/blob/HEAD/stage-1-proposals.md)
* [Stage 0 Proposals](https://github.com/tc39/proposals/blob/HEAD/stage-0-proposals.md)
* [Inactive Proposals](https://github.com/tc39/proposals/blob/HEAD/inactive-proposals.md)

### Contributing New Proposals

Please see [Contributing to ECMAScript](/CONTRIBUTING.md) for the most up-to-date information on contributing proposals to this standard.

## Developing the Specification

After cloning, do `npm install` to set up your environment. You can then do `npm run build` to build the spec or `npm run watch` to set up a continuous build. The results will appear in the `out` directory, which you can use `npm run clean` to delete.

## Community

* [ES discourse](https://es.discourse.group/): Forum for ECMAScript discussion and questions
* [Matrix](https://github.com/tc39/how-we-work/blob/HEAD/matrix-guide.md): Chat
## docsify

基于 docsify

https://docsify.js.org/#/zh-cn/cover

## 启动服务

docsify serve ./docs

https://zeroone001.github.io/robotdemo.github.io/#/


## 仓库地址

https://github.com/BerserkerRider/robot.github.io

## gittalk

展示GitHub issues 内容的插件

https://github.com/gitalk/gitalk

### 安装

https://github.com/gitalk/gitalk#install

```js
var gitalkConfig = {
    clientID: "a2bdae5457402030fb6b",
    clientSecret: "c1c9ce6f3334a85f5456b602ca138dee038fd414",
    repo: "robotdemo.github.io",
    owner: "zeroone001",
    admin: ["zeroone001"],
    perPage: 20,
    language: "zh-CN",
    // labels: ['Open'],
    pagerDirection: "last",
    distractionFreeMode: false,
    proxy: 'http://192.168.31.16:8011'
};
const gitalk = new Gitalk({
    clientID: 'GitHub Application Client ID',
    clientSecret: 'GitHub Application Client Secret',
    repo: 'https://github.com/zeroone001/robotdemo.github.io/tree/master',      // The repository of store comments,
    owner: 'zeroone001',
    admin: ['zeroone001'],
    id: location.pathname,      // Ensure uniqueness and length less than 50
    distractionFreeMode: false  // Facebook-like distraction free mode
})

gitalk.render('gitalk-container');
```

## 第三方登录

https://www.ruanyifeng.com/blog/2019/04/github-oauth.html

## 开源
