Hello 
Presentation for OUGN is available [here](Oracle_Goldengate_OUGN_2024_final2.pptx)
```
TERMINAL WINDOW #1

for i in {1..10000}
do
echo "Insert Data $i - `date +%d-%m-%Y-%H%M%S`"
sqlplus -s sys/Oracle_4U as sysdba<<EOF
set heading on feedback on;
alter session set container=pdb1;
insert into test_Ins(c1, c2, c3) values ($i, sysdate, 'Loop1');
commit;
EOF
done;

```
![Oracle DB](https://www.gravityer.com/_next/image?url=https%3A%2F%2Fvivid-cow-9924242169.media.strapiapp.com%2Foracle_database_18edd9bd15.jpg&w=1080&q=75)