### Test pipeline

- make overlay env and clone repos  
1. cd ~/workspace/envset  
2. bash env\_oneclick/install\_navi\_motion\_env\_local.sh  

- motion version before refactor
1. navi is a little outdated for motion. please use navi master and motion 7164cd35625c33364914a22571d53aa71f1856a2
2. once centos8 port is done, I will fix navi to use motion master.

- run sample commands
1. cd ~/workspace/navi/motion/navistrat
2. conda activate navi\_motion\_env
3. ./dumperapp/build\_bazel.sh
4. ./pyrunner navistrat/krx\_lm/krx\_feed\_test.py (Note that it is python3.6. you may need pip install recordclass=0.5.0)
