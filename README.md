Mansi Three for Mi Note 10 Lite
==================================================
Basic   | Spec Sheet
-------:|:----------
CPU     | Qualcomm® Kryo™ 470, 8nm process
Frequency | Octa-core processor, up to 2.2 GHz
GPU     | Adreno™ 618 graphics processor up to 700 MHz
ROM     | 64GB/128GB UFS2.1 flash storage
RAM     | 6GB/8GB LPDDR4x
Android | Android 10
Battery | 5260 mAh (typ)*/ 5170mAh (min)
Display | 6.47″ 3D curved AMOLED display 2340 x 1080 FHD+, 398 PPI
Rear Camera  | Sony IMX686, 64MP, 0.8μm with 4-in-1 Super pixel, 1/1.73″, f/1.89 aperture
Front Camera | 16MP, 1.0μm, 1/3.06″, f/2.48 aperture

IMPORTANT HARDWARE INFORMATION
==================================================
|Hardware | Information |
--------:|:--------------
Flash    | 
LCD      | 
TouchPanel | 
Fingerprint | 
Camera_Main | 
Camera_Sub | 
Camera_Front | 
Audio | 
Accelerometer | 
Alsps    | 
Gyroscope| 
Magnetometer| 

BUILD KERNEL INFORMATION
==================================================
1. Configure
    
		repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-10.0-WIP
		repo sync

2. Then add these projects to .repo/manifest.xml
    
		<project path="device/xiaomi/toco" name="slfl/android_device_xiaomi_toco" remote="github" revision="master" />

3. Build Three
    
		. build/envsetup.sh
		lunch omni_tucana-eng
		mka recoveryimage ALLOW_MISSING_DEPENDENCIES=true # Only if you use minimal twrp tree.
    
4. Flash(boot) recovery
    fastboot boot out/target/product/toco/recovery.img

4. Rebot phone and use new kernel
