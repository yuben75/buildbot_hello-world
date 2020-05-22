# hello-world
hello world project for buildbot tutorials

###############################################
docker run -it -p 8010:8010 -p 9989:9989 -p 443:443 -p 80:80 buildbot/buildbot-master:v2.7.0 /bin/sh
###############################################
buildbot create-master master
cp ./master/master.cfg.sample  ./master/master.cfg
buildbot start master
###############################################

#buildbot-worker create-worker worker 192.168.1.111:9989 example-worker pass
buildbot-worker create-worker worker localhost example-worker pass
buildbot-worker start worker


###############################################
buildbot reconfig master


#docker cp ./master.cfg id:/var/lib/buildbot
#
