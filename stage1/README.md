The initial stub for loading CTGP-R. According to the channel there are three different stubs, determined by reading byte 0x32 in the text section, which is a byte in the middle of a branch.

|Number|Byte 0x32|Text Size|Name in Repo|
|-|:-:|:-:|:-|
|1|0x16 (>= 6)|0x1B7A0|sd_stub_v0.dol|
|2|0x04 (< 5)|0x1A5E0|chan_stub.dol|
|3|0x05 (== 5)|0x1A640|sd_stub_v1.dol|

The boot.elf in the main download is identical to the boot.dol. At some point the SD stub was updated (SD00030004-SD00030006 2014-02-27), although I'm not sure what the difference is. The website changelog reads:

> Updates the files on the SD card used to launch the Channel to their latest version.

This update also updated the meta.xml file to include `ahb_access`.
