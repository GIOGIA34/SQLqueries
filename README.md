# SQLqueries
SELECT E.customer_id, D.country, C.City, A.first_name, A.last_name,
SUM(amount)AS Total_Amount_Paid
FROM customer Z
INNNER JOIN addres B ON A.address_id=B.address_id
INNER JOIN city C ON  B.city_id=C.city_id
INNER JOIN country D ON C.country_id=D.country_id
INNER JOIN payment E ON A.customer_id=E.customer_id
WHERE D.country IN ("India, 'CHina', "UNited States', 'Japan, 'Mexico', 'Brazil')
AND city IN (Aurora, 'ACua', "Citrus Heights', 'Iwaki', "Ambatur')
GROUP BY D.country, C.city, A.firt_name, A.last_name, E.customer_id
ORDER BY Total_Amount-Paid desc
LIMIT 5

