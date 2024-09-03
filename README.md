# Домашнее задание к занятию 14 «Средство визуализации Grafana»

1. ![image](https://github.com/user-attachments/assets/9207b1b1-6914-4e7a-a954-2f9d5748a607)

2.
  - утилизация CPU для nodeexporter (в процентах, 100-idle);
  ```
  100 - (rate(node_cpu_seconds_total{cpu="0", job="nodeexporter", mode="idle"}[1m]) * 100)
  100 - (rate(node_cpu_seconds_total{cpu="1", job="nodeexporter", mode="idle"}[1m]) * 100)
  ```
  - CPULA 1/5/15;
  ```
  node_load1
  node_load5
  node_load15
  ```
  - количество свободной оперативной памяти;
  `node_memory_MemFree_bytes`
  - количество места на файловой системе.
  `node_filesystem_free_bytes{mountpoint="/"}`
  - Скрин дашборда
  - 
![image](https://github.com/user-attachments/assets/f1f07129-5fea-4db1-93be-69a956645ecb)

3. Алерт в CPULA не виден, так как загрузка ЦПУ очень мала и он выходит за рамки оси, выставлен в 80%
   ![image](https://github.com/user-attachments/assets/4991cb5b-f893-4f57-aad0-c4a30725cec2)

4. [dashboard.json](https://github.com/Shchu4ka/monitoring2/blob/main/dashboard.json)
