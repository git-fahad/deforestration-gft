## Visualization queries Grafana

#### I. Highest Loss-Threshold Combination for a state

```
SELECT 
    threshold,
    SUM(tc_loss_ha_2001 + tc_loss_ha_2002 + tc_loss_ha_2003 + tc_loss_ha_2004 + tc_loss_ha_2005 + tc_loss_ha_2006 + tc_loss_ha_2007 + tc_loss_ha_2008 + tc_loss_ha_2009 +tc_loss_ha_2011 + tc_loss_ha_2013 + tc_loss_ha_2014 + tc_loss_ha_2015 + tc_loss_ha_2016 + tc_loss_ha_2017 + tc_loss_ha_2018 + tc_loss_ha_2019 + tc_loss_ha_2020 + tc_loss_ha_2021 + tc_loss_ha_2022 + tc_loss_ha_2023 ) AS total_loss_ha
FROM deforestration_jk 
WHERE state = 'Jammu and Kashmir'
GROUP BY threshold
ORDER BY total_loss_ha DESC
```
  
#### II. Total Gain of Forest from 2000 to 2020 by Sate
  ```
  SELECT 
    state,
    SUM(gain_2000-2020_ha) AS total_gain_ha
FROM deforestration_jk
GROUP BY state
ORDER BY total_gain_ha DESC;
```

### III. Annual deforestation Loss for each state
```
SELECT
    state,
    '2001' AS year,
    SUM(tc_loss_ha_2001) AS loss_ha 
FROM deforestration_jk 
GROUP BY state

UNION ALL

SELECT 
    state,
    '2002' AS year,
    SUM(tc_loss_ha_2002) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2003' AS year,
    SUM(tc_loss_ha_2003) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2004' AS year,
    SUM(tc_loss_ha_2004) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2005' AS year,
    SUM(tc_loss_ha_2005) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2006' AS year,
    SUM(tc_loss_ha_2006) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2007' AS year,
    SUM(tc_loss_ha_2007) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2008' AS year,
    SUM(tc_loss_ha_2008) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2009' AS year,
    SUM(tc_loss_ha_2009) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2010' AS year,
    SUM(tc_loss_ha_2010) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2012' AS year,
    SUM(tc_loss_ha_2012) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2013' AS year,
    SUM(tc_loss_ha_2013) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2014' AS year,
    SUM(tc_loss_ha_2014) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2015' AS year,
    SUM(tc_loss_ha_2015) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2016' AS year,
    SUM(tc_loss_ha_2016) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2017' AS year,
    SUM(tc_loss_ha_2017) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2018' AS year,
    SUM(tc_loss_ha_2018) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2019' AS year,
    SUM(tc_loss_ha_2019) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2020' AS year,
    SUM(tc_loss_ha_2020) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2021' AS year,
    SUM(tc_loss_ha_2021) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2022' AS year,
    SUM(tc_loss_ha_2022) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

UNION ALL

SELECT 
    state,
    '2023' AS year,
    SUM(tc_loss_ha_2023) AS loss_ha 
FROM deforestration_jk 
GROUP BY state 

ORDER BY state, year;
```
