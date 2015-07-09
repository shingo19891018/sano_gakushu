# 佐野_学習Git

#!/bin/bash

DAYS=$1


echo " "

time awk '$10>=10000' /home/ec2-user/loglog/bm_site_log/access_log.${DAYS}* | awk '{print $10 $7}' | sort  | uniq -c | sort -r | head

echo " "
echo "+-------------------------------+"
echo "|                               | "
echo "     ACCESS COUNT!   ${RES}      "
echo "|                               | "
echo "+---\  /------------------------+"
echo "     \/"

echo " "
