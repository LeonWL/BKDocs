# 创建用户组

蓝鲸权限中心推荐通过用户组的方式来管理权限，可以关联权限模板来给一个用户组授权，然后通过将用户或组织加入用户组，这些用户或组织就自动拥有了该用户组的权限。 

## 前置条件

> 1. 登录用户是 admin
>
> 2. 创建好权限模板

## 操作步骤

1. 点击`用户组`菜单，进入用户组列表页。

   ![image-20200921103738104](CreateGroups/image-20200921103738104.png)

2. 点击`新建`按钮创建新用户组。

   - 用户组名：`必填`，全局唯一，用户组名必须大于 4 个字符。
   - 描述：`必填`，将用户组的功能描述清楚，便于管理员或者用户申请时辨识。
   - 添加组成员：`非必填`，组成员包括用户和组织，表示给对应的成员分配该组的权限。
   - 添加组权限：`非必填`，组权限添加已经创建好的权限模板，表示将权限赋予该组。

   ![image-20200921103903534](CreateGroups/image-20200921103903534.png)

