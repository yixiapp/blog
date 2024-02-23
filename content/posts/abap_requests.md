+++
title = '修改请求状态'
date = 2024-02-22T14:34:19+08:00
tags = ["传输请求"]
categories = ["abap"]
draft = true
+++

有时我们会希望挽回释放的请求，有时我们想改变请求的层级。

在ECC中，用SE38执行 RDDIT076 程序，可以修改请求的状态，但在HANA版本中好像不行。

这时可以直接修改表 E070，把R改成D。
![20240222172916](http://qiniu.yixiapp.com/image/sap/2024/20240222172916.png)
如图，上层的请求在 STRKORR 里面，可以改变请求的从属关系。

请求锁定对象的表是 TCLOK，可删除数据解锁。
![20240222171725-2024-02-22](http://qiniu.yixiapp.com/image/sap/2024/20240222171725-2024-02-22.png)

此外，EO71表记录了请求包含的对象。