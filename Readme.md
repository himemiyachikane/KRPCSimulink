# KRPC Simulink Wrapper

- dependencies:
  - KRPC(tested V0.4.8)
    - default parameter(IP 127.0.0.1 port 50000 for RPC,and 50001 for streaming)
  - python(tested 3.6.7)
  - Matlab(>= 2018B)
- function:
  - read data from KSP
    - data read:
      - KSP time
      - vehicle position,velocity,Quaternion(attitude)
      - both radar height and height above sea level are get.
    - simulink time is synchrorized with KSP
  - set engine thrust in KSP
    - the aircraft in KSP must have 4 engines
    - the order of engine thrust data can be get by run "KRPC{'engine_tags'}" in matlab command window when simulink sim is started, after you set the tag of your engines
- demo:
  - aircraft:Quad.craft
  - start flight in KSP,turn on the fuel battery,ignite 4 engines 
  - set Probodobodyne RoveMate as the control part if you have kerbonauts onboard.
  -  run the simulation
  - drone will take off,ascend to 250m ASL,move to the top of KSC,land and set throttle to 0%
  - Accelerate or rapid accelerate mode of simulink is strongly recommend.
  - if your computer is too slow,the drone may go haywire.