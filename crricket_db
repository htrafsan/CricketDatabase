use Final_ICC

create table country
(
c_name varchar(20),
membership varchar(20),
budget int,
no_of_std int,
constraint Country_name primary key(c_name),
)

create table Presedent
(
p_name varchar(30),
c_name varchar(20),
board_name varchar(20),
yr int,
constraint President_n primary key(p_name,yr),
foreign key(c_name) references country,
)

create table stadium
(
name varchar(40),
c_name varchar(20),
capacity int,
city varchar(20),
constraint Stadium_n primary key(name),
foreign key (c_name) references country,
)

create table umpire
(
id char(5),
name varchar(30),
c_name varchar(20),
salary int,
grade char(2),
constraint Umpire_id primary key (id),
foreign key(c_name) references country,
)

create table country_rank
(
name varchar(20),
odi_rank int,
test_rank int,
Ttwenty_rank int,
constraint C_rank primary key (name),
foreign key(name) references country,
)

create table commitee
(
M_name varchar(30),
c_name varchar(20),
deg varchar(30),
yr int,
constraint Committee primary key(M_name, c_name, deg, yr),
foreign key(c_name) references country,
)

create table Player
(
id char(5),
name varchar(25),
c_name varchar(20),
age int,
Birth_year int,
Rolee varchar(10),
bat_s varchar(30),
bowl_s varchar(30),
constraint Player_id primary key(id),
foreign key (c_name) references country,
)

create table player_rank
(
id char(5),
odi_position int,
test_position int,
TT_position int,
constraint PR_id primary key (id),
foreign key(id) references player,
)

create table player_career
(
id char(5),
match int,
total_run int ,
total_wk int,
debut int ,
constraint PC_id primary key (id),
foreign key(id) references player,
)

create table Event_o
(
event_name varchar (30),
yr int,
budget int,
winner_pb int,
runners_pb int,
constraint Event_year primary key (yr),
)

create table CT_event
(
yr int,
winner varchar (20),
runner_up varchar (20),
MOT varchar (30),
constraint CT_yr primary key (yr),
foreign key(yr) references Event_o,
)

create table Odi_event
(
yr int,
winner varchar (20),
runner_up varchar (20),
MOT varchar (30),
constraint odi_yr primary key (yr),
foreign key (yr) references Event_o,
)

create table Ttwenty_event
(
yr int,
winner varchar (20),
runner_up varchar (20),
MOT varchar (30),
constraint Tt_yr primary key (yr),
foreign key (yr) references Event_o,
)

bulk insert country
from 'F:\project\country.csv'
with (
rowterminator = '\n' ,
fieldterminator = ','
);

bulk insert [dbo].[Presedent]
from 'F:\project\president.csv'
with (
rowterminator ='\n',
fieldterminator = ','
);

bulk insert stadium
from 'F:\project\stadium.csv'
with (
rowterminator = '\n',
fieldterminator = ','
);

bulk insert [dbo].[umpire]
from 'F:\project\Umpire.csv'
with (
rowterminator ='\n',
fieldterminator = ','
);

bulk insert [dbo].[country_rank]
from 'F:\project\Country_rank.csv'
with (
rowterminator = '\n',
fieldterminator = ','
);

bulk insert [dbo].[commitee]
from 'F:\project\Committee.csv'
with (
rowterminator = '\n',
fieldterminator = ','
);

bulk insert [dbo].[Player]
from 'F:\project\Player.csv'
with (
rowterminator = '\n',
fieldterminator = ','
);

bulk insert [dbo].[player_career]
from 'F:\project\Career.csv'
with (
rowterminator='\n',
fieldterminator = ','
);

bulk insert [dbo].[player_rank]
from 'F:\project\Player_rank.csv'
with (
rowterminator = '\n',
fieldterminator = ','
);

bulk insert [dbo].[Event_o]
from 'F:\project\Event.csv'
with (
rowterminator = '\n',
fieldterminator = ','
);

bulk insert [dbo].[Ttwenty_event]
from 'F:\project\T20.csv'
with (
rowterminator ='\n',
fieldterminator = ','
);

bulk insert [dbo].[Odi_event]
from 'F:\project\Odi_Event.csv'
with (
rowterminator = '\n',
fieldterminator = ','
);

bulk insert [dbo].[CT_event]
from 'F:\project\CT_Event.csv'
with (
rowterminator = '\n',
fieldterminator = ','
);
