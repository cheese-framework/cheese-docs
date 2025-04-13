---
outline: deep
---

# 项目信息

## 项目结构
```
.
├─ node_modules ---npm包存放位置，会打包到最终脚本app。
├─ dev ---开发依赖存放位置，用于开发时进行代码混淆或其他自动化操作以便快速开发，不会打包到最终脚本App。
├─ src
│  └─ main
│      └─ assets --静态资源存放位置，如找图的小图、插件、模型等。
│      └─ js/ts --脚本文件存放位置。
│      └─ ui --ui存放位置。
│      └─ icon.png  --app打包的图标，替换您自己的图标即可。
├─ cheese.toml --项目的配置文件。
├─ jsconfig.json/tsconfig.json --js/ts的配置文件，不需要动。
└─ package.json --当前包的配置文件，不需要动。

```

## 项目配置文件
```toml
#项目的配置结构可能会随版本更新发生变化。为了确保配置文件正确，建议您定期访问(https://cheese.codeocean.net/other/project-information.html)获取最新的配置信息。
# 语言绑定
bindings= "js-node"
# bindings= "js"
# bindings= "ts-node"
# bindings= "ts"
# ui类型
ui = "xml"
# 入口文件
main = "main"

[app]# 信息配置
# app版本号
version = "0.0.1"
# app包名
package = "cheese.demo"
# app名
name = "Demo"
# 无障碍服务名称
accessible_service_name = "cheese"
# 无障碍服务描述
accessible_service_desc = "cheese"
# 输入法名称
inputmethod_service_name = "cheese"
# 权限清单
permissions = [
"android.permission.SYSTEM_ALERT_WINDOW",
]

[build]# 构建配置
# android_sdk_build-tools版本
build-tools = { version = "34.0.0" }
# 热更新 - 默认关闭
# hot = { version = "0.0.1" , url = "http://127.0.0.1:7777/update"}
# 代码保护 推荐打包后的app再次使用如360、腾讯等第三方加固 - 默认关闭 模式：1.obfuscator 将js脚本混淆 2.cloak：汇编级别保护，将js脚本直接编译为机器码并进一步机密不可还原
# protection = "obfuscator"
# 架构支持 更改此项编译解包需要打开 - 默认关闭
# ndk = ["x86_64", "arm64-v8a"]
# 排除内置库 更改此项编译解包需要打开 - 默认关闭
# excludeLib = ["yolo", "opencv", "paddleocr", "onnx", "ddddocr", "mlkitocr"]
```
