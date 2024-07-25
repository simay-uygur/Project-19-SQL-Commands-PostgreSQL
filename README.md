# Project-19-SQL-Commands-PostgreSQL
These are assignments given in Patika Java Intermediate course.


## Tasks
- Write a LEFT JOIN query to see the city names from the city table and country names from the country table together.

- Write a RIGHT JOIN query to see the payment_id from the payment table and first_name and last_name from the customer table together.

- Write a FULL JOIN query to see the rental_id from the rental table and first_name and last_name from the customer table together.

## Queries

```sql
-- Task 1
SELECT city.city, country.country FROM city
LEFT JOIN country ON city.country_id = country.country_id;

-- OR THE SAME RESULT CAN BE ACHIEVED BY:
SELECT city.city, country.country FROM country
LEFT JOIN city ON city.country_id = country.country_id;

-- Task 2
SELECT customer.first_name, customer.last_name, payment.payment_id FROM customer
RIGHT JOIN payment ON customer.customer_id = payment.customer_id;

-- FROM THE RESULTS ALL CUSTOMERS HAVE A PAYMENT (NO NULL VALUE IN THE BELOW QUERIE'S TABLE)
SELECT customer.first_name, customer.last_name, payment.payment_id FROM payment
RIGHT JOIN customer ON customer.customer_id = payment.customer_id;

-- Task 3
SELECT customer.first_name, customer.last_name, rental.rental_id FROM customer
FULL JOIN rental ON rental.customer_id = customer.customer_id;
-- THERE IS NO NULL VALUE THEREFORE EVERY CUSTOMER HAS A RENTAL

```

## Tables

### TABLE 1
```
city country
A Corua (La Corua) Spain
Abha Saudi Arabia
Abu Dhabi United Arab Emirates
Acua Mexico
Adana Turkey
Addis Abeba Ethiopia
Aden Yemen
Adoni India
Ahmadnagar India
Akishima Japan
Akron United States
al-Ayn United Arab Emirates
al-Hawiya Saudi Arabia
al-Manama Bahrain
al-Qadarif Sudan
al-Qatif Saudi Arabia
Alessandria Italy
Allappuzha (Alleppey) India
Allende Mexico
Almirante Brown Argentina
Alvorada Brazil
Ambattur India
Amersfoort Netherlands
Amroha India
Angra dos Reis Brazil
Anpolis Brazil
Antofagasta Chile
Aparecida de Goinia Brazil
Apeldoorn Netherlands
Araatuba Brazil
Arak Iran
Arecibo Puerto Rico
Arlington United States
Ashdod Israel
Ashgabat Turkmenistan
Ashqelon Israel
Asuncin Paraguay
Athenai Greece
Atinsk Russian Federation
Atlixco Mexico
Augusta-Richmond County United States
Aurora United States
Avellaneda Argentina
Bag Brazil
Baha Blanca Argentina
Baicheng China
Baiyin China
Baku Azerbaijan
Balaiha Russian Federation
Balikesir Turkey
Balurghat India
Bamenda Cameroon
Bandar Seri Begawan Brunei
Banjul Gambia
Barcelona Venezuela
Basel Switzerland
Bat Yam Israel
Batman Turkey
Batna Algeria
Battambang Cambodia
Baybay Philippines
Bayugan Philippines
Bchar Algeria
Beira Mozambique
Bellevue United States
Belm Brazil
Benguela Angola
Beni-Mellal Morocco
Benin City Nigeria
Bergamo Italy
Berhampore (Baharampur) India
Bern Switzerland
Bhavnagar India
Bhilwara India
Bhimavaram India
Bhopal India
Bhusawal India
Bijapur India
Bilbays Egypt
Binzhou China
Birgunj Nepal
Bislig Philippines
Blumenau Brazil
Boa Vista Brazil
Boksburg South Africa
Botosani Romania
Botshabelo South Africa
Bradford United Kingdom
Braslia Brazil
Bratislava Slovakia
Brescia Italy
Brest France
Brindisi Italy
Brockton United States
Bucuresti Romania
Buenaventura Colombia
Bydgoszcz Poland
Cabuyao Philippines
Callao Peru
Cam Ranh Vietnam
```


### TABLE 2

