# MosDNS GeoData Rules Auto-Builder

本项目利用 GitHub Actions 每日自动从上游拉取 `.dat` 规则库，并解析转化为 MosDNS 原生支持的纯文本 (`.txt`) 格式。

* **使用的转换工具:** [urlesistiana/v2dat](https://github.com/urlesistiana/v2dat)
* **引用的上游规则库:** [MetaCubeX/meta-rules-dat](https://github.com/MetaCubeX/meta-rules-dat)

---

## **rule-set**

mosdns：[meta branch](https://github.com/0xTimi2233/geodat-format-mosdns/tree/meta)

---

## 🛠️ 如何 Fork 并自定义你自己的规则？

如果你需要增加、减少或修改导出的规则列表，可以 Fork 本仓库并按照以下步骤操作：

### 1. Fork 本项目
点击页面右上角的 `Fork` 按钮，将此项目复制到你自己的 GitHub 账号下。

### 2. 开启 Actions 写入权限 (关键步骤)
由于工作流需要将生成的规则推送到 `meta` 分支，你需要开启 Git 机器人的写入权限：
1. 进入你 Fork 后的仓库，点击顶部的 **Settings**
2. 在左侧菜单找到 **Actions** -> **General**
3. 滚动到页面最底部的 **Workflow permissions**
4. 选择 **Read and write permissions** 并点击 `Save` 保存。

### 3. 修改规则列表
在主分支 (`main`) 中打开 **`rules.txt`** 文件。
你可以按照 `类型-标签` 的格式单行添加你需要的规则。例如：
```text
geosite-cn
geosite-apple
geoip-cn
```

### 4. 获取生成的规则文件

编译好的 `.txt` 纯文本规则文件存放在独立的 `meta` 分支中

---
