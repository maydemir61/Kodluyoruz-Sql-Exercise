## Exercise1
~~~~ sql
select title,description from film;
select * from film where length>60 and length<75;
select * from film where rental_rate=0.99 and replacement_cost = 12.99 or replacement_cost=28.99;
select last_name from customer where first_name='Mary'; 
select * from film where not length>50 and not(rental_rate=2.99 or rental_rate=4.99);
~~~~

## Exercise2

~~~~ sql
select * from film where replacement_cost between 12.99 and 16.99;
select * from actor where first_name in('Penelope','Nick','Ed');
select * from film where rental_rate in(0.99,2.99,4.99) and replacement_cost in (12.99,15.99,28.99);
~~~~

## Exercise3

~~~~sql
select * from country where country like 'A%a';
select * from country where country like '______%n' ;
select * from country where country Ilike '%t%t%t%t%';
select * from film where title like 'C%' and length>90 and rental_rate in (2.99)
~~~~

## Exercise4

~~~~ sql
select distinct replacement_cost from film;
select count( distinct replacement_cost )from film;
select count(*) from film where title like 'T%' and rating in('G');
select count(*) from country where Length(country)=5;
select count(*) from city where city Ilike '%r';
~~~~

## Exercise5

~~~~ sql
select * from film where title like '%n' 
order by length desc limit 5 ;
select * from film where title like '%n'
order by length  offset 5 limit 5;
select * from customer where store_id in(1) 
order by last_name desc limit 4 ;
~~~~

## Exercise6

~~~~ sql
select round(avg(rental_rate),3) from film;
select COUNT(*) from film where title like 'C%';
select Max(length) from film where rental_rate in(0.99);
select count(distinct replacement_cost) from film where length>150 ;
~~~~

## Exercise7

~~~~sql
select rating,count(*) from film group by rating;
select replacement_cost,count(*) from film group by replacement_cost having count(*)>50 order by replacement_cost;
select store_id,count(*) from customer group by store_id;
select count(*) from city group by country_id order by count(*) desc limit 1
~~~~

## Exercise8

~~~~sql
create table employee (
id int not null,
name varchar(50),
birthday date,
email varchar(100)
)

