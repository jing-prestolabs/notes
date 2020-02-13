### Test pipeline

- make overlay env and clone repos
 cd ~/workspace/envset
 bash env_oneclick/install_navi_motion_env_local.sh
- motion version before refactor
 navi is a little outdated for motion. please use navi master and motion 7164cd35625c33364914a22571d53aa71f1856a2
 once centos8 port is done, I will fix navi to use motion master.
- run sample commands
 cd ~/workspace/navi/motion/navistrat
 conda activate navi_motion_env
 ./dumperapp/build_bazel.sh
 ./pyrunner navistrat/krx_lm/krx_feed_test.py
 Note that it is python3.6. you may need pip install recordclass=0.5.0
