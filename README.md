# CS209A_Project

## Topic A

1. 各个国家java代码质量

   1. 

2. 各国家java使用人数

   1. 通过项目查找人的国家
   2. 统计人数

3. 地区活跃度

   - 人的最后更新时间

4. 组织影响力

5. java时间尺度的流行度和频率趋势

   1. 项目创建及更新时间
   2. 项目数量

   <img src="README.assets/image-20220429204839551.png" alt="image-20220429204839551" style="zoom:50%;" />

6. Github Repos Total Stars in Time

   - star数量时间变化



## Topic B

> pay attention, search API may don't give out the entire results

JAVA发展趋势分析:

> 1. analyse the language itself
> 2. analyse its community which stands for vitality of a language

> targets: JAVA developers

1. Total trending

   1. 流行度 (how many people use it): 
      - repos的数量，总数或者只看增长速率 ( in recent years)
      - advanced: use stars, forks and more metrics (average stars or else) to evaluate the popularity
   2. 和哪些语言配合比较多: 
      - star最多的前20%（or fixed number）的repo中, which languages does JAVA coopereate with.
   3. what are hot topics and fields:
      - use description of repos to analyse frequency of words

   > Goal: give users a picture about how popular Java is nowadays and give developers some suggestions about what they should learn to catch up with the development of JAVA

2.  community situation:

   > haven't come up with detail solutions, followings are just conceptions

   1. number of issue, PR, comments 
   2. updated time of things above
   3. habits of users involved in  JAVA repos 
      1. what's the work time for them during a day (or a week)

   > Goal: manifest vigour of JAVA, and also give JAVA developers advice on how and when to communicate with other JAVA developers.

## Tools
### API
github API: https://docs.github.com/cn/rest
### Third Libraries
Echarts: https://echarts.apache.org/zh/index.html

### Reference
analysis 1: https://www.benfrederickson.com/github-developer-locations/

github official report: https://baijiahao.baidu.com/s?id=1716745477182306006&wfr=spider&for=pc

### Others
star时间

```
Accept: application/vnd.github.v3+json
https://api.github.com/repos/OWNER/REPO/stargazers
```

