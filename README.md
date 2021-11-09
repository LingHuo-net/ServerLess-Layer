# ServerLess-Layer

- DotNet60
  - .net 6.0 runtime 
- DotNet50
  - .net 5.0 (v5.0.11)
- DotNet31
  - .net core 3.1


## How to use ServerLess-Layer

### 腾讯云
请从Release中下载对应的版本
上传至云函数中“层”

使用 CustomRuntime
云函数中使用该Layer

bootstrap 文件 
``` sh
#!/bin/sh
echo "Start dotnet bootstrap ~~~"
export DOTNET_ROOT=/opt/runtime
export PATH=$(pwd):/opt/runtime:${PATH}
dotnet ./bin/YourDllFile.dll
```
