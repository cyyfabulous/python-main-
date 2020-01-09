# python-main-
## python 中有main（）的 原因

当py 文件作为模块被导入的时候，此时  __name__  模块名 就变成了其 py的名字（即模块名） ，则 if __name__ == '__main__': 就不会被执行

而当 py 文件 被命令行运行的时候，这个模块的 __name__ 就被 Python 解释器设定为 '__main__' ，

举例：
import this.py
   if __name__ == '__main__':      __name__ 实际为 this
   
python -m this/python that.py
   当作可执行模块
   if __name__ == '__main__':      __name__ 就被 Python 解释器设定为 '__main__'
   
—— 注意，不要写错，python -m that.py 会报错的 —— 有 -m 参数，就不要写文件尾缀 .py：



总结一下：

当 Python 文件被当作模块，被 import 语句导入时，if 判断失败，main() 函数不被执行；
当 Python 文件被 python -m 运行的时候，if 判断成功，main() 函数才被执行。
