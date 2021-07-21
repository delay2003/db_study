## postgresql db study 

--select
select * from dept;

--insert
insert into dept (deptno, dname, loc) values (10, 'ACCOUNTING', 'NEW YORK');
insert into dept (deptno, dname, loc) values (20, 'RESEARCH', 'DALLAS');

--delete
delete from dept where deptno = 30;

--update
update dept set deptno = 30 where deptno = 20;

--sequence
--유일한 값을 생성하게 도와주는 객체
--주로 ID와 같이 순차적으로 증가하는 COL에 많이 사용
create sequence seq_deptno start 50 increment 10; 
insert into dept (deptno, dname, loc) values (nextval('seq_deptno'), null , 'SEOUL');
drop sequence seq_deptno;
select currval('seq_deptno');

--where
--like
--특정패턴과 유사한 집합 (%, _)
select dname from dept where dname like '%E%'; 
select dname from dept where dname not like '%E%';

--in
--조회하고자 하는 값이 여러개일때, in(a,b,c)
select * from dept where deptno in (20,40);

--between
--~이상 ~이하 값들에 사용
select * from dept where deptno between 20 and 40;

--is null
select * from dept where dname is null;

--is not null
select * from dept where dname is not null;
