# lj_crawl
一个爬取链家（上海）房价的爬虫。  
  
## lj_get_plate.py  
用于爬取城市板块名称，并保存至数据库。  
  
## lj_get_data.py  
用于爬取房价数据，并保存至/tmp/tmp_house.txt  
![district](https://github.com/jacenr/lj_crawl/blob/master/Screenshots/district.png) 
![plate](https://github.com/jacenr/lj_crawl/blob/master/Screenshots/plate.png) 
  
## house_price_sample_20171226.txt  
为爬取的样例数据。  
```
sh4644321,260,62230    // 房源ID，总价，单价
sh4853052,450,69039
sh4829769,280,63854
sh4794551,192,66875
sh4755861,358,61937
sh4820639,215,67313
sh4817861,550,63569
```

## 使用方法  
在Linux下执行如下步骤：  
* 在mysql中创建db: lianjia  
* 修改py文件中mysql_conn变量的连接信息  
* 修改py文件中lj_ershou_url变量的url为你想爬取城市的二手房url  
* 运行lj_get_plate.py初始化lianjia数据库  
* 执行lj_get_data.py爬取链家房价  