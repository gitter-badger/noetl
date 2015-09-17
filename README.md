# noetl
NoETL (Not Only ETL) is a prototype of a system to manage the sequence of the process execution by controlling forks and child processes. 

Functionality is described on wiki - https://github.com/akuksin/noetl/wiki

To execute the process assuming you've just cloned the repo to ~/projects/github folder, simply run:

python ~/projects/github/noetl/noetl/noetl.py ~/projects/github/noetl/conf/coursor.inherit.cfg.v1.json

An output of execution should be:

2011-09-16 16:31:03.419073  - INFO -  Configuration file is:  ~/projects/github/noetl/conf/coursor.inherit.cfg.v1.json
2011-09-16 16:31:03.419024  - INFO -  LogFile /tmp/log/noetl-20150916163103.log
TestIt is True
2011-09-16 16:31:03.419024  - INFO -  LogFile /tmp/log/noetl-20150916163103.log
step1 : ls -ltr /tmp
step1 : echo '~/projects/github/noetl'
step2 : echo "Cursor 201109" > /tmp/201109.test
step2 : echo "Cursor 201110" > /tmp/201110.test
step2 : echo "Cursor 201111" > /tmp/201111.test
step3 : ls -ltr /tmp/201109.test
step3 : ls -ltr /tmp/201110.test
step3 : ls -ltr /tmp/201111.test
step3 : ls -ltr /tmp/201112.test
step4 : rm /tmp/201109.test
step4 : rm /tmp/201110.test
step4 : rm /tmp/201111.test
step4 : rm /tmp/201112.test
step5 : ls -ltr /tmp/201112.test
Done Testing
