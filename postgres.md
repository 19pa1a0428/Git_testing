create table Test(
order_num int Primary key
);

select * from Test

alter table Test add trader varchar(50);

insert into Test values ('1', 'Rahul')

insert into Test values ('2', 'Venkata')

alter table Test add facility_id varchar(50)

update Test set facility_id = '2' where order_num = '2'


create table facility (
	facility_id int primary key,
	facility_name varchar(50)
);

select * from facility
select * from test

insert into facility values ('1', 'test supplier')

alter table facility rename column facility_name to facility

alter table facility add test_col int
alter table facility drop test_col

ALTER TABLE test
ALTER COLUMN facility_id TYPE INTEGER
USING facility_id::INTEGER;

select order_num, trader, facility from test inner join facility on test.facility_id = facility.facility_id


select count(*) from test where facility_id = '1'
