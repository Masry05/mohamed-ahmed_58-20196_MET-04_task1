# Task 1 — Inconsistencies and duplicates

**Name:** Mohamed Ahmed Mohamed Abdelaziz  
**ID:** 58-20196  
**Major:** MET  
**Lab:** 04

I started with 39 signup rows and inspected their value counts and data types before changing anything. Faculty, city, and club labels had different cases, abbreviations, and alternative names; I stripped spaces, ignored case, and used explicit dictionaries to map every variant to the required canonical value, then asserted that only those values remained. I collapsed extra spaces in names and used consistent title case, while trimming and lowercasing emails. I mapped the different yes/no fee entries to booleans and parsed both timestamp formats, treating slash-separated dates as day/month/year. After these fixes, I found and removed 3 identical rows, leaving 36. The other repeated student–club entries were separate submissions that showed signup history, often with an updated fee status. The assignment asks for one final row per student and club, so I kept the latest submission, removing 4 earlier entries and leaving 32 rows. The order matters: if I did this before fixing club spellings, I would find only 2 repeated student–club rows after the 3 exact copies, temporarily leaving 34 rows and missing 2 repeats. Two students named Mohamed Adel have different IDs (55-2992 and 61-4844), so using student ID with club as the key keeps them separate.
