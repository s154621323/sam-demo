# SAM Demo - AWS Serverless Application Model

这是一个使用AWS SAM (Serverless Application Model) 构建的无服务器应用程序示例项目。

## 项目结构

- `hello-world/` - 应用程序的Lambda函数代码，使用TypeScript编写
- `events/` - 用于测试函数的事件文件
- `template.yaml` - 定义应用程序AWS资源的SAM模板
- `samconfig.toml` - SAM CLI配置文件

## 功能特性

- 基于Node.js 18.x的Lambda函数
- API Gateway集成，提供REST API端点
- 使用esbuild进行TypeScript编译和打包
- 支持本地测试和部署

## 快速开始

### 前置要求

- [SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)
- [Node.js 18](https://nodejs.org/en/)
- [Docker](https://hub.docker.com/search/?type=edition&offering=community)

### 构建和部署

```bash
# 构建应用程序
sam build

# 部署到AWS（首次部署使用引导模式）
sam deploy --guided
```

### 本地测试

```bash
# 本地启动API
sam local start-api

# 测试单个函数
sam local invoke HelloWorldFunction --event events/event.json
```

## API端点

- **GET /hello** - Hello World Lambda函数端点

## 部署配置

项目配置为部署到 `ap-southeast-2` 区域，使用 `hello-world` 作为堆栈名称。

## 许可证

ISC