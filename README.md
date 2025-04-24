# dai-task3
#using a database named billionaires
SELECT * FROM billionaires;
#if only want  to see a person's name and networth
SELECT personname,finalworth FROM billionares;
#we wanna findout all the countries in the list
SELECT * FROM billionaires;
#there are many repeated countries function to find unique ones
SELECT DISTINCT countries FROM billionaires;
#calculate number of unnique countries
SELECT COUNT(DISTINCT countries) FROM billionaires;
#how many people are in the list
SELECT COUNT(DISTINCT personname) FROM billionaires;
#average networth of this list
SELECT AVG(finalworth) FROM billionaires;
#list the richest people in france but not from paris
SELECT * FROM billionaires
 WHERE country = 'france' AND city <> 'paris';
 #prople from france or spain
 SELECT * FROM billionaires;
 WHERE country = 'france' OR country = 'spain';
 #using IN 
 SELECT * FROM billionaires;
 WHERE country IN('france','spain','italy');
#how many are selfmade
SELECT COUNT(personname) FROM billionaires;
WHERE selfmadde = 'true';
#find the number of billionaires by industry
SELECT industries, COUNT(personname) AS billionaire_count FROM billionaires
GROUP BY industries
ORDER BY COUNT(personname) DESC;
#list the number of toop 10
SELECT industries, COUNT(personname) AS billionaire_count FROM billionaires
GROUP BY industries
ORDER BY COUNT(personname) DESC
LIMIT 10;
#list the number of billioanires by birth month
SSELCT birth month,COUNT(personname) FROM billionaires
GROUP BY birthmonth
ORDER BY COUNT(personname) DESC;
