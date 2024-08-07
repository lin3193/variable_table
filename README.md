# variable_table
使用變數方式表值函數@的暫時資料表，相對於使用#的暫存表無法使用索引、不需要drop執行後會自動釋放。可用於table function
```
-- declare table
declare @tmp_people as TABLE 
(
	id int,
    username NVARCHAR(100),
    age int
)

-- 2 rows
INSERT INTO @tmp_people (id,username,age)
VALUES
(1,'Wang',20),(2,'Lin',28)

-- select 
select * from @tmp_people
```
result:
```
id	username	age
1	Wang	20
2	Lin	28
```
