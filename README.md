# AI_ML_pipeLine
## Lab 1
1. pip3 install -U TWCC-CLI
2. twccli config init
3. export LANG=C.UTF-8
4. export LC_ALL=C.UTF-8
5. export PYTHONIOENCODING=UTF-8
6. cd .twcc_data/
7. cat credential
8. cat resources
9. cd
10. rm -rf .twcc_data/
11. twccli config init
12. export LANG=C.UTF-8
13. export LC_ALL=C.UTF-8
14. export PYTHONIOENCODING=UTF-8
## Lab 2
1. twccli ls vcs
2. twccli ls vcs -ptype
3. twccli mk key -n $KEY_NAME
4. twccli mk vcs -key $KEY_NAME -n $VCS_NAME
5. twccli ls vcs
6. twccli net vcs -s $VCS_ID -fip 
7. twccli ls vcs
8. twccli rm vcs -f -s $VCS_ID
9. twccli ls ccs -itype
10. twccli ls ccs -img
11. twccli mk ccs -gpu 1
12. twccli rm ccs -f -s $CCS_ID
## Lab 3
1. twccli mk ccs -gpu 1 -n $CCS_NAME
2. twccli ls ccs -s $CCS_ID -gssh
3. ssh $USER_NAME @ $DEST_IP –p
4. git clone https://github.com/wilicc/gpu-burn.git
5. cd gpu-burn
6. make
7. exit
## Lab 4
1. ssh-keygen -t rsa -n 4096
2. ssh-copy-id `twccli ls ccs -s $CCS_ID -gssh`
3. ssh `twccli ls ccs -s $CCS_ID -gssh`
4. ssh `twccli ls ccs -s $CCS_ID -gssh` `nvidia-smi`
## Lab 5
1. sudo apt install jp
2. twccli ls key -json | jq '.[].name '| paste -sd " " -
3. twccli ls ccs -s $CCS_ID -p -json | jq"."
4. twccli net ccs -s $CCS_ID -p 5000 -open
5. twccli ls ccs -s $CCS_ID -p -json | jq"."
6. twccli ls ccs -s $CCS_ID -p -json | jq ".[] | select (.target_port| contains(5000) ) "
## Lab 6
1. wget https://gist.githubusercontent.com/NCHC-Oliver/2b95ea9d2530d3a4048a69245a10ae03/raw/b6ba6cf0516daa3c1b8973c1a39fb78908f4474c/TWCC_IaC.sh
2. bash TWCC_LaC.sh 
