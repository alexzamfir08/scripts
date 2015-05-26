MAX=95
EMAIL=alex.z@insxcloud.com
PART=sda1
HOST=hostname
USE=`df -h |grep $PART | awk '{ print $5 }' | cut -d'%' -f1`
if [ $USE -gt $MAX ]; then
  echo "Percent used: $USE" | mail -s "Running out of disk space on $HOST" $EMAIL
fi
