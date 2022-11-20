for i in `seq 1 100000`; \
do s=`date "+%Y-%m-%d %H:%M:%S"`; \
sa=`curl -s -w "%{http_code}"  http://userfinance-internal.liveme-finance-ekslivemefinance-microfinance-41901:8888`; \
echo $s $sa; done

curl userfinance-internal.liveme-finance-ekslivemefinance-microfinance-41901:8888