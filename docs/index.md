# Welcome to MkDocs

For full documentation visit [mkdocs.org](http://mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs help` - Print this help message.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

# le tri
# lop ios28
# Code camp Postgres

# các câu lệnh tạo bảng
```

create table topics(

topic_id serial not null,
topic_name character varying(10),
constraint topic_pk primary key (topic_id)
);

create table questions (

question_id serial not null,
question character varying(100),
wrong_ans character varying(50)[],
true_ans character varying(50),

topic_id integer not null,

constraint questions_pkey primary key (question_id),
constraint questions_topics_topic_fkey foreign key (topic_id) references topics (topic_id)
);

create table level_money (

level_id serial not null,
level_mon integer default 0,
constraint level_money_pk primary key (level_id)
);


--table of user
create table user_id (

user_id serial not null,
user_name character varying(50),
time_play integer not null default 0,
score integer not null default 10,
constraint user_id_pkey primary key (user_id)
)
```

# các câu lệnh truy vấn
```
insert into topics (topic_name) values
('de'),
('tb'),
('kho'); 

--nhap du lieu 100 cau hoi

insert into questions (question,wrong_ans,true_ans,topic_id) values

('1+1','{"1","1","1"}','2',1),
('1+2','{"2","2","2"}','3',1),
('1+3','{"3","3","3"}','4',1),
('1+4','{"4","4","4"}','5',1),
('1+5','{"5","5","5"}','6',1),
('1+6','{"6","6","6"}','7',1),
('1+7','{"7","7","7"}','8',1),
('1+8','{"8","8","8"}','9',1),
('1+9','{"9","9","9"}','10',1),
('1+10','{"10","10","10"}','11',1),

('1+11','{"11","11","11"}','12',1),
('1+12','{"12","12","12"}','13',1),
('1+13','{"13","13","13"}','14',1),
('1+14','{"14","14","14"}','15',1),
('1+15','{"15","15","15"}','16',1),
('1+16','{"16","16","16"}','17',1),
('1+17','{"17","17","17"}','18',1),
('1+18','{"18","18","18"}','19',1),
('1+19','{"19","19","19"}','20',1),
('1+20','{"20","20","20"}','21',1),

('1+21','{"21","21","21"}','22',1),
('1+22','{"22","22","22"}','23',1),
('1+23','{"23","23","23"}','24',1),
('1+24','{"24","24","24"}','25',1),
('1+25','{"25","25","25"}','26',1),
('1+26','{"26","26","26"}','27',1),
('1+27','{"27","27","27"}','28',1),
('1+28','{"28","28","28"}','29',1),
('1+29','{"29","29","29"}','30',1),
('1+30','{"30","30","30"}','31',1),

('1+31','{"31","31","31"}','32',2),
('1+32','{"32","32","32"}','33',2),
('1+33','{"33","33","33"}','34',2),
('1+34','{"34","34","34"}','35',2),
('1+35','{"35","35","35"}','36',2),
('1+36','{"36","36","36"}','37',2),
('1+37','{"37","37","37"}','38',2),
('1+38','{"38","38","38"}','39',2),
('1+39','{"39","39","39"}','40',2),
('1+40','{"40","40","40"}','41',2),

('1+41','{"41","41","41"}','42',2),
('1+42','{"42","42","42"}','43',2),
('1+43','{"43","43","43"}','44',2),
('1+44','{"44","44","44"}','45',2),
('1+45','{"45","45","45"}','46',2),
('1+46','{"46","46","46"}','47',2),
('1+47','{"47","47","47"}','48',2),
('1+48','{"48","48","48"}','49',2),
('1+49','{"49","49","49"}','50',2),
('1+50','{"50","50","50"}','51',2),

('1+51','{"51","51","51"}','52',2),
('1+52','{"52","52","52"}','53',2),
('1+53','{"53","53","53"}','54',2),
('1+54','{"54","54","54"}','55',2),
('1+55','{"55","55","55"}','56',2),
('1+56','{"56","56","56"}','57',2),
('1+57','{"57","57","57"}','58',2),
('1+58','{"58","58","58"}','59',2),
('1+59','{"59","59","59"}','60',2),
('1+60','{"60","60","60"}','61',2),

('1+61','{"61","61","61"}','62',3),
('1+62','{"62","62","62"}','63',3),
('1+63','{"63","63","63"}','64',3),
('1+64','{"64","64","64"}','65',3),
('1+65','{"65","65","65"}','66',3),
('1+66','{"66","66","66"}','67',3),
('1+67','{"67","67","67"}','68',3),
('1+68','{"68","68","68"}','69',3),
('1+69','{"69","69","69"}','70',3),
('1+70','{"70","70","70"}','71',3),

('1+71','{"71","71","71"}','72',3),
('1+72','{"72","72","72"}','73',3),
('1+73','{"73","73","73"}','74',3),
('1+74','{"74","74","74"}','75',3),
('1+75','{"75","75","75"}','76',3),
('1+76','{"76","76","76"}','77',3),
('1+77','{"77","77","77"}','78',3),
('1+78','{"78","78","78"}','79',3),
('1+79','{"79","79","79"}','80',3),
('1+80','{"80","80","80"}','81',3),

('1+81','{"81","81","81"}','82',3),
('1+82','{"82","82","82"}','83',3),
('1+83','{"83","83","83"}','84',3),
('1+84','{"84","84","84"}','85',3),
('1+85','{"85","85","85"}','86',3),
('1+86','{"86","86","86"}','87',3),
('1+87','{"87","87","87"}','88',3),
('1+88','{"88","88","88"}','89',3),
('1+89','{"89","89","89"}','90',3),
('1+90','{"90","90","90"}','91',3),

('1+91','{"91","91","91"}','92',1),
('1+92','{"92","92","92"}','93',1),
('1+93','{"93","93","93"}','94',1),
('1+94','{"94","94","94"}','95',2),
('1+95','{"95","95","95"}','96',2),
('1+96','{"96","96","96"}','97',2),
('1+97','{"97","97","97"}','98',3),
('1+98','{"98","98","98"}','99',3),
('1+99','{"99","99","99"}','100',3),
('1+100','{"100","100","100"}','101',1);


--truy van mot cau hoi bat ky
select * from questions offset random() * (select count(*) from questions) limit 1;

--json ????

select row_to_json(row) from (select * from questions offset random() * (select count(*) from questions) limit 1) row;

-- Hãy cập nhật thông tin bảng với yêu cầu mới thêm
ALTER TABLE questions ADD COLUMN description text;

--Truy vấn số lượng câu hỏi theo mỗi mức độ khó để kiểm tra số lượng

câu hỏi cho mỗi mức độ khó đã bằng nhau chưa:
select count(*) from questions where topic_id = 1;
select count(*) from questions where topic_id = 2;
select count(*) from questions where topic_id = 3;


--Truy vấn lấy ngẫu nhiên được 1 câu hỏi thuộc mức độ Dễ (Trung

bình, Khó):
select * from questions where topic_id = 1 or topic_id = 2 or topic_id = 3 offset random() * (select count(*) from questions where topic_id = 1) limit 1;


--Truy vấn lấy ra ngẫu nhiên 15 câu hỏi và sắp xếp theo thứ tự độ khó

tăng dần (mỗi độ khó có 5 câu hỏi sử dụng UNION):
(select * from questions where topic_id = 1 order by random() limit 5) union all
(select * from questions where topic_id = 2 order by random() limit 5) union all
(select * from questions where topic_id = 3 order by random() limit 5);

-- Nhập dữ liệu cấu hình cho game


insert into level_money (level_mon) values
(800),
(1000),
(1200),
(1500),
(2000),

(2500),
(3000),
(3500),
(4000),
(4500),

(5000),
(5500),
(6000),
(6500),
(7000);

-- Truy vấn lấy được ngẫu nhiên 2 trong số 4 đáp án của 1 câu hỏi bất

kỳ, trong đó bắt buộc phải chứa đáp án đúng:

create or replace function trogiup5050 (id integer) returns table(idd character varying(50), wrongans character varying(50)) as
$body$
begin
return query
select q.true_ans, q.wrong_ans[trunc(3*random()) + 1] from questions as q where q.question_id = id;
end;
$body$
LANGUAGE plpgsql;
select trogiup5050(15);


-- Nhập dữ liệu mẫu 100 người chơi:
insert into user_id (user_name, time_play, score) values
('le a','1','1'),
('le b','2','2'),
('le c','3','3'),
('le d','4','4'),
('le e','4','5'),
('le f','4','6'),
('le g','4','7'),
('le h','4','8'),
('le i','4','9'),
('le k','4','10'),

('le l','5','11'),
('le m','6','12'),
('le n','7','13'),
('le o','8','14'),
('le p','9','15'),
('le v','9','16'),
('le r','9','17'),
('le s','9','38'),
('le t','9','19'),
('le u','9','12'),

('le v','10','145'),
('le w','20','123'),
('le x','10','34'),
('le w','18','1643'),
('le x','28','1345'),
('le A','18','124'),
('le B','28','1456'),
('le C','18','324'),
('le D','17','1547'),
('le E','26','123'),

('le F','14','1435'),
('le J','24','156'),
('le H','14','3534'),
('le I','14','12'),
('le J','24','145'),
('le K','14','1546'),
('le L','24','13'),
('le M','14','35'),
('le N','13','1345'),
('le O','22','1346'),

('le P','15','134'),
('le V','26','156'),
('le R','17','3345'),
('le S','18','12'),
('le T','25','15'),
('le U','14','13'),
('le V','23','14'),
('le W','12','345'),
('le X','12','15'),
('le Y','24','145'),

('le X','17','145'),
('le AA','26','31'),
('le BB','14','23'),
('le CC','13','441'),
('le DD','24','143'),
('le FF','15','1435'),
('le GG','26','156'),
('le HH','17','37'),
('le II','135','156'),
('le JJ','23','145'),

('le KK','13','135'),
('le LL','23','15'),
('le MM','13','33'),
('le NN','13','15'),
('le OO','23','145'),
('le PP','13','12'),
('le VV','23','154'),
('le RR','13','365'),
('le SS','13','14'),
('le TT','23','13'),

('le UU','12','12'),
('le VV','28','13'),
('le WW','18','345'),
('le XX','18','156'),
('le YY','28','1345'),
('le ZZ','18','1645'),
('le 1','28','1234'),
('le 2','18','36'),
('le 3','18','156'),
('le 4','28','165'),

('le 5','14','15'),
('le 5','24','15'),
('le 7','14','36'),
('le 8','14','14'),
('le 9','24','14'),
('le 10','14','31'),
('le 11','24','41'),
('le 12','14','63'),
('le 13','14','14'),
('le 14','24','13'),

('le 15','12','1'),
('le 16','23','1'),
('le 17','1','3'),
('le 18','1','1'),
('le 19','2','1'),
('le 20','1','1'),
('le 21','2','1'),
('le 22','1','3'),
('le 23','1','1'),
('le 24','2','1');

--Tìm kiếm câu hỏi theo id, theo từ khóa trong câu hỏi, theo từ khóa

trong câu trả lời.
CREATE OR REPLACE FUNCTION tim_da(IN chuoi character varying)
RETURNS TABLE(question_id integer, question character varying, wrong_ans character varying[], true_ans character varying, topic_id integer) AS
$BODY$
begin
return query 
select
q.question_id,
q.question,
q.wrong_ans,
q.true_ans,
q.topic_id
from questions as q where (q.true_ans ilike concat('%',$1,'%') or q.wrong_ans[1] ilike concat('%',$1,'%') or
q.wrong_ans[2] ilike concat('%',$1,'%') or q.wrong_ans[3] ilike concat('%',$1,'%') or q.question_id = chuoi::integer);

end;
$BODY$
LANGUAGE plpgsql VOLATILE
COST 100
ROWS 1000;
ALTER FUNCTION tim_da(character varying)
OWNER TO postgres;

--Xóa một câu hỏi:
delete from questions as q where q.question_id = 100;
ALTER SEQUENCE questions_question_id_seq RESTART;
UPDATE questions SET question_id = DEFAULT;
```





