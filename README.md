###<strong>Ansible playbook to restore a table from a gzipped MySQL dump file using http://www.tsheets.com/downloads/oss/extract_sql.pl </strong> 

***
<strong>Usage:</strong> <br />
ansible-playbook -i inventory restore_table.yml <br />
ansible-playbook restore_table.yml --extra-vars='db_backup=/root/test.sql.gz table=test_table db_name=new_test working_dir=/root/test table_new=test_new timeout=3600' <br />
***

<strong>Explanation for each variable:</strong>

db_backup ==> Full path to gzip file. <br /> 
table ==> Table to extract. <br />
table_new ==> Use this if you want to restore into a new table. <br />
db_name ==> Database to use for restoring the table. Can be same. <br />
backup:yes ==> Will dump the database before restoring the table. <br />
timeout ==> async value for longer tasks. Default value 1800 seconds. <br />

