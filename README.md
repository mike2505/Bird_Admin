# Bird_Admin
Most popular scroll application vulnerability.
acces to admin menu + visualy changing balance.
possible lfi&rci (2L2C) .
changing config.

## Requirements

1. Rooted Android device with gapps 
2. Burpsuite
3. Bird Application

## Installing lsposed & SSLunpinning

1. Open Magisk and go to modules
2. Search for Riru - LSPosed, Install it.

![image](https://user-images.githubusercontent.com/37780087/192861656-12d7bf78-f3ec-4e96-889f-9380e03c8d26.png)

3. Download LSPosed app from [google play](https://play.google.com/store/apps/details?id=org.lsposed.manager&hl=en_US&gl=US)
4. Open LSPosed, go to repository and search for SSLUnpining, Click on it
5. Go TO releases, Click on Assets and then on app-release.apk

![image](https://user-images.githubusercontent.com/37780087/192861831-1a246e66-0fa5-4053-a38e-a81e11d409af.png)

6. Download and install it.
7. Go again to LSPosed - modules - SSLUnpining
8. Search for bird and enable it

## Configuring Burpsuite

1. Open burpsuite and go to proxy
2. Click on Options anmd look at Proxy Listeners
3. Click Add
4. Bind to port: 8383 | Bind to address: All interfaces

![image](https://user-images.githubusercontent.com/37780087/192862004-61094279-a445-445b-8189-6fd09f02cbcd.png)

5. Click ok and done

## Enabling proxy on wifi

[!] Note: You must be on the same wifi as pc
 
### Check ip of pc

1. Open terminal on your computer
2. Type ip a and look at your ip

### Enabling proxy

1. While connecting to wifi press advanced options
2. Look for proxy and change from None to Manual
3. Enter your ip as Proxy hostname and 8383 as Proxy port
4. Click Save

## False2True :D

Okay, now we are ready to start.


1. Open bird application and start intercepting.
2. Click on side menu and go to settings.
3. Forward all requests until you see /user
4. Right click - do intercept - response to this request
5. Forward again until you see response from this request :D
6. Change everything from false to true

yuhu now you have access to the admin menu

![image](https://user-images.githubusercontent.com/37780087/192862411-8d1c33af-565c-4f01-96a4-d31fdb25c61e.png)
