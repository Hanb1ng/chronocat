### 如果你来自 [go-cqhttp#2471](https://github.com/Mrs4s/go-cqhttp/issues/2471) 并打算迁移，那么请先看完：

# 方案一：使用 [Shamrock](https://github.com/linxinrao/Shamrock)

Shamrock 是一个基于 Xposed 实现的 Onebot11/12 标准 QQBot 框架。

特点：

- 无缝迁移：Shamrock 会直接支持 OneBot API 和 go-cqhttp 的扩展 API，迁移成本是最低的

![image](https://github.com/chrononeko/bugtracker/assets/20179549/7dd24be9-aa7f-4a3e-9066-2619019860fa)

- 可在多平台部署：安卓手机可直接部署，Windows 和 Linux 均可安装模拟器进行部署。Docker 环境可使用 Docker 内 Android 部署。
- 更新积极：Shamrock 的维护状态非常良好，基本有问题就会立即处理

---

需要注意：Shamrock 的维护者不建议立刻进行迁移，并且 **不推荐迁移到闭源框架**。

![image](https://github.com/chrononeko/bugtracker/assets/20179549/22bc1b63-d563-48b6-bbab-c12422a8cc23)

# 方案二：等待 [Lagrange](https://github.com/Linwenxuan05/Lagrange.Core) 完善

Lagrange 是 QQNT 的协议实现。

根据目前的消息：

- Lagrange 即将迁移 Go 语言，不用担心 C# 内存消耗的问题
- 现在 QQNT 的 sign 已经差不多了，“一切交给时间”，大家可以不要着急，先等待一段时间。

![image](https://github.com/chrononeko/bugtracker/assets/20179549/258e46ff-ee09-4fc2-aa0d-c2503f6f755e)

---

### 有关 Chronocat

Chronocat 的文档仍在完善。如果文档有缺，可以加讨论群（[811724851，点击即可加群](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=xX4FW_xMucouwJ8ZhaJ49nQSFEmBNmO1&authKey=4zuRY8%2BK6rpGD9yHwZU1CODaI8IndZWwkJyK8KITbAzjJEq23%2BIFwxD0PS7gm%2FB%2F&noverify=0&group_code=811724851)），我会优先编写大家需要的内容。此外：

- 如果你的 go-cqhttp 已经完全无法使用，希望立即迁移且不想重构代码，我推荐使用上面的 Shamrock。
- 如果你希望等待协议实现，我推荐等待上面的 Lagrange。
- **Chronocat 同样不建议在你的 bot 仍然可用的情况下就开始迁移**。可以继续保持现有方案，然后再慢慢开始考虑迁移计划。

# 最后再次强调：不推荐迁移到闭源框架。

理由应该无需说明。
