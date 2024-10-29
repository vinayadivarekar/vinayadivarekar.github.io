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