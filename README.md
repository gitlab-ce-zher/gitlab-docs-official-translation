# gitlab 中文文档追踪工作组

gitlab 官方文档中文翻译和问题追踪工作组，仅用来处理相关任务分派和跟踪。


Slack 工作组：[**Gitlab-cn Slack Workplace**](https://join.slack.com/t/gitlab-cn/shared_invite/enQtNTY4Njg4NzEyMzQxLTQwMGY5Nzc0MTllOTYzYjNhM2NjYWRmMzFlNGY1YThmN2FlNTY1ODcwZmM2NjcxY2I2ZTRmMDEwODhjMTliMmU)

QQ 群：[**GitLab 文档翻译群**](https://shang.qq.com/wpa/qunwpa?idkey=78d01268ad403b4bd9798369a4130e77c277bfacf904a389ff11ab4d1cb97fb0)

## 工作流程

1. 目前项目的 [Issue](https://github.com/gitlab-ce-zher/gitlab-docs-official-translation/issues) 中包含了尚待翻译的绝大多数文档，要参与的同学可以自行去 Issue 中通过回复 issue 的方式认领，以避免重复工作。整个翻译进度通过 [project](https://github.com/gitlab-ce-zher/gitlab-docs-official-translation/projects/2) 追踪，[查看待领取的 Issue](https://github.com/gitlab-ce-zher/gitlab-docs-official-translation/issues?q=is%3Aissue+is%3Aopen+label%3Apending)。

2. Issue 中支持的自动化指令，这些自动化指令可以自动为 issue 打标签、分配任务和关闭 issue：

   - 在 issue 中回复 `/accept` 可以领取任务
   - 若已向官方提交 PR 再回复 `/pushed`
   - 若被合并再回复 `/merged`

3. Issue 各状态解释

    各状态按流程的顺序排列
   - `weclome`：由流程机器人自动添加的任务，管理员尚未审批，不可被认领。
   - `pending`：待认领任务，表示由该任务已由管理员审批，可被者认领的新增文档任务或者有更新的文档任务，译者输入 `/accept` 接受任务。
   - `Translating`：翻译进行中，任务认领后 Issue 会指派给认领的翻译组成员。
   - `Pushed`：翻译基本完成后，译者已发送 PR 到文档项目。
   - `Finished`：PR 已经完成合并，任务关闭。

4. 待任务被指派给你的后就可以开始翻译了，对于翻译文稿中涉及到的静态文件，直接沿用英文版的文件（例如 `![english image](/docs/conecept.....)`），不再需要自行拷贝。


## 新增了一点自动化指令

所有指令，都在 Issue 中以 Comment 的形式输入，仅对 Member 有效。如果出错或者不符合条件，不会有任何提示。

1. `/accept`: 适用于 `pending` 状态，且当前无人指派的 Issue，输入该指令，会将该 Issue 指派给当前用户。并变更状态为 `translating`
1. `/pushed`: 适用于 `translating` 状态的 Issue，输入该指令，会将该 Issue 指派给当前用户。并变更状态为 `pushed`
1. `/merged`: 适用于 `pushed` 状态的 Issue，输入该指令，会将该 Issue 指派给当前用户。并变更状态为 `finished`，然后关闭 Issue

> 注意：每个用户只能同时有三个处于 `translating` 状态的 Issue，超过上限之后，Bot 不会回应 `/accept` 指令。所以务必确认指派已经完成之后才开始翻译工作。

## 发现文档更新怎么办？
如果发现文档更新，并且根据文档名称在 [Issue 库](https://github.com/gitlab-ce-zher/gitlab-docs-official-translation/issues)中找不到对应的 Issue，可以
[新建 Issue](https://github.com/gitlab-ce-zher/gitlab-docs-official-translation/issues/new)，Issue 标题写入变更的文件名，例如 `/api/settings.md`，并在 Body 中加入 `@loverto, @bubbleatgit`。这样就可以避免在你进行翻译的同时，Bot 重新将该文件放入任务队列。

## 翻译注意事项

在翻译 Gitlab 官方文档前需要注意以下几点：