insert into employee (id, name, email, birthday) values (1, 'Kevyn Maciunas', 'kmaciunas0@businessweek.com', '2021/05/30');
insert into employee (id, name, email, birthday) values (2, 'Barris Brunskill', 'bbrunskill1@naver.com', '2021/03/03');
insert into employee (id, name, email, birthday) values (3, 'Edee Stoeckle', 'estoeckle2@ifeng.com', '2021/04/06');
insert into employee (id, name, email, birthday) values (4, 'Fletch Colley', 'fcolley3@who.int', '2021/02/12');
insert into employee (id, name, email, birthday) values (5, 'Katya Livick', 'klivick4@businessweek.com', '2020/08/08');
insert into employee (id, name, email, birthday) values (6, 'Godiva Tabour', 'gtabour5@parallels.com', '2021/02/20');
insert into employee (id, name, email, birthday) values (7, 'Ricoriki Iceton', 'riceton6@seesaa.net', '2020/11/21');
insert into employee (id, name, email, birthday) values (8, 'Constantina O''Keevan', 'cokeevan7@indiegogo.com', '2020/12/02');
insert into employee (id, name, email, birthday) values (9, 'Pamela O''Dea', 'podea8@statcounter.com', '2021/01/05');
insert into employee (id, name, email, birthday) values (10, 'Richmond Lissimore', 'rlissimore9@51.la', '2020/11/11');
insert into employee (id, name, email, birthday) values (11, 'Jose Tarplee', 'jtarpleea@nydailynews.com', '2020/08/11');
insert into employee (id, name, email, birthday) values (12, 'Garvin Doe', 'gdoeb@abc.net.au', '2020/09/20');
insert into employee (id, name, email, birthday) values (13, 'Farris MacNab', 'fmacnabc@blogs.com', '2021/07/15');
insert into employee (id, name, email, birthday) values (14, 'Janaye Gapper', 'jgapperd@msu.edu', '2020/09/24');
insert into employee (id, name, email, birthday) values (15, 'Rustie Schruurs', 'rschruurse@mayoclinic.com', '2020/08/24');
insert into employee (id, name, email, birthday) values (16, 'Rhona Vlach', 'rvlachf@ustream.tv', '2021/06/07');
insert into employee (id, name, email, birthday) values (17, 'Konrad Pendrigh', 'kpendrighg@wikispaces.com', '2020/11/01');
insert into employee (id, name, email, birthday) values (18, 'Clarance Oselton', 'coseltonh@nps.gov', '2020/11/08');
insert into employee (id, name, email, birthday) values (19, 'Deva Longhurst', 'dlonghursti@narod.ru', '2021/06/11');
insert into employee (id, name, email, birthday) values (20, 'Cheslie Antoniazzi', 'cantoniazzij@liveinternet.ru', '2020/12/22');
insert into employee (id, name, email, birthday) values (21, 'Calhoun Lamb-shine', 'clambshinek@pcworld.com', '2021/01/25');
insert into employee (id, name, email, birthday) values (22, 'Lucien Ridolfi', 'lridolfil@newsvine.com', '2020/12/02');
insert into employee (id, name, email, birthday) values (23, 'Bertrand Diack', 'bdiackm@google.ca', '2021/01/25');
insert into employee (id, name, email, birthday) values (24, 'Hynda Denerley', 'hdenerleyn@domainmarket.com', '2020/08/22');
insert into employee (id, name, email, birthday) values (25, 'Shayne Romayn', 'sromayno@constantcontact.com', '2021/03/23');
insert into employee (id, name, email, birthday) values (26, 'Nata Sline', 'nslinep@mayoclinic.com', '2020/09/07');
insert into employee (id, name, email, birthday) values (27, 'Jacquetta Lyven', 'jlyvenq@epa.gov', '2020/08/29');
insert into employee (id, name, email, birthday) values (28, 'Nertie O''Dempsey', 'nodempseyr@un.org', '2020/08/06');
insert into employee (id, name, email, birthday) values (29, 'Jaine Middlemist', 'jmiddlemists@acquirethisname.com', '2021/01/13');
insert into employee (id, name, email, birthday) values (30, 'Birk Threadgill', 'bthreadgillt@tuttocitta.it', '2021/01/28');
insert into employee (id, name, email, birthday) values (31, 'Culley Caherny', 'ccahernyu@foxnews.com', '2021/02/06');
insert into employee (id, name, email, birthday) values (32, 'Jason Dubock', 'jdubockv@dailymail.co.uk', '2021/02/04');
insert into employee (id, name, email, birthday) values (33, 'Peria Middle', 'pmiddlew@technorati.com', '2020/12/14');
insert into employee (id, name, email, birthday) values (34, 'Kylie Beartup', 'kbeartupx@tamu.edu', '2020/12/05');
insert into employee (id, name, email, birthday) values (35, 'Fielding Flanne', 'fflanney@opera.com', '2021/07/12');
insert into employee (id, name, email, birthday) values (36, 'Lenna Almak', 'lalmakz@discovery.com', '2021/06/28');
insert into employee (id, name, email, birthday) values (37, 'Angy Curtain', 'acurtain10@google.com.au', '2021/07/10');
insert into employee (id, name, email, birthday) values (38, 'Emogene Turbayne', 'eturbayne11@sciencedirect.com', '2020/12/23');
insert into employee (id, name, email, birthday) values (39, 'Natividad Rikard', 'nrikard12@icio.us', '2021/03/06');
insert into employee (id, name, email, birthday) values (40, 'Ax MacAlpine', 'amacalpine13@angelfire.com', '2020/08/29');
insert into employee (id, name, email, birthday) values (41, 'Prince Talmadge', 'ptalmadge14@prnewswire.com', '2021/06/28');
insert into employee (id, name, email, birthday) values (42, 'Helenelizabeth Godfree', 'hgodfree15@themeforest.net', '2021/07/01');
insert into employee (id, name, email, birthday) values (43, 'Julianna Burrus', 'jburrus16@artisteer.com', '2021/03/15');
insert into employee (id, name, email, birthday) values (44, 'Maxwell Bocock', 'mbocock17@merriam-webster.com', '2020/09/23');
insert into employee (id, name, email, birthday) values (45, 'Riva Stuckley', 'rstuckley18@hibu.com', '2021/05/16');
insert into employee (id, name, email, birthday) values (46, 'Geneva Dyett', 'gdyett19@microsoft.com', '2021/02/21');
insert into employee (id, name, email, birthday) values (47, 'Conny Beaushaw', 'cbeaushaw1a@google.cn', '2020/09/27');
insert into employee (id, name, email, birthday) values (48, 'Howard Rove', 'hrove1b@globo.com', '2021/06/17');
insert into employee (id, name, email, birthday) values (49, 'Seward Van Castele', 'svan1c@cmu.edu', '2021/07/13');
insert into employee (id, name, email, birthday) values (50, 'Stevana Cadlock', 'scadlock1d@posterous.com', '2020/09/28');
insert into employee (id, name, email, birthday) values (51, 'Caroline Schleswig-Holstein', 'cschleswigholstein1e@hhs.gov', '2021/02/19');
insert into employee (id, name, email, birthday) values (52, 'Cathrine Labin', 'clabin1f@vkontakte.ru', '2020/08/16');
insert into employee (id, name, email, birthday) values (53, 'Ethelred Casely', 'ecasely1g@china.com.cn', '2021/06/28');
insert into employee (id, name, email, birthday) values (54, 'Elliott Helsby', 'ehelsby1h@statcounter.com', '2020/08/20');
insert into employee (id, name, email, birthday) values (55, 'Shawn Whitton', 'swhitton1i@nydailynews.com', '2020/12/07');
insert into employee (id, name, email, birthday) values (56, 'Daile Stredwick', 'dstredwick1j@51.la', '2021/06/18');
insert into employee (id, name, email, birthday) values (57, 'Kristos Balazs', 'kbalazs1k@constantcontact.com', '2021/07/21');
insert into employee (id, name, email, birthday) values (58, 'Hettie Labroue', 'hlabroue1l@vk.com', '2021/03/13');
insert into employee (id, name, email, birthday) values (59, 'Urban Millin', 'umillin1m@ucoz.com', '2021/06/21');
insert into employee (id, name, email, birthday) values (60, 'Gil Ticehurst', 'gticehurst1n@telegraph.co.uk', '2020/08/24');
insert into employee (id, name, email, birthday) values (61, 'Niki Coller', 'ncoller1o@ucoz.com', '2021/05/02');
insert into employee (id, name, email, birthday) values (62, 'Maribelle Branson', 'mbranson1p@uol.com.br', '2021/01/02');
insert into employee (id, name, email, birthday) values (63, 'Marrilee Strangeway', 'mstrangeway1q@cam.ac.uk', '2021/01/14');
insert into employee (id, name, email, birthday) values (64, 'Hasheem Sayle', 'hsayle1r@purevolume.com', '2021/01/30');
insert into employee (id, name, email, birthday) values (65, 'Bev Wherton', 'bwherton1s@liveinternet.ru', '2021/07/22');
insert into employee (id, name, email, birthday) values (66, 'Mathe Haggeth', 'mhaggeth1t@cnbc.com', '2020/12/09');
insert into employee (id, name, email, birthday) values (67, 'Olag Stuck', 'ostuck1u@booking.com', '2021/02/17');
insert into employee (id, name, email, birthday) values (68, 'Bay Eagell', 'beagell1v@phpbb.com', '2020/08/31');
insert into employee (id, name, email, birthday) values (69, 'Betti Thurlby', 'bthurlby1w@tripadvisor.com', '2021/01/29');
insert into employee (id, name, email, birthday) values (70, 'Brooks Bassham', 'bbassham1x@godaddy.com', '2021/05/21');
insert into employee (id, name, email, birthday) values (71, 'Heindrick Pendre', 'hpendre1y@sciencedirect.com', '2020/11/27');
insert into employee (id, name, email, birthday) values (72, 'Thekla Adamsson', 'tadamsson1z@pagesperso-orange.fr', '2020/10/18');
insert into employee (id, name, email, birthday) values (73, 'Bard Gossage', 'bgossage20@apache.org', '2020/09/17');
insert into employee (id, name, email, birthday) values (74, 'Eziechiele Hatter', 'ehatter21@npr.org', '2021/04/28');
insert into employee (id, name, email, birthday) values (75, 'Findley Ivashov', 'fivashov22@sourceforge.net', '2021/03/31');
insert into employee (id, name, email, birthday) values (76, 'Noami Seabrook', 'nseabrook23@ask.com', '2020/09/30');
insert into employee (id, name, email, birthday) values (77, 'Toddie Borton', 'tborton24@webeden.co.uk', '2020/10/22');
insert into employee (id, name, email, birthday) values (78, 'Leo Cobbe', 'lcobbe25@biglobe.ne.jp', '2021/06/08');
insert into employee (id, name, email, birthday) values (79, 'Danica Schleicher', 'dschleicher26@lycos.com', '2021/05/12');
insert into employee (id, name, email, birthday) values (80, 'Elihu Pyle', 'epyle27@a8.net', '2021/05/03');
insert into employee (id, name, email, birthday) values (81, 'Idelle Swainsbury', 'iswainsbury28@163.com', '2021/04/11');
insert into employee (id, name, email, birthday) values (82, 'Gisela Thoumasson', 'gthoumasson29@amazon.com', '2021/05/30');
insert into employee (id, name, email, birthday) values (83, 'Janetta Bromley', 'jbromley2a@people.com.cn', '2021/05/15');
insert into employee (id, name, email, birthday) values (84, 'Myles Neal', 'mneal2b@opensource.org', '2021/04/08');
insert into employee (id, name, email, birthday) values (85, 'Marilee Montgomery', 'mmontgomery2c@t-online.de', '2020/09/27');
insert into employee (id, name, email, birthday) values (86, 'Rina Dibley', 'rdibley2d@last.fm', '2021/04/10');
insert into employee (id, name, email, birthday) values (87, 'Hamlin Perazzo', 'hperazzo2e@soup.io', '2020/08/09');
insert into employee (id, name, email, birthday) values (88, 'Celene MacAndrew', 'cmacandrew2f@craigslist.org', '2020/10/06');
insert into employee (id, name, email, birthday) values (89, 'Vicki Settle', 'vsettle2g@dailymail.co.uk', '2021/07/21');
insert into employee (id, name, email, birthday) values (90, 'Reinaldos Acom', 'racom2h@about.me', '2020/11/27');
insert into employee (id, name, email, birthday) values (91, 'Shela Antonescu', 'santonescu2i@aol.com', '2021/04/09');
insert into employee (id, name, email, birthday) values (92, 'Immanuel Girvin', 'igirvin2j@usgs.gov', '2021/07/23');
insert into employee (id, name, email, birthday) values (93, 'Hazel Feild', 'hfeild2k@github.com', '2020/12/31');
insert into employee (id, name, email, birthday) values (94, 'Janis Pascho', 'jpascho2l@alexa.com', '2020/07/31');
insert into employee (id, name, email, birthday) values (95, 'Lorine Blackader', 'lblackader2m@miibeian.gov.cn', '2020/10/02');
insert into employee (id, name, email, birthday) values (96, 'Hazlett Masic', 'hmasic2n@surveymonkey.com', '2021/05/24');
insert into employee (id, name, email, birthday) values (97, 'Evvy Bumpas', 'ebumpas2o@issuu.com', '2021/07/18');
insert into employee (id, name, email, birthday) values (98, 'Kendrick Gundrey', 'kgundrey2p@bbb.org', '2021/04/15');
insert into employee (id, name, email, birthday) values (99, 'Jo Brickham', 'jbrickham2q@usda.gov', '2020/10/25');
insert into employee (id, name, email, birthday) values (100, 'Carmel Olijve', 'colijve2r@pcworld.com', '2021/07/09');


update employee set name='Ali Birinci' where id =99;
update employee set birthday='1990-05-05' where id =90;
update employee set email='email@email.com' where name like 'A%';
update employee set name='Şükrü' where id=10; 
update employee set name='Ali Birinci' where id =75;

delete from employee where id =1;
delete from employee where name like 'A%';
delete from employee where name like '%Jo%';
delete  from employee where id =15;
delete from employee where id between 10 and 20;
~~~~

## Exercise9

~~~~sql
select city,country from country join city on country.country_id=city.country_id;
select payment_id,first_name,last_name from customer join payment on  customer.customer_id=payment.customer_id;
select first_name,last_name,rental_id from customer join rental on customer.customer_id=rental.customer_id;
~~~~

## Exercise10

~~~~sql
select city,country from city left join country on city.country_id=country.country_id;
select payment_id,first_name,last_name from customer right join payment on customer.customer_id=payment.customer_id;
select rental_id,first_name,last_name from customer full join rental on customer.customer_id=rental.customer_id; 
~~~~
