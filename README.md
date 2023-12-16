# CSTNetDown

可备份中科院系统邮箱中信件到本地。

## 安装

Windows 系统中安装 Python 3 之后运行 `install.bat` 即可。

## 研究所邮箱

```python
from cstnetdown import bypop
bypop(account, password, directory)
```
其中 `account` 为研究所邮箱，`password` 可为[客户端专用密码](https://help.cstnet.cn/redianwenti/zhuanyongmima.html)，`directory` 为储存邮件的本地目录。

此方法仅可下载收件箱中的邮件。要下载其他文件夹的邮件，需要手动在邮箱系统中倒腾。

## 国科大邮箱

```python
from cstnetdown.crawl import prepare, start
driver = prepare(directory)
# Allow "Enhanced Safe Browsing / 增强型保护" in Chrome here
# Log in UCAS e-mail service in the browser here
# Open first e-mail in some folder (e.g., Inbox)
start(driver)
```
其中 `directory` 参数意义同前。
