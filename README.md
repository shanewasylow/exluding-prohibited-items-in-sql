# exluding-prohibited-items-in-sql
SQL scripts to exclude prohibited items from the website

--Excluding items based on their category
SELECT *
FROM items
WHERE country IN ('DE', 'UK')
    AND category NOT IN (
        'medications_prescription',
        'dangerous_items'
    );

--Excluding items based on their name
SELECT *
FROM items
WHERE country IN ('DE', 'UK')
    AND name NOT LIKE '%ninja%'
    AND name NOT LIKE '%daggers%';
