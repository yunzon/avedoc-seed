# avedoc-seed
 The repository for representing Ave Docs

[![Build Status](https://dev.azure.com/swzhang/seanpipeline/_apis/build/status/yunzon.avedoc-seed?branchName=master)](https://dev.azure.com/swzhang/seanpipeline/_build/latest?definitionId=2&branchName=master)

# Before you start

## DocFx

一个可以将源代码以及 Markdown 文件生成一个静态的 HTML 网站的工具。


## Azure pipeline
**Azure pipeline** 是Azure DevOps中的一个Service，提供了一套build和release的服务，跟Jenkins 一样，是一套CI/CD 工具。

Azure pipeline的优势：

1.	入门容易，界面友好，操作简单，配置灵活，不需要额外插件支持主流代码托管平台
2.	开源仓库提供免费服务，私有仓库每月提供1800分钟免费额度
3.	高度集成 Microsoft  Azure  的其他服务，这个Demo就利用了Azure Storage 托管static site


# Quick start



## Prepare: 

1. Docfx 文档工程： https://github.com/yunzon/avedoc-seed
2. Azure DevOps 环境   https://dev.azure.com/
3. 一份owner权限的 Azure subscription ( 如果使用Azure Storage host static web site)


## Get start：

1.	创建Azure pipeline project
2.	根据步骤，授权Azure pipeline app 权限 给  Git repository，
3.	 Design pipeline task
4.	 Pipeline app会自动将步骤3中的task以YAML格式存储在授权的Git Repo中
5.	 执行pipeline

Pipeline task中集成了各种功能，可以根据实际需要组合出各种需求，本项目中定义的task:

1.	安装windows 2019
2.	安装Powershell，安装docFx
3.	Download repo 到本地
4.	调用docFx build repo
5.	Copy build结果到sites目录
6.	Copy sites 目录到Azure Storage

Github repository 的master 分支有任何改动，将会自动触发Azure pipeline rebuild repo。
