# NatappAutoGetUrl


linuxshell脚本一键读取： string=$(awk -F: '/http/' log.txt )| echo ${string##*//}|awk 'BEGIN{FS="."}{print $1 }'      //其中log.txt为natapp运行日志
