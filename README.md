Hominhphat23
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

Version
20.17.0

Platform
Darwin x.home 24.0.0 Darwin Kernel Version 24.0.0: Mon Aug 12 20:52:18 PDT 2024; root:xnu-11215.1.10~2/RELEASE_ARM64_T8122 arm64
Subsystem
Buffer/Blob

What steps will reproduce the bug?
new Blob(['aaaaaaaa']).slice(0, 1.5)
How often does it reproduce? Is there a required condition?
Always, no special requirements needed.

What is the expected behavior? Why is that the expected behavior?
I would not expect Node to crash with a native error, as this is not possible/easy to catch.

What do you see instead?
$ node -e "new Blob(['aaaaaaaa']).slice(0, 1.5)"

  #  node[76610]: static void node::Blob::ToSlice(const FunctionCallbackInfo<v8::Value> &) at ../src/node_blob.cc:248
  #  Assertion failed: args[1]->IsUint32()

----- Native stack trace -----

 1: 0x1043430d4 node::Assert(node::AssertionInfo const&) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
 2: 0x10584e098 node::Blob::ToSlice(v8::FunctionCallbackInfo<v8::Value> const&) (.cold.1) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
 3: 0x104314e08 node::Blob::HasInstance(node::Environment*, v8::Local<v8::Value>) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
 4: 0x104539bc8 v8::internal::MaybeHandle<v8::internal::Object> v8::internal::(anonymous namespace)::HandleApiCallHelper<false>(v8::internal::Isolate*, v8::internal::Handle<v8::internal::HeapObject>, v8::internal::Handle<v8::internal::FunctionTemplateInfo>, v8::internal::Handle<v8::internal::Object>, unsigned long*, int) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
 5: 0x1045392c0 v8::internal::Builtin_HandleApiCall(int, unsigned long*, v8::internal::Isolate*) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
 6: 0x104dc0b24 Builtins_CEntry_Return1_ArgvOnStack_BuiltinExit [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
 7: 0x104d383e4 Builtins_InterpreterEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
 8: 0x104d383e4 Builtins_InterpreterEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
 9: 0x104d3650c Builtins_JSEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
10: 0x104d361f4 Builtins_JSEntry [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
11: 0x10460dbc8 v8::internal::(anonymous namespace)::Invoke(v8::internal::Isolate*, v8::internal::(anonymous namespace)::InvokeParams const&) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
12: 0x10460dda0 v8::internal::Execution::CallScript(v8::internal::Isolate*, v8::internal::Handle<v8::internal::JSFunction>, v8::internal::Handle<v8::internal::Object>, v8::internal::Handle<v8::internal::Object>) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
13: 0x1044d3bb0 v8::Script::Run(v8::Local<v8::Context>, v8::Local<v8::Data>) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
14: 0x1043364f4 node::contextify::ContextifyScript::EvalMachine(v8::Local<v8::Context>, node::Environment*, long long, bool, bool, bool, v8::MicrotaskQueue*, v8::FunctionCallbackInfo<v8::Value> const&) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
15: 0x104335e08 node::contextify::ContextifyScript::RunInContext(v8::FunctionCallbackInfo<v8::Value> const&) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
16: 0x104539bc8 v8::internal::MaybeHandle<v8::internal::Object> v8::internal::(anonymous namespace)::HandleApiCallHelper<false>(v8::internal::Isolate*, v8::internal::Handle<v8::internal::HeapObject>, v8::internal::Handle<v8::internal::FunctionTemplateInfo>, v8::internal::Handle<v8::internal::Object>, unsigned long*, int) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
17: 0x1045392c0 v8::internal::Builtin_HandleApiCall(int, unsigned long*, v8::internal::Isolate*) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
18: 0x104dc0b24 Builtins_CEntry_Return1_ArgvOnStack_BuiltinExit [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
19: 0x104d383e4 Builtins_InterpreterEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
20: 0x104d383e4 Builtins_InterpreterEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
21: 0x104d383e4 Builtins_InterpreterEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
22: 0x104d383e4 Builtins_InterpreterEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
23: 0x104d383e4 Builtins_InterpreterEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
24: 0x104d383e4 Builtins_InterpreterEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
25: 0x104d3650c Builtins_JSEntryTrampoline [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
26: 0x104d361f4 Builtins_JSEntry [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
27: 0x10460dbc8 v8::internal::(anonymous namespace)::Invoke(v8::internal::Isolate*, v8::internal::(anonymous namespace)::InvokeParams const&) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
28: 0x10460d014 v8::internal::Execution::Call(v8::internal::Isolate*, v8::internal::Handle<v8::internal::Object>, v8::internal::Handle<v8::internal::Object>, int, v8::internal::Handle<v8::internal::Object>*) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
29: 0x1044e7904 v8::Function::Call(v8::Local<v8::Context>, v8::Local<v8::Value>, int, v8::Local<v8::Value>*) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
30: 0x1043243e4 node::builtins::BuiltinLoader::CompileAndCall(v8::Local<v8::Context>, char const*, node::Realm*) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
31: 0x1043b414c node::Realm::ExecuteBootstrapper(char const*) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
32: 0x104307bb4 node::StartExecution(node::Environment*, std::__1::function<v8::MaybeLocal<v8::Value> (node::StartExecutionCallbackInfo const&)>) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
33: 0x1042713a4 node::LoadEnvironment(node::Environment*, std::__1::function<v8::MaybeLocal<v8::Value> (node::StartExecutionCallbackInfo const&)>, std::__1::function<void (node::Environment*, v8::Local<v8::Value>, v8::Local<v8::Value>)>) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
34: 0x104383394 node::NodeMainInstance::Run(node::ExitCode*, node::Environment*) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
35: 0x104383104 node::NodeMainInstance::Run() [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
36: 0x10430afa0 node::Start(int, char**) [/Users/neo/.nvm/versions/node/v20.17.0/bin/node]
37: 0x183130274 start [/usr/lib/dyld]

----- JavaScript stack trace -----

1: slice (node:internal/blob:265:21)
2: [eval]:1:24
3: runScriptInThisContext (node:internal/vm:209:10)
4: node:internal/process/execution:118:14
5: [eval]-wrapper:6:24
6: runScript (node:internal/process/execution:101:62)
7: evalScript (node:internal/process/execution:133:3)
8: node:internal/main/eval_string:51:3