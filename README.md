## Add this line to your manifest ROM before ```repo sync```:

Sepolicy line:
```
  <project path="device/qcom/sepolicy_vndr/sm6225" name="SM6225-Devs-ID/device_qcom_sepolicy_vndr" remote="github" revision="14-caf-sm6225" />
```
hardware/qcom-caf/common line:
```
    <linkfile src="os_pickup_audio-ar.mk" dest="hardware/qcom-caf/sm6225/audio/Android.mk" />
    <linkfile src="os_pickup_qssi.bp" dest="hardware/qcom-caf/sm6225/Android.bp" />
    <linkfile src="os_pickup.mk" dest="hardware/qcom-caf/sm6225/Android.mk" />
```

HALs line:
```
  <project path="hardware/qcom-caf/sm6225/audio/agm" name="SM6225-Devs-ID/vendor_qcom_opensource_agm" remote="github" revision="14-caf-sm6225" />
  <project path="hardware/qcom-caf/sm6225/audio/pal" name="SM6225-Devs-ID/vendor_qcom_opensource_arpal" remote="github" revision="14-caf-sm6225" />
  <project path="hardware/qcom-caf/sm6225/audio/primary-hal" name="SM6225-Devs-ID/hardware_qcom_audio" remote="github" revision="14-caf-sm6225" />
  <project path="hardware/qcom-caf/sm6225/data-ipa-cfg-mgr" name="SM6225-Devs-ID/vendor_qcom_opensource_data-ipa-cfg-mgr" remote="github" revision="14-caf-sm6225" />
  <project path="hardware/qcom-caf/sm6225/dataipa" name="SM6225-Devs-ID/vendor_qcom_opensource_dataipa" remote="github" revision="14-caf-sm6225" />
  <project path="hardware/qcom-caf/sm6225/display" name="SM6225-Devs-ID/hardware_qcom_display" remote="github" revision="14-caf-sm6225" />
  <project path="hardware/qcom-caf/sm6225/media" name="SM6225-Devs-ID/hardware_qcom_media" remote="github" revision="14-caf-sm6225" />
```

Adapt new platform to your BoardConfigQcom.mk ROM:
- https://github.com/SM6225-Devs-ID/android_hardware_qcom-caf_common/commit/a48d4bc534f0c7372e99ce37be131041e95b8777

- https://github.com/SM6225-Devs-ID/android_hardware_qcom-caf_common/commit/6bbe2e1716588743288780c7b8f6efe6e679b70d

- https://github.com/SM6225-Devs-ID/android_hardware_qcom-caf_common/commit/24d2155b4da096839a2529740346e9112e3e3f0e

- https://github.com/SM6225-Devs-ID/android_hardware_qcom-caf_common/commit/8da8f41bc8268cf151dd38773e3b644ad6ef0c32

- https://github.com/SM6225-Devs-ID/android_hardware_qcom-caf_common/commit/7637025dc36e0b1a9f852cacc26c0e9606377824

- https://github.com/SM6225-Devs-ID/android_hardware_qcom-caf_common/commit/c3176db584c5b3d305c947f8945f6a746ae8238a

Clone device tree to your initialize repo,done!!

Compile Now!!