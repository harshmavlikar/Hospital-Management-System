CREATE TABLES

create table patients(
     id int Auto_increment primary key,
     name varchar(225) not null,
     age int not null,
     gender varchar(10) not null
     );


create table doctors
     (
     id int auto_increment primary key,
     name varchar(255) not null,
     specialization varchar(255) not null
     );



create table appointments(
     id int auto_increment primary key,
     patient_id int not null,
     doctors_id int not null,
     appointment_date date not null,
     foreign key(patient_id) references patients(id),
     foreign key(doctors_id) references doctors(id)
     );

insert into doctors(name, specialization) values("Harsh Mavlikar", "Physician");

insert into doctors(name, spec ialization) values("Tony Stark", "Nero-Surgeon");