```
first_name last_name payment_id
Peter Menard 17503
Peter Menard 17504
Peter Menard 17505
Peter Menard 17506
Peter Menard 17507
Peter Menard 17508
Harold Martino 17509
Harold Martino 17510
Harold Martino 17511
Douglas Graf 17512
Douglas Graf 17513
Douglas Graf 17514
Douglas Graf 17515
Douglas Graf 17516
Douglas Graf 17517
Douglas Graf 17518
Henry Billingsley 17519
Henry Billingsley 17520
Henry Billingsley 17521
Carl Artis 17522
Carl Artis 17523
Carl Artis 17524
Carl Artis 17525
Arthur Simpkins 17526
Arthur Simpkins 17527
Arthur Simpkins 17528
Ryan Salisbury 17529
Ryan Salisbury 17530
Ryan Salisbury 17531
Ryan Salisbury 17532
Ryan Salisbury 17533
Roger Quintanilla 17534
Roger Quintanilla 17535
Roger Quintanilla 17536
Joe Gilliland 17537
Joe Gilliland 17538
Joe Gilliland 17539
Joe Gilliland 17540
Juan Fraley 17541
Juan Fraley 17542
Juan Fraley 17543
Juan Fraley 17544
Jack Foust 17545
Jack Foust 17546
Jack Foust 17547
Albert Crouse 17548
Albert Crouse 17549
Albert Crouse 17550
Albert Crouse 17551
Albert Crouse 17552
Jonathan Scarborough 17553
Jonathan Scarborough 17554
Jonathan Scarborough 17555
Justin Ngo 17556
Justin Ngo 17557
Justin Ngo 17558
Justin Ngo 17559
Terry Grissom 17560
Terry Grissom 17561
Gerald Fultz 17562
Gerald Fultz 17563
Gerald Fultz 17564
Keith Rico 17565
Keith Rico 17566
Keith Rico 17567
Keith Rico 17568
Samuel Marlow 17569
Samuel Marlow 17570
Samuel Marlow 17571
Samuel Marlow 17572
Samuel Marlow 17573
Samuel Marlow 17574
Willie Markham 17575
Willie Markham 17576
Willie Markham 17577
Willie Markham 17578
Ralph Madrigal 17579
Ralph Madrigal 17580
Ralph Madrigal 17581
Ralph Madrigal 17582
Lawrence Lawton 17583
Lawrence Lawton 17584
Lawrence Lawton 17585
Lawrence Lawton 17586
Nicholas Barfield 17587
Nicholas Barfield 17588
Nicholas Barfield 17589
Nicholas Barfield 17590
Nicholas Barfield 17591
Roy Whiting 17592
Roy Whiting 17593
Roy Whiting 17594
Roy Whiting 17595
Roy Whiting 17596
Benjamin Varney 17597
Benjamin Varney 17598
Benjamin Varney 17599
Benjamin Varney 17600
Benjamin Varney 17601
Bruce Schwarz 17602

```

### TABLE 3
```
first_name last_name rental_id
Tommy Collazo 2
Manuel Murrell 3
Andrew Purdy 4
Delores Hansen 5
Nelson Christenson 6
Cassandra Walters 7
Minnie Romero 8
Ellen Simpson 9
Danny Isom 10
April Burns 11
Deanna Byrd 12
Raymond Mcwhorter 13
Theodore Culp 14
Ronald Weiner 15
Steven Curley 16
Isaac Oglesby 17
Ruth Martinez 18
Ronnie Ricketts 19
Roberta Harper 20
Craig Morrell 21
Raul Fortier 22
Barry Lovelace 23
Juan Fraley 24
Pamela Baker 25
Billy Poulin 26
Robert Baughman 27
Constance Reid 28
Marie Turner 29
Ray Houle 30
Fred Wheat 31
Joy George 32
Kay Caldwell 33
Freddie Duggan 34
Roberto Vu 35
Bonnie Hughes 36
Javier Elrod 37
Michael Silverman 38
Gertrude Castillo 39
Marvin Yee 40
Yvonne Watkins 41
Harvey Guajardo 42
Neil Renner 43
Gertrude Castillo 44
Troy Quigley 45
Maria Miller 46
Virginia Green 47
Jenny Castro 48
Gene Sanborn 49
Carol Garcia 50
Mabel Holland 51
Edgar Rhoads 52
Dave Gardiner 53
Toni Holt 54
Monica Hicks 55
Chester Benner 56
Jennifer Davis 57
Matthew Mahan 58
Manuel Murrell 59
Gordon Allard 60
Jo Fowler 61
Chad Carbone 62
Martin Bales 63
Harry Arce 64
Arthur Simpkins 65
Jacqueline Long 66
Sherry Marshall 67
Sylvia Ortiz 68
Richard Mccrary 69
Beverly Brooks 70
Robin Hayes 71
Ann Evans 72
Clarence Gamez 73
Jennie Terry 74
Ben Easter 75
Mary Smith 76
Jim Rea 77
Juanita Mason 78
Courtney Day 79
George Linton 80
Velma Lucas 81
Jesus Mccartney 82
Monica Hicks 83
Lester Kraus 84
Vincent Ralston 85
Nora Herrera 86
Eric Robert 87
Heather Morris 88
Marc Outlaw 89
Deborah Walker 90
Margie Wade 91
Michael Silverman 92
Bobbie Craig 93
Sue Peters 94
Bryan Hardison 95
Joyce Edwards 96
Hilda Hopkins 97
Cassandra Walters 98
Marie Turner 99
Lucy Wheeler 100
Tim Cary 101
```

