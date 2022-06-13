# SQL语言案例

## 一、基本查询

1. 查询所有学生的所有信息

   SELECT * FROM STX_STUDENTS ;

2. 只查询姓名和院系信息

   SELECT STU_ID ,STU_NAME  FROM STX_STUDENTS ;

3. 将stu_name、college分别起别名为姓名、院系

   SELECT STU_NAME AS "姓名",COLLEGE AS "院系" FROM STX_STUDENTS ;

## 二、条件查询

1. 查询男生信息

   SELECT * FROM STX_STUDENTS ss WHERE GENDER = '男';

2. 查询姓李、姓周的小伙伴，查询名字以龙结尾的小伙伴

   SELECT * FROM STX_STUDENTS ss WHERE STU_NAME LIKE '李%' ;

   SELECT * FROM STX_STUDENTS ss WHERE STU_NAME LIKE '周%' ;

   SELECT * FROM STX_STUDENTS ss WHERE STU_NAME LIKE '%龙' ;

3. 查询姓名为两个字的小伙伴

   SELECT * FROM STX_STUDENTS ss WHERE STU_NAME LIKE '__' ;

4. 查询院系为大数据与软件学院的学生

   SELECT * FROM STX_STUDENTS ss WHERE COLLEGE  = '大数据与软件学院' ;

5. 查询系为大数据与软件学院，并且专业为软件工程的学生

   STX_STUDENTS ss WHERE COLLEGE  = '大数据与软件学院' AND MAJOR = '软件工程' ;

6. 查询成绩在80~90之间的学生

   SELECT * FROM STX_STUDENTS ss WHERE SCORE BETWEEN 80 AND 90 ;

## 二、排序

1. 按成绩降序排序

   SELECT * FROM STX_STUDENTS ss ORDER BY SCORE DESC  ;

2. 按院系和成绩排序

   SELECT * FROM STX_STUDENTS ss ORDER BY COLLEGE , SCORE ;

## 三、聚合函数

1. 统计学生个数

   SELECT COUNT(STU_ID) FROM STX_STUDENTS ss ; 

2. 统计智能工程学院有多少学生

   SELECT COUNT(*) FROM STX_STUDENTS ss WHERE COLLEGE = '智能工程学院' ; 

3. 统计软件工程专业有多少学生

   SELECT COUNT(*) FROM STX_STUDENTS ss WHERE MAJOR  = '软件工程' ; 

4. 统计有多少个院系

   SELECT COUNT(DISTINCT COLLEGE)  FROM STX_STUDENTS ss; 

5. 求平均分数

   SELECT AVG(SCORE)  FROM STX_STUDENTS ss; 

6. 求最高分

   SELECT MAX(SCORE)  FROM STX_STUDENTS ss; 

7. 同时求平均分，最高分

   SELECT AVG(SCORE), MAX(SCORE)  FROM STX_STUDENTS ss; 

## 四、分组查询

1. 统计每个院系有多少人

   SELECT COLLEGE , COUNT(*) AS "人数"  FROM STX_STUDENTS ss GROUP BY COLLEGE ; 

2. 统计每个院系有多少人并按人数进行排序

   SELECT COLLEGE , COUNT(*) AS "人数"  FROM STX_STUDENTS ss GROUP BY COLLEGE ORDER BY COUNT(*)  ;

3. 统计各院系的平均分数

   SELECT COLLEGE , AVG(SCORE) AS "平均分"  FROM STX_STUDENTS ss GROUP BY COLLEGE  ;

4. 统计各院系的平均分数，并按平均分排序

   SELECT COLLEGE , AVG(SCORE) AS "平均分"  FROM STX_STUDENTS ss GROUP BY COLLEGE ORDER BY AVG(SCORE) ;

5. 统计各院系的平均分数，只统计人数在2人以上的院系。阅读PPT303页where 和 having的区别

   SELECT COLLEGE , COUNT(COLLEGE)  AS "人数"  FROM STX_STUDENTS ss GROUP BY COLLEGE HAVING COUNT(1) > 2  ;

## 五、联表查询



