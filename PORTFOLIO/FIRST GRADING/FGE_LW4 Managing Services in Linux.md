![image](https://github.com/user-attachments/assets/bfe5a948-f527-42ed-954b-6a4eea7125ea)


# SYSADM1 -- Managing Services in Linux

# Requirement: 

-   A virtual machine running Linux

![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image2.png)

Complete this lab as follows:

1.  Use the service --status-all command to list all active and inactive
    services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

  -----------------------------------------------------------------------
  **Active**                             **Inactive**
  -------------------------------------- --------------------------------
  alsa-utils                             bluetooth

  anacron                                console-setup.sh

  apparmor                               grub-common

  cron                                   keyboard-setup.sh

  cups                                   plymouth
  -----------------------------------------------------------------------

SS:

![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image3.png){width="3.337713254593176in"
height="2.2771926946631673in"}
![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image4.png){width="3.1651979440069993in"
height="2.221791338582677in"}

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd

![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image5.png){width="4.359946412948381in"
height="1.1875in"}

3.  Check the status of the Bluetooth service. What is its status?

Bluetooth.service is is still inactive because of an unmet condition

SS:
![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image6.png){width="7.027083333333334in"
height="1.2722222222222221in"}

4.  Check the status of the cups services. Since when was it running?

It was running since Thu 2024-09-12 09:07:01

SS:
![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image7.png){width="7.027083333333334in"
height="2.859722222222222in"}

5.  Stop cups services.

![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image8.png){width="7.027083333333334in"
height="1.1784722222222221in"}

6.  Verify if the service was stopped.

![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image9.png){width="7.027083333333334in"
height="3.2444444444444445in"}

7.  Restart the cups services

![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image10.png){width="6.105018591426072in"
height="0.635505249343832in"}

8.  Verify if the service was restarted.
    ![](vertopal_ed11f64eef7848a7b6f0b6ceee4a7140/media/image11.png){width="7.027083333333334in"
    height="3.0388888888888888in"}
