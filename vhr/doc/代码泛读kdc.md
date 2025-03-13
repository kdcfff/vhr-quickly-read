## 这是关于kdc的代码泛读
### 项目用例图
![img.png](img.png)
### 从`ChatContorller`看项目整体架构
> 项目是一个典型的mvc架构，`HrContorller`作为控制器，`HrService`作为业务层，`HrMapper`作为数据层，`Hr`作为模型层，`HrContorller`调用`HrService`，`HrService`调用`HrMapper`，`HrMapper`调用数据库。
- 我们从getAllHrs获取所有hr的个人信息
![img_1.png](img_1.png)
- getAllHr调用HrService
![img_2.png](img_2.png)
- HrService调用HrMapper
![img_3.png](img_3.png)
### 从项目包图看项目架构
![img_4.png](img_4.png)
- 项目在mvc架构下完成crud操作
![img_5.png](img_5.png)
- 通过aop切面编程将核心逻辑进行解耦