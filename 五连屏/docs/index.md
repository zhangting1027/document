创思感知技术文档 2014.7 对应主版本：V1.2

**第一步：** 对DEMO使用到数据库的调用方式进行配置

目的：

在demo中，有些控件是动态提取数据，为此对数据的提取方式进行配置，以便于控件能够优化且高效的提取所需信息

说明：

根据动态提取数据的方式目前已确定的分为两种，一种是连接数据库DbConnection连接，另外一种是使用xml进行连接XmlData指定文件夹中的数据信息进行动态提取，根据需要选择所需的提取数据的方式，下面将给出两种配置方式，可根据需要选择,具体使用方法会在控件中具体解释

方法：

1. 打开Troncell平台文件，找到Shell下Data文件夹，在该文件夹下打开Data.xml文件，使用编辑工具打开
2. 在Data.xml 添加如下代码：
  1. DbConnection进行数据库连接

\<!--Name为控件在调用数据库连接时候的名字--\>

\<DbDataName="BubbleData"\>

\<!--关于DbData的配置信息节点--\>

\<CustomerConfig\>

\<!--用于连接数据库字符串的配置--\>

\<DbConnection\>

\<!--制定数据库的类型--\>

\<DbType\>System.Data.SQLite\</DbType\>

\<!--连接字符串BasePath是数据目录根目录和BubbleData的目录--\>

\<ConnectionStringValue="Data Source={$BasePath}/{$DataSourcePath};Version=3;Pooling=True;Max Pool Size=100;"\>

\<!--连接使用到的数据库的名称--\>

\<ArgsDataSourcePath="Card.db3"\>\</Args\>

\</ConnectionString\>

\</DbConnection\>

\<!--数据库中所要连接到的表，可有多个Table--\>

\<Tables\>

\<!--Name为执行sql语句后所得到的信息，组成一个虚拟的表名称--\>

| \<TableName="Bubble"\>\<!--value是所需执行的sql语句--\>\<DataQueryValue="select ID,Name,IconPath,EventID,EventAction,NavigatePage,EventPath from FishEye"\>\</DataQuery\>\</Table\>\</Tables\>\</CustomerConfig\>\</DbData\>
 |
| --- |

  1. XmlData指定文件夹中的数据信息进行动态提取

1. 需要在Data.xml同级文件夹中建立一个与下面\<XmlDataName="CirclePanelData"\>中Name相同名称的文件件
2. 在其中添加名称为\<DataQueryValue="CircleData.xml"\>中value值的xml

\<!--Name为控件在调用数据库连接时候的名字--\>

\<XmlDataName="CirclePanelData"\>

\<!--关于DbData的配置信息节点--\>

\<CustomerConfig\>

\<!--数据库中所要连接到的表，可有多个Table--\>

\<Tables\>

\<!--value是所需执行的sql语句--\>

\<TableName="Circle"\>

\<!--value中是所要使用的xml--\>

\<DataQueryValue="CircleData.xml"\>\</DataQuery\>

\</Table\>

\</Tables\>

\</CustomerConfig\>

\</XmlData\>

1. 打开1中新建好的文件夹下2的xml值，添加如下代码：

\<Config\>

\<!--Items为所需要配置的节点放置在Items中， Version的值没有实际意义，整体的结构类似于一张二维表，其中的Item中的信息看做一行信息，Item的个数看做列数--\>

\<ItemsVersion="90"\>

\<!--Item是所需要配置的节点，按照需要配置Item的个数 Name类似于数据库中的行数，ImagePath为资源所在的相对路径，相对于此xml的位置，EventId，EventPath可以为空--\> \<ItemName=""ImagePath="Images\0.jpg"EventId=""EventPath="" /\>

\<ItemName=""ImagePath="Images\1.jpg"EventId=""EventPath="" /\>

\<ItemName=""ImagePath="Images\2.jpg"EventId=""EventPath="" /\>

\<ItemName=""ImagePath="Images\9.jpg"EventId=""EventPath="" /\>

\</Items\>

\</Config\>

3/ **3**