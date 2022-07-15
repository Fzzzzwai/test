*斜体*

_斜体_

__粗体__

**粗体**

***加粗斜体***

___加粗斜体___

~~删除线~~



# 一级标题

## 二级标题

### 三级标题

#### 四级标题

##### 五级标题

###### 六级标题



* 无序列表*
* 无序列表*

+ 无序列表+
+ 无序列表+

- 无序列表-
- 无序列表-

1. 有序列表
2. 有序列表

 - 无序列表1
   - 无序列表1.1
   - 无序列表1.2

[百度](www.baidu.com)

> 这是一个引用



> 第一层
>
> > 第二层
> >
> > > 第三层



------------------------------

***



<u>下划线</u>



| 姓名 | 年龄 | 工作 |
| :--: | :--: | :--: |
| 方正 |  20  | 学生 |
|      |      |      |

| 姓名 | 工作 | 年龄 |
| ---- | ---- | ---- |
|      |      |      |



<img src="D:\Pictures\24.jpg" alt="科比" style="zoom:100%;" />





链接：[百度](www.baidu.com)

脚注：[文字](解释“脚注名字”)

`printf("hello world");`

```java
    public void testUpdate() throws Exception {
    // 接收页面提交的参数
    String brandName = "香飘飘";
    String companyName = "香飘飘";
    int ordered = 1000;
    String description = "绕地球三圈";
    int status = 1;
    int id = 4;
          //1. 获取Connection
    //3. 加载配置文件
    Properties prop = new Properties();
    prop.load(new FileInputStream("jdbc-demo/src/druid.properties"));
    //4. 获取连接池对象
    DataSource dataSource = DruidDataSourceFactory.createDataSource(prop);

    //5. 获取数据库连接 Connection
    Connection conn = dataSource.getConnection();

    //2. 定义SQL
    String sql = " update tb_brand\n" +
            "         set brand_name  = ?,\n" +
            "         company_name= ?,\n" +
            "         ordered     = ?,\n" +
            "         description = ?,\n" +
            "         status      = ?\n" +
            "     where id = ?";

    //3. 获取pstmt对象
    PreparedStatement pstmt = conn.prepareStatement(sql);

    //4. 设置参数
    pstmt.setString(1,brandName);
    pstmt.setString(2,companyName);
    pstmt.setInt(3,ordered);
    pstmt.setString(4,description);
    pstmt.setInt(5,status);
    pstmt.setInt(6,id);

    //5. 执行SQL
    int count = pstmt.executeUpdate(); // 影响的行数
    //6. 处理结果
    System.out.println(count > 0);
          //7. 释放资源
    pstmt.close();
    conn.close();
    }
```





