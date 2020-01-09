# python-main-
## python 中有main（）的 原因

当py 文件作为模块被导入的时候，此时  __name__  模块名 就变成了其 py的名字（即模块名） ，则 if __name__ == '__main__': 就不会被执行
而当 py 文件 被命令行运行的时候，这个模块的 __name__ 就被 Python 解释器设定为 '__main__' ，

即 
