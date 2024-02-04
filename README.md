### DigiPi

Autio: IQaudiO - Pi-codecZero

- SD Card PiOS Lite with desktop
- VNC + I2C
- /boot/config.txt ->
    framebuffer_width=1024
    framebuffer_height=768
    hdmi_force_hotplug=1
    hdmi_group=2
    hdmi_mode=16
    #dtparam=audio=on          # disable the Pi’s on-board sound card.
    dtoverlay=rpi-codeczero    # Configuring Linux for the IQaudio sound card
    #dtoverlay=vc4-kms-v3d
    #max_framebuffers=2

- Codec Zero Configuration:
    (https://github.com/iqaudio/Pi-Codec)
    -> https://www.raspberrypi.com/documentation/accessories/audio.html#raspberry-pi-codec-zero
    $ sudo alsactl restore -f ~/Documents/Pi-Codec/Codec_Zero_AUXIN_record_and_HP_playback.state
    $ sudo nano /etc/rc.local
    ADD -> sudo alsactl restore -f ~/Documents/Pi-Codec/Codec_Zero_AUXIN_record_and_HP_playback.state

