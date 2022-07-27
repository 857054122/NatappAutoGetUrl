# NatappAutoGetUrl


linuxshell脚本一键读取： string=$(awk -F: '/http/' log.txt )| echo ${string##*//}|awk 'BEGIN{FS="."}{print $1".natappfree.cc" }'
    //其中log.txt为natapp运行日志


windows mobaxterm
第一步：筛选出最后一行带natapp域名的数据
cat log.txt|grep natapp|sed 'N;D'
第二步：通过awk FS切词拼接
 cat log.txt|grep natapp|sed 'N;D'|awk 'BEGIN{FS="//"}{print $2 }'|awk 'BEGIN{FS="."}{print $1".natappfree.cc"}'
