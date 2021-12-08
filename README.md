# Sql

dbo.pet


Alter Table pet Add p_kind varchar(16);

Insert Into dbo.pet (p_id,p_name,p_age,p_color,p_kind) values (2,'Mavi','3','Blue','Cat');

Insert Into dbo.pet (p_id,p_name,p_age,p_color) values (1,'Bulut','1','Blue');

UPDATE pet SET  p_kind='Bird' WHERE p_id = '1'

UPDATE pet SET  p_color='Blue' WHERE p_id = '1' 

UPDATE pet SET  p_color='Blue' WHERE p_id = '2' 


Insert Into dbo.pet (p_id,p_name,p_age,p_color,p_kind) values (3,'Amber','5','Black','Dog');

Insert Into dbo.pet (p_id,p_name,p_age,p_color,p_kind) values (4,'Amber','5','Black','Dog');

Insert Into dbo.pet (p_id,p_name,p_age,p_color,p_kind) values (5,'Jack','2','Black','Dog');

Insert Into dbo.pet (p_id,p_name,p_age,p_color,p_kind) values (6,'Tarçın','3','Orange','Cat');

Insert Into dbo.pet (p_id,p_name,p_age,p_color,p_kind) values (7,'Nazmi','4','Grey','Cat');

Insert Into dbo.pet (p_id,p_name,p_age,p_color,p_kind) values (8,'Dost','8','White','Dog');

Insert Into dbo.pet (p_id,p_name,p_age,p_color,p_kind) values (9,'Cankuş','1','Yellow','Bird');

Insert Into dbo.pet (p_id,p_name,p_age,p_color,p_kind) values (10,'Limon','2','Yellow','Bird');

UPDATE pet SET  p_kind='Bird', p_name='Love' , p_age='2' WHERE p_id = '4'
