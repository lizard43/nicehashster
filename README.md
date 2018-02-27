# nicehashster
Monitor NiceHash Excavator and display stats on rig OLED

# General JSON
This is a few of the chnages that I makes the the NHM2 general config file that is located in:

C:\Users\youruser\AppData\Roaming\nhm2\configs

- Enable the web API
    - "ExcavatorExtraStartupParameters": "-wp 8080 -wi 0.0.0.0"
- Disable AMD detection (I only have NVidia in my rig)
    - "DisableDetectionAMD": true
- Switch profitability threshold. Too low and you'll churn the miner. Too high, you risk getting stuck on a low paying job. 0.03 seems to be a sweet spot for my rig
    - "SwitchProfitabilityThreshold": 0.03
- Put cards in P0 performance state. 
    - "NVIDIAP0State": true
    - Not all cards support this mode. Check state with
        - nvidia-smi -q -d PERFORMANCE
