# Sql


create table humans(

     h_id int primary key,
     
	   h_age int,
     
	   h_name varchar(16),
     
	  h_surname varchar(16),
    
	 h_city varchar(16)
   
);


create table pet(

    p_id int primary key,
    
	p_name varchar(16),
  
	p_age int,
  
	p_color varchar(16) ,
	
	h_id int  FOREIGN KEY REFERENCES humans(h_id)
	
	);


DROP TABLE IF EXISTS human_pet;

create table human_pet(
  
	h_id int  FOREIGN KEY REFERENCES humans(h_id),
  
	p_id int  FOREIGN KEY REFERENCES pet(p_id),
  
	primary key(p_id,h_id)
	
);



### dbo.pet


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


![image](https://user-images.githubusercontent.com/61595808/145254301-496bbebb-00da-4d9e-a2ca-f368548381b2.png)


### ------------------------------------------------------------------------------------------------------------

SELECT humans.h_id, humans.h_name ,human_pet.h_id,human_pet.p_id

FROM pet INNER JOIN (humans INNER JOIN human_pet ON humans.h_id = human_pet.h_id) ON pet.p_id = human_pet.p_id

WHERE (((humans.h_surname)='Kaş'));


![image](https://user-images.githubusercontent.com/61595808/145259685-c71c5e89-94fa-4d80-8eca-3325c9d76a66.png)


### ------------------------------------------------------------------------------------------------------------
 


