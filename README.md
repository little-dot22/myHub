# myHub

1. 编写api文件夹下的openapi.yaml文件。

2. 使用openapi-generator生成idl文件夹，其中包含.proto文件，具体方法如下：

    - 安装docker desktop以在windows下使用docker.
    - 打开docker desktop应用，会自动开启docker引擎，配置docker的镜像站点

          "registry-mirrors": [
            "https://79c44ubb.mirror.aliyuncs.com"
          ]
    - vscode终端输入以下代码：

          docker run --rm -v "${PWD}:/local" openapitools/openapi-generator-cli generate -i /local/api/openapi.yaml -g protobuf-schema -o /local/idl
    - 此时应该创建好了idl文件夹，其中包括models，services文件夹，里面有.proto文件。
    
3. 