# 感受高效：七行代码的后台代码-Flask

通过简单使用著名的精简型Python Web后台框架Flask，来感受其高效。

## 使用pip安装flask模块

- 管理员打开命令行

![Prompt](../assets/013.png)

- `python -m pip install --upgrade pip` 升级pip版本
- `pip install flask`安装flask模块
  
## 编写程序，保存为 `flask_demo.py`

内容如下：

```python
from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello():
    return "Hello World!"

if __name__ == "__main__":
    app.run()
```

## 在当前目录重开一个命令行

- 按住shift右键点击程序所在目录窗口的空白处，左键`在此处打开powershell窗口`
- 输入`python .\flask_demo.py`开启后台服务（可在输入`python+空格`后，输入`flask+<tab>`自动补全到同样的效果）  
  ![Run Demo](../assets/014.png)

- 在浏览器地址栏输入`127.0.0.1:5000`查看效果，实现完成  
  ![Naviation on Browser](../assets/015.png)

- 可以在后台看到访问记录
  ![Log](../assets/017.png)

---

- 初学者只要之后不久对面向对象有初步了解就可以简单理解这七行代码，不需要知道实现的细节。
- 这也正展现了Python作为面向对象弱类型解释性语言而能简单高效实现功能的魅力。
