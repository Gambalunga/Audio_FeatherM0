### Arduino Audio Library for Arduino SAMD21

This polyphonic library allows you to play WAV files from SPI Flash and SD card. Plays up to ~4 WAV files simultaneously. 

Medium quality output 8bit and up to 44.1khz if using QUAD SPI flash on the Adafruit M0 boards. Reduced quality ~22khz using an SD card. 

It all sound fairly marginal at 8bit. Until we get 16bit DMA output going on the SAMD21, for good sound quality, I recommend going with a [Teensy](https://www.pjrc.com/teensy/td_libs_Audio.html) or a peripherial codec to do the heavy lifting.

This library plays WAV files stored on the SPI Flash Adafruit includes on their Express boards. 
This includes: 
* Itsybits M0 Express (tested) 
* Trinket M0 Express (have board will test) 
* ItsyBitsy M4 Express 
* Feather M0 Express



Read this great description in the Adafruit tutorial for getting the WAV files onto your Adafruit M0 Express board https://learn.adafruit.com/introducing-itsy-bitsy-m0?view=all#using-spi-flash Thanks to Tondy Dicola and Adafruit for making this so easy!

For the SD card use these lines need to be edited in SamdAudio.cpp

![edits sd](https://github.com/hydronics2/SamdAudio/blob/master/library_modification_SD_card.JPG)

To revert back to the default flash storage use:

![edits flash](https://github.com/hydronics2/SamdAudio/blob/master/library_modification_flash.JPG)
