## APEE 刷题工具

> 支持组卷考试的刷题工具

### 功能规划

- 支持用户注册登录
- 支持题目收藏、错题本
- 支持管理员题库导入
- 支持组卷考试
- 支持顺序刷题、随机刷题，题源可选择某类或者全部

### 题库数据转为JSON流程

1. 使用 Excel 打开题库 `xls` 文件
2. 删除 `表头` 和 `I列` 之后的所有列
3. 清空第 `1` 列数据，批量填充为` ##oyp##`
4. 鼠标选中所有列，按 `Ctrl + C` 复制内容
5. 新建 `text.txt`，将内容粘贴到其中
6. 运行 `1_转为JSON.py` 程序
7. 运行 `2_存入数据库.py` 程序