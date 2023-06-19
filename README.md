# Design_of_databse_for_Limitless_Estatee
This mini project mainly focuses on designing of database for Limitless Real Estate 

## Introduction: 
	A limitless estate database design allows for the storage and management of a vast amount of estate-related data, accommodating the ever-growing volume of information as the database expands. By adopting a limitless design approach, the database can easily adapt to changing requirements and accommodate new types of estate-related data without significant restructuring or limitations.

## Goals:

1.Develop a user-friendly website that provides a seamless experience for CP-Firms and their clients, focusing on intuitive navigation, clear information presentation, and easy accessibility to essential features.

2.Integrate advanced real estate CRM software that centralizes customer data, allowing CP-Firms to access comprehensive profiles, preferences, and communication history, enabling personalized and targeted interactions with clients.

3.Enable secure and organized data storage, ensuring that customer information is safely stored and easily accessible to authorized personnel, minimizing the risk of data loss or mishandling.

4.Provide analytics and reporting capabilities to gain insights into customer behavior, and sales performance, empowering CP-Firms to make data-driven decisions and optimize their strategies.

5.Improve operational efficiency for CP-Firms by automating repetitive tasks, simplifying data management, and streamlining workflows, reducing manual efforts and enhancing productivity. 
																												
## Database of Limitless Estate system consist of following entities:

## •	clients : - 

This entity contains the id, client_first_name , client_last_name , client_
email , client_contact , prefer_location and budget 

## •	property :- 

This entity contains id, property_name, price, no_of_bedrooms, no_of_flats, carpet_area, amenities, agent_id, city_id, region_id

## •	agents :- 

This entity contains id, agent_first_name, agent_last_name, agent_email, agent_contact, agent_location 

## •	sales :- 

This entity contains id, property_id, client_id, agent_id, sale_price, sale_date

## •	city :- 

This entity contains id, city_name

## •	region :- 

This entity contains id, region_name

## •	address :- 

This entity contain id, city_id, region_id

## •	admins :- 

This entity contain id, admin_first_name, admin_last_name, admin_email, admin_login_id, admin_password
														
## Database design:-

## 1.	clients 
Field 	            Type	         Null	   Key	          Extra

id	                 int          	No	  primary		  auto_increment
client_first_name	varchar(20)     	No			
client_last_Name	varchar(20)	      No			
client_email	    varchar(30)     	No			
client_contact	    int           	No			
prefer_location	  varchar(15)	      No			
budget	         decimal(10,2)    	No			


## 2.	regions
Field	        Type	      Null	  Key	      	Extra

id	          int 	       No	  primary		auto_increment
region_name	varchar(15)	   No			


## 3.	cities
Field	    Type	      Null	  Key	    	Extra

id	       int 	      No	  primary		auto_increment
city_name	varchar(15)	No			


## 4.	addresses
Field	    Type	  Null	  Key		      Extra

id	       int	   No	   primary		auto_increment
city_id    int	   No	   foreign		
region_id  int	   No	   foreign		



5.	properties
Field	Type	Null	Key	Default	Extra
     id	int 	No	primary		Auto_increment
property_name	varchar(20)	No			
price	decimal(10,2)	No			
no_of_bedrooms	int	No			
no_of_flats	int	No			
carpet_area	int	No			
amenities	varchar(100)	No			
agent_id	int	No	foreign		
city_id	int	No	foreign		
region_id	int	No	foreign		




6.	agents
Field	Type	Null	Key	Default	Extra
        id	int	No	primary		auto_increment
agent_first_name	varchar(10)	No			
agent_last_name	varchar(10)	No			
agent_email	varchar(30)	No			
agent_contact	varchar(15)	No			
agent_location	int	No	foreign		



7.	sales
Field	Type	Null	Key	Default	Extra
    id	int	No	primary		auto_increment
property_id	int	No	foreign		
client_id	int	No	foreign		
agent_id	int	No	foreign		
sale_price	double(10,2)	No			
sale_date	date	No			



8.	admins
Field	Type	Null	Key	Default	Extra
       id	int	No	primary		auto_increment
admin_first_name	varchar(10)	No			
admin_last_name	varchar(10)	No			
admin_email	varchar(20)	No			
admin_login_id	int	No			
admin_password	varchar(10)	No			




