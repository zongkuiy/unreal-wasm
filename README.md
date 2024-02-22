# ue-wasm

### unreal engine 支持 Cesium 的 wasm 打包功能调研

- 支持 Cesium 的 ue 版本   
  4.26 - 4.27, 5.0 - 5.3

- 支持 html5 打包的 ue 版本
  - 原生支持：4.23及以下   
  已在4.23.2中尝试， 可以成功打包出 wasm 版本运行在 chrome 中
  - 非原生支持
  需要自己编译 ue， 参考   
https://www.bilibili.com/read/cv9954841/   
https://github.com/Xi3Chen/UE4.27PackingH5DDoc?tab=readme-ov-file

> 阶段性结论: 为了同时支持wasm导出和sesium， 需要自行编译一个ue版本

### ue 编译记录
主要参考文档   
https://github.com/UnrealEngineHTML5/Documentation/blob/master/Platforms/HTML5/HowTo/README.md   
https://www.bilibili.com/read/cv9954841/    

1. 获取虚幻引擎源代码访问权限   
   https://www.unrealengine.com/zh-CN/ue-on-github
   https://docs.unrealengine.com/5.3/zh-CN/downloading-unreal-engine-source-code/

> 注意：官方库目前只有两个4.24的html版本, 暂时用下面的版本进行构建   
https://github.com/SpeculativeCoder/UnrealEngine-HTML5-ES3

2. 下载ue代码   
   编译需要的磁盘空间较大，一定放在余量超过150G的磁盘分区   
```bash
  git clone -b 4.27-html5-es3 --single-branch https://github.com/SpeculativeCoder/UnrealEngine.git ue-4.27-html5-es3
```
