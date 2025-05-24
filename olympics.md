## EDITS IN PHASE-4:
 1. Added attributes Address,Salary in Employee Table
 2. Removed Stastics Attribute from Sport Entity
 3. Removed Country Attribute  from Awards


## ORDER OF QUERIES EXECUTION

#### OPTION-1:
Input: Age = 30

```sql
SELECT * 
FROM SPORTSPEOPLE
WHERE TIMESTAMPDIFF(YEAR, DOB, CURDATE()) > %s;
```
#### OPTION-2:
Input: Country = India

```sql
SELECT Fname, Lname
FROM SPORTSPEOPLE
WHERE Country = %s;
```

#### OPTION-3:
Input: Country = USA

```sql
SELECT 
SP.Country,
COUNT(*) AS Total_Medals
FROM
AWARDS A
JOIN 
SECURED_BY SB ON A.AWsports_ID = SB.SEC_awssports_ID
JOIN 
SPORTSPEOPLE SP ON SB.SEC_sportspeople_ID = SP.Sportspeople_ID
WHERE 
SP.Country = %s
GROUP BY 
SP.Country;
```

#### OPTION-4:


```sql
SELECT Inventory_name,Type,Quantity,Status,Cost
FROM INVENTORY
WHERE Inventory_name LIKE '%ball%';
```
#### OPTION-5:
Input: Sex = F,Level = GOLD,Country = USA,Year = 2020

```sql
SELECT COUNT(DISTINCT sp.Sportspeople_ID) AS DistinctAthletes
FROM SECURED_BY sb
JOIN AWARDS aw ON sb.SEC_awssports_ID = aw.AWsports_ID
JOIN SPORTSPEOPLE sp ON sb.SEC_sportspeople_ID = sp.Sportspeople_ID
WHERE sp.Sex = %s
AND aw.Level = %s
AND aw.Year = %s
AND sp.Country = %s;
```
#### OPTION-6:
Input: Country  = USA,Sport = Swimming, Div = 400m Medley,Year = 2020

```sql
SELECT 
        A.Level AS Award_Level, 
        CONCAT(SP.Fname, ' ', SP.Lname) AS Athlete_Name, 
        A.Year AS Award_Year
FROM 
        AWARDS A
JOIN 
        SECURED_BY SB ON A.AWsports_ID = SB.SEC_awssports_ID
JOIN 
        SPORTSPEOPLE SP ON SB.SEC_sportspeople_ID = SP.Sportspeople_ID
JOIN 
        SPORTS S ON A.AWsports_ID = S.Sport_ID
WHERE 
        SP.Country = %s
        AND S.Sname = %s
        AND S.Division = %s
        AND A.Year = %s;
```
#### OPTION-7:
Input: Country = Ireland,Brand = Nike,Years = 2022,2024

```sql
SELECT COUNT(*)
FROM MADE_PURCHASES_FROM mpf
JOIN AUDIENCE aud ON mpf.MPF_ticket_ID = aud.Ticket_ID
JOIN BUSINESSES bus ON mpf.MPF_registration_ID = bus.Registration_ID
WHERE bus.Enterprise_name = %s
        AND aud.Country_of_origin = %s
        AND bus.Contract_year IN %s;
```
#### OPTION-8:
Input: ID=1, Name = Ramesh Narayan,Sex = M,DOB = 2006-10-12,Country = India

```sql
INSERT INTO AUDIENCE (Ticket_ID, Fname, Lname, Sex, DOB, Country_of_Origin)
VALUES (%s, %s, %s, %s, %s, %s);
```
#### OPTION-9:
Input: Inventory_Name=Boxing Gloves,Quantity = 17
```sql
UPDATE INVENTORY SET Quantity = %s WHERE Inventory_name = %s;
```
#### OPTION-10:
Input: Sport_Name = Boxing
```sql
DELETE FROM SPORTS WHERE Sname = %s;
```
