# NCD 豁免思想实验模拟器

这是一个可离线运行的静态模拟器，用于展示一个简化的 NCD waiver（无赔款优待豁免）思想实验。它的目标是支持透明沟通、参数敏感性分析与机制讨论，而不是复现任何正式规则、未公开方法或生产定价引擎。

## 在线演示

- 根入口：[https://xiang-shan.github.io/-NCD-/](https://xiang-shan.github.io/-NCD-/)
- 兼容入口：[https://xiang-shan.github.io/-NCD-/simulation.html](https://xiang-shan.github.io/-NCD-/simulation.html)

## 仓库内容

- [index.html](./index.html)：默认入口，适用于本地打开和 GitHub Pages
- [simulation.html](./simulation.html)：兼容入口，会跳转到主页面
- [math_model.md](./math_model.md)：建模假设、公式与口径说明
- [vendor-mathjax](./vendor-mathjax)：本地 MathJax 运行时，用于公式渲染
- [vendor-katex](./vendor-katex)：本地 KaTeX CSS 与字体资源

## 本地使用

直接在浏览器中打开 [index.html](./index.html) 即可。页面完全静态，不依赖后端服务，也不需要额外安装包。

## 模型范围

当前版本采用一组刻意简化的分析口径：

- 按地区切换 NCD 下界：
  - 北京厦门：11 档，最低等级为 `-5`
  - 非北京厦门：10 档，最低等级为 `-4`
- 用年度 Markov transition（马尔可夫转移）表示等级迁移
- 用 Poisson（泊松）分布表示年度责任赔次
- 把自动驾驶豁免上限写成场景参数，可在 `0/1/2/3/4` 之间切换
- 用截断二项分布建模“实际享受豁免次数”，自动满足“实际豁免次数不超过真实出险次数”

## 使用边界

这个仓库应被理解为一个透明分析框架，而不是政策解读。页面中的地区选择、豁免上限、参数、矩阵和指标都用于帮助讨论 trade-off（权衡），不应被解读为任何已定监管细则、官方算法或正式市场规则。
