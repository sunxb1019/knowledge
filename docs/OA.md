# OA文档

## 企业微信工资单发送

![1563436873729](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1563436873729.png)

正常登陆OA系统，点击**“人事”**、**“工资发布”**，跳转至工资单发布系统界面

![1563437357285](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1563437357285.png)

![1563437441298](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1563437441298.png)

根据上图填写主要信息，并上传工资明细Excel（发送模板点击最下方蓝色字体下载）

![1563437641362](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1563437641362.png)

模板填写无特殊要求，保证第一列为正确的员工编号即可，发送后可在发送记录页面查看发送是否成功

---

## 文档上传（前端）

![1564620557051](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1564620557051.png)

进入门户首页，依次点击【知识】-【新建文档】右侧显示有权限新建文档的文档目录，点击文档目录可以进入该文件夹，或直接在左侧目录树中查找。

![1564621567269](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1564621567269.png)

点击到最底层文件夹，显示加号，即可新建文档。

![1564621716041](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1564621716041.png)

1. 文档目录：要求必填，为前台显示名称
2. 工具栏：与常用的办公软件基本相同，鼠标悬停显示中文解释
3. 正文内容编辑区：该区域书写正文内容
4. 底部标签页：打开文档是默认显示正文内容页；文档属性自动生成无需维护内容保持默认即可；文档附件页用于挂接文档附件

![1564622010972](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1564622010972.png)

点击右上角绿色加号按钮，选择本地文件作为附件上传

![1564622145554](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1564622145554.png)

勾选已上传文件，点击右上角红色减号按钮点击确定删除附件

![1564622276276](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1564622276276.png)

所有内容编辑完成以后点击【提交】按钮，设置文档可见范围。默认可见范围根据文件夹权限已提前设置，如需更改需相应文件夹维护权限。同样点击右上角加号与减号按钮增加删除共享人员。

## 文档目录维护（后端）

![1564625233920](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1564625233920.png)

1. 点击【维护权限】后添加此目录的维护权限，拥有维护权限的用户是不需要系统权限就可以管理指定的这个目录的；

2. 点击【创建权限】后进入文档创建权限的列表页面，点击【添加】后显示如图，添加文档创建权限，设置哪些人可以创建文档，添加人员页面如图18所示；

   ![1564625320162](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1564625320162.png)

   - 部门+安全级别：选择部门并设定安全级别，只有被选中的部门且此部门中大于设定的安全级别的人员才能在此目录中添加文档；
   - 分部+安全级别：选择分部并设定安全级别，只有被选中分部中大于设定安全级别的人员才能在此目录新建文档；
   - 角色+安全级别+级别：选择角色，并且人员在角色中的级别需低于这里的级别，再看人员的安全级别是否大于设定的安全级别，如果大于就可以新建文档；
   - 安全级别：只要大于安全级别的用户都可以新建文档；
   - 用户类型：用户类型中主要分为两种，一个是内部员工，一个是客户，只是客户类型又分了很多种类，如图19所示，内部员工就是雇员，其它的都是客户，所以一般我们只要选择雇员即可。
   - 人力资源：选择某个具体的用户做为此目录的创建者。

3. 点击【复制权限】后添加的用户可以将此目录下的文档复制到另一个目录中去，前提是另一个目录也要有复制权限；

4. 点击【移动权限】后添加的用户可以将此目录下的文档移动到另一个目录中去，前提是另一个目录也要有移动权限；

5. 点击默认共享后可以设置目录下文档的共享范围，选择相应的对象，点击下方加号按钮增加，删除操作与附件删除操作相同。

   ![1564627078376](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1564627078376.png)

   - 目录共享机制首先需要明确的是目录本身是不能共享的，共享的是目录下存放的文档；在文档共享的时候可以看到两个名词：默认共享和非默认共享；所谓“默认共享”是指由管理员设置在子目录上的共享对象，当在此目录中新建了文档之后文档会继承此目录中设置的共享对象；而“非默认共享”是指由用户在添加文档之后设置的共享对象；
   - 在目录设置—权限管理中，除了可以设置目录中文档的创建权限外，还可以设置文档默认共享范围
     - 与创建人有关 内部人员：首先是内部人员，即系统中注册的用户，然后才是与文档创建人之间的关系，最后是这个人有什么样的权限，系统中默认为文档创建人本人有完全控制权限，创建人的直接上级拥有的是查看权限，这里需要说明的是默认共享对象中必需有一个人拥有完全控制权限，否则放到这个目录中的文档就没有人可以对这个文档有完全控制权限了；
     - 与创建人有关 外部人员：这里是指非oa系统中的用户，而是指给开通了外部登录账号的客户用户，是由客户创建的文档赋予权限。（可忽略，本公司没有使用）
     - 与创建人无关：这里可以根据分部（指公司）、部门、岗位等相关信息创建共享

6. 选择好人员以后需要选择权限，权限分为查看、编辑与完全控制。

   - 查看：用户可对内容进行浏览，勾选可下载按钮控制下载权限
   - 编辑：对文档拥有修改权限
   - 完全控制：在修改权限的基础上增加，删除权限

   

---

## OA流程自助删除功能使用说明

![1563334312230](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1563334312230.png)

依次点击**“流程”、“新建流程”、“OA流程自助删除”**

![1563334469807](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1563334469807.png)

在需删除流程框中选择需要删除的流程，此处可以查询的流程为本人发起的流程，他人发起的流程无法删除

![1563334543035](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1563334543035.png)

选择后会带出需删除流程的详细信息，确认无误点击提交按钮系统将自动删除。

**ps：一经提交删除的流程将无法找回，请仔细确认是否选择正确。**

