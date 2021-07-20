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

--sequence에 대해 알아보기.
