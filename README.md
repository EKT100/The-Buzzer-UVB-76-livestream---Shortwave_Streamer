# The-Buzzer-UVB-76-livestream - Shortwave_Streamer
This repository is mainly for The Buzzer/UVB-76 YouTube livestream. It contains a KiwiSDR autoreloader to prevent timeouts. Attached are 2 files: kiwi-reload (versions 7.2.0-8.0.1) and autoreload (versions 3.5-3.7). 

How to use kiwi-reload
1. Download "kiwi-reload Shortwave_Streamer.zip" file
2. Go into File Explorer and find the file you just downloaded
3. Once found, right-click the folder and choose "Extract All..."
4. Once extracted, open the file to "8.0.1 (experimental)"
5. Double-click the "kiwireload-version-8.0.1-experimental.exe" Application
6. If you get a blue popup window saying "Windows protected your PC" Click the 'More info" button down below
7. And click the "Run anyway" button right next to the "Don't run" button
8. Command Prompt will open and give it a few seconds to do it's thing and it will have text saying:
9. 2026-10-03 15:57:23,560 [INFO] No receivers on file, importing the built-in default list...
2026-10-03 15:57:24,132 [INFO] Imported 18 receiver(s) from the built-in default list
2026-10-03 15:57:24,133 [INFO] The Receiver is at: http://127.0.0.1:5000
2026-10-03 15:57:24,134 [INFO] Configure these Settings at: http://127.0.0.1:5001
 * Serving Flask app 'kiwireload_viewer'
 * Debug mode: off
 * Serving Flask app 'kiwireload_settings'
 * Debug mode: off
2026-10-03 15:57:24,146 [INFO] ←[31m←[1mWARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.←[0m
 * Running on all addresses (0.0.0.0)
 * Running on http://xxx.x.x.x:5001
 * Running on http://xxx.xxx.x.xxx:5001
2026-10-03 15:57:24,147 [INFO] ←[33mPress CTRL+C to quit←[0m
2026-10-03 15:57:24,147 [INFO] ←[31m←[1mWARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.←[0m
 * Running on all addresses (0.0.0.0)
 * Running on http://xxx.0.0.x:5000
 * Running on http://xxx.xxx.x.xxx:5000
2026-10-03 15:57:24,147 [INFO] ←[33mPress CTRL+C to quit←[0m
   9. After that, look carefully in Command Prompt and you will find 4 IPv4 addresses
   10. At this line: 2026-10-03 15:57:24,146 [INFO] ←[31m←[1mWARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.←[0m
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5001
 * Running on http://192.168.1.120:5001
 * 11. Highlight the 1st IPv4 address "http://127.0.0.1:5001" this is the link to go into the kiwi-reloader settings where you can tweak a bunch of settings to your desires
   12. Press Control + C to copy the IPv4 address and then go into your browser and type: 'FireFox download" and click the 1st option (FireFox is recommended for this)
   13. Once FireFox downloaded, Install it and go through it's setup process.
   14. Once the setup is done, go to the address bar at the top and press Control + V to paste the IPv4 Address and hit Enter
   15. This is the kiwi-reloader settings where you can tweak a bunch of stuff to match your desires. At the bottom of the "tuning & Timing" section, there is a setting called "Max session length (min)" in the box next to it there is a number 14 which means that every 14 minutes, the kiwi-reloader switches to a different SDR to prevent timeout (which is 30 minutes every 24 hours have passed)
   16. Delete that number and put "28" in there so you're not wasting the extra 16 minutes the SDR has until timeout
   17. Then, click the blue button down below called "Save Settings"
   18. Next, create a new tab and in the address bar type: "about:config" you will be directed to a window called "Proceed with Caution" and press the button "Accept the Risk and Continue"
   19. Type "media.autoplay.default" and change it's value from 1 to 0
   20. Finally, go back into Command Prompt and look for the 2nd pair of IPv4 Addresses and highlight the 1st one, copy it, and then go back into FireFox and then in the address bar paste the IPv4 address hit enter and there you go! you Successfully have kiwi-reloader!
