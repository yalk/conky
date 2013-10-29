conky
=====
by chunkyhead


A basic conky top bar to display system stats

Conky is a system monitor widget.
The conky is configured for the following tasks:
1. Displaying current time and date
2. Uptime of the machine
3. Processor temperature (Configured especially for 1 core + 1 hyperthreaded)
4. RAM stats
5. /,/home/ stats
6. Traffic monitoring on network connection (LAN/Wi-Fi)
7. All this is displayed on the top of your screen

Note:
For conky to be able 
1. Run
      You need to first install the "conky-all" package which should be available on the official repositories of most of the Linux distributions
2. Detect temperature of CPU Cores
      A. Install "lm-sensors", should be available on the official repositories of most of the Linux distributions
      B. Run "cat /proc/cpuinfo" (without quotes) on the terminal to get details about your cores and accordingly add in .conkyrc file, add the temperature command (exec sensors | grep 'Core 0' | cut -c16-20) on as many real cores (eg Core0, Core1) as you have
          Note: "cut -c16-20" is to convert the temperate into 'C, if you want it in 'F, remove it
3. Monitoring network
    To monitor network you need to add corect interfaces to the commands run "iwconfig" or "ifconfig" depending on your Linux distribution and replace wlp6s0(wireless interface) and enp6s(ethernet interface) with the appropriate interface
    Eg. ${font}${color1}${upspeed wlp6s0} will become ${font}${color1}${upspeed wlan0}

You are free to modify this code, for details on more commands you can run refer: 
