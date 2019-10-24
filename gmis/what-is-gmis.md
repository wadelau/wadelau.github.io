# [gMIS](/gmis/index)
## [What is gMIS?](/gmis/what-is-gmis)

### gMIS: A general-purpose management information system software.
![gMIS Logo](https://ufqi.com/dev/gmis/gmis-logo-201606.png)

### gMIS in a Brief
-gMIS is a [-GWA2](https://ufqi.com/dev/gwa2/) based Management Information System (MIS) software with configurable input and output interfaces.  

Various management application software systems can be built on it, such as  
-- Content Management System (CMS), 
-- Customer Resource Management (CRM), 
-- Enterprise Resource Planning Management (ERP),  
-- Office automation systems (OA), 

as well as different industry application management system softwares, such as  
-- Human Resource Management System (HR), 
-- Student Management, 
-- Archive Management, 
-- Tourism Management, 
-- Book Management,  
-- Commodity Management and business operations support systems (BOSS), etc.  

With zero code development, -gMIS can build a set of management information systems (MIS) software in a few minutes.

Its slogan is **Lower Costs, 较低成本; Better Productivity, 较高效率**.

### gMIS Background

> “In a demand-driven opinion, we faced increasing requests of creating enormous table-based management tools for operation teams in years of 2005-2010 at ChinaM, an affiliate of [Telstra](http://telstra.com.au) in Beijing.  
> Those shared some common functions and most of them just needed to achieve basic goals (CURDLS) for a table.
> So we conducted many practices to find one to meet this kind of demand, for all, forever.”

Its source code locates in [-GitHub-Wadelau](https://github.com/wadelau/gMIS) , and its live demo lives in [-gmis](https://ufqi.com/dev/gmis/gmis-demo) .  
  
This project has been started and pondered during the study in the [University of Derby](https://www.derby.ac.uk/),  and it is based on some observations and demands from ChinaM. 

In the short time in [Sina Corp](http://weibo.com),  it has been created from top to down and the polishing work are continuing and lasting till now.  

### Main Developers
[Zhenxing Liu](https://github.com/wadelau), 

Shujuan Wang, 

Ding Xu, 

Shaopeng Xu, 

Cecil Yuan

### gMIS Layouts
![gMIS Layouts](https://ufqi.com/dev/gmis/page-relation.201303.v1.png)

####	MIS, GWA2 and gMIS
According to OCC’s MIS guidelines , a Management Information System (MIS) is defined as “a system or process that provides the information necessary to manage an organization effectively. MIS and the information it generates are generally considered essential components of prudent and reasonable business decisions”. A MIS has these goals:

- Enhance communication among employees.

- Deliver complex material throughout the institution.

- Provide an objective system for recording and aggregating information.

- Reduce expenses related to labour-intensive manual activities.

 - Support the organization's strategic goals and direction.

Regarding to general purposes, especially with MySQL as back-end, we have tools like phpMyAdmin  and its descendant, Chive  (Web-based MySQL Admin Interface). These systems have three common merits:

 - No-targeting user data.

 - On-demand and instant deployment without 2nd-round development needed.

- Basic data and structures manipulations: create, update, retrieve, delete, list and search (CURDLS).

General Web Application Architecture  (GWA2) is a framework for web applications development. Its feathers include MVC-based, core-shared, clear and clean structures, quite fast new instances deployment and easy kick-start. GWA2 uses Smarty  as its default template engine. 

gMIS is a new and generally-targeted kind of MIS. It is a GWA2-based web application and has following characteristics:

- For general purpose, no user data involved in codes.

- XML configurations.

- Run immediately on connection to databases.

- 	Ajax-enabled, i.e. GTAjax .

- 	Inline editing of user data.

- 	Customized input and output, e.g. WYSWYG.

-	Strong searching, i.e. innovative page navigator.  

- Addtional interesting functions

We explore gMIS in next sections in detail and explain what these items represent.


[Back top](/gmis/what-is-gmis)

[Previous](/gmis/index) .... [Next](./gmis/gmis-pros-cons)

[Back to Up](../index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjAwMTQ2NjkxOSwtMjY2NDc5NjUxLC0xMz
cyNjI5OTQzLC0xODcxOTIyNzM1LDExMjI0MjU0NTNdfQ==
-->