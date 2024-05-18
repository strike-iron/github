# GitHub Actions

> 从 2024 年 6 月 30 日起，所有 GitHub Pages 版本都将使用 GitHub Actions。
> 无需进行其他更改，但必须在存储库中启用 GitHub Actions 才能继续构建。 有关 GitHub
> Actions 运行器的详细信息，请参阅“管理存储库的 GitHub Actions 设置”
>
{style="note"}

GitHub Actions 是一个 CI/CD 平台, 可以用于自动化构建、测试和部署管道, 从而自动化执行工作流
workflow.

GitHub Actions 的工作流文件存储在 `.github/workflows/` 目录中, 每一个工作流文件都可以任意命名,
并使用 `yaml` 标记语言编写.

GitHub Actions 由工作流 workflows 构成, 一个工作流在仓库响应事件时触发.

工作流由作业 jobs 构成, 一个工作流可以包含一个或多个可按顺序或并发运行的作业.

作业由步骤 steps 构成, 一个作业的运行环境可以是虚拟机, 也可以是容器.

步骤由脚本或操作 actions 构成.

## 工作流 workflows

工作流是在 `.github/workflows` 中定义的 yaml 文件. 一个仓库可以拥有多个工作流,
每个工作流可以执行不同的作业集.
工作流之间可以进行互相引用.

## 事件 events

事件是仓库用于触发工作流的活动.

## 作业 jobs

作业是工作流在运行环境上执行的一组步骤集, 步骤按顺序执行, 并且相互依赖.
由于步骤都在同一运行环境上, 所以可以将数据从一个步骤共享到另一个步骤.

默认情况下, 作业间没有依赖关系, 并发运行. 但我们可以设置一个作业依赖另一个作业,
从而顺序执行有依赖关系的作业.

## 操作 actions

操作通常用于执行复杂且可以复用的作业.

## 运行环境 runners

GitHub 提供了 Ubuntu Linux, Microsoft Windows 和 macOS 三种运行环境来执行我们的工作.
并且我们也可以托管自己的运行环境.

<seealso>
    <category ref="reference">
        <a href="https://docs.github.com/zh/actions/quickstart">GitHub Actions 快速入门</a>
    </category>
</seealso>
