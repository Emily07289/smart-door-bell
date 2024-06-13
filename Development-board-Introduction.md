AMB82-MINI overview<br><br>
https://rkuo2000.github.io/EdgeAI-course/lecture/2024/03/01/Edge-AI-MCU-Intro.html<br>
--- ---
# Edge-AI MCU Introduction<br>
introduction to Edge-AI MCUs, MCU interfaces.<br>
--- ---
## Edge-AI MCU<br>
### Realtek AMB82-mini

 ![ ](https://camo.githubusercontent.com/2f3185a599037adeadd9b22bcc49a77b9a53198a5315207128641e1fa462ba26/68747470733a2f2f7777772e616d656261696f742e636f6d2f77702d636f6e74656e742f75706c6f6164732f323032332f30332f616d6238325f6d696e692e706e67)<br><br>
[RTL8735B](https://www.amebaiot.com/en/amebapro2/): 32-bit Arm v8M, up to 500MHz, 768KB ROM, 512KB RAM, 16MB Flash (MCM embedded DDR2/DDR3L up to 128MB) 802.11 a/b/g/n WiFi 2.4GHz/5GHz, BLE 5.1, NN Engine 0.4 TOPS, Crypto Engine, Audo Codec, …<br><br>
[Ameba Arduino](https://www.amebaiot.com/en/ameba-arduino-summary/)<br><br>
[Amebapro2 AMB82-mini Arduino Example Guides](https://www.amebaiot.com/en/amebapro2-amb82-mini-arduino-peripherals-examples)<br><br>
[Amebapro2 AMB82-mini Arduino getting started](https://www.amebaiot.com/en/amebapro2-amb82-mini-arduino-getting-started/)<br><br>
--- ---
### Nvidia Jetson<br>
Jetson Orin NX | Jetson Nano<br>
 ![ ](https://camo.githubusercontent.com/389eae433e4ca556e231ee49eaebd9a25f385083098ab86d837874776fd72667/68747470733a2f2f6763732e72696d672e636f6d2e74772f67342f3236352f6433352f706c6179726f626f742d696e632f642f34622f36652f32323332353031333036343535385f3739322e706e67)
 ![ ](https://camo.githubusercontent.com/0d49ccc514b857e12f89ad9398abe46b296a972ddbcbab4aae05acc9f4113342/68747470733a2f2f7777772e78696d65612e636f6d2f737570706f72742f6174746163686d656e74732f646f776e6c6f61642f31333034352f6a6574736f6e2d6e616e6f5f6e76696469615f6d6f64756c652e6a7067)
--- ---
[Jetson module comparison](https://connecttech.com/jetson/jetson-module-comparison/)<br><br>
* Jetson Nano 4G = 0.472 TOPs<br>
* Xavier NX 8GB = 21 TOPs<br>
* AGX Xavier = 32 TOPs<br>
* Orin NX 8GB = 70 TOPs<br>
* Orin NX 16GB = 100 TOPs<br>
* AGX Orin 32GB = 200 TOPs<br>
* AGX Orin 64GB = 275 TOPs<br><br>
--- ---
### Kneron KL520<br>
 ![ ](https://camo.githubusercontent.com/6b500740b330c59686a20999afca41e1ef3c947801f91042b1f0f2578e5b8424/68747470733a2f2f696d6167652e6b6e65726f6e636c6f75642e636f6d2f70726f647563742f4857323032313033313830303030303031382f68617264776172652d707265766965772d696d6167652d312e706e67)<br>
* support Framework: ONNX, Tensorflow, Keras, Caffe<br>
* support Model: VGG16, GoogleNet, YOLO, Tiny YOLO, Lenet, MobileNet, DenseNet<br>
* memory type: LPDDR2<br>
* NPU power efficiency : 0.55TOPS/W<br>
* Overall power consumption : 0.5W<br>
* Camera: EUA1200: 1080p progressive scan CMOS sensor<br>
--- ---
### [ESP32-S3-BOX-3](https://www.espressif.com/en/news/ESP32-S3-BOX-3)<br>
[Unboxing ESP32-S3-BOX-3](https://www.youtube.com/watch?v=4W3w93GQk7E&ab_channel=EspressifSystems)<br>
[Hardare Overview](https://github.com/espressif/esp-box/blob/master/docs/hardware_overview/esp32_s3_box_3/hardware_overview_for_box_3.md)<br>
 ![ ](https://github.com/espressif/esp-box/raw/master/docs/_static/box_3_hardware_overview/esp32_s3_box_3.png)<br>
--- ---
## MCU Interfaces introduction
### GPIO (General Purpose I/O)<br>
![](https://raw.githubusercontent.com/rkuo2000/EdgeAI-course/main/images/GPIO_circuit_diagram.png)<br>
![](https://github.com/rkuo2000/MCU-course/raw/main/images/GPIO_LED_circuit.png?raw=true)<br>
--- ---
### ADC (Analog Digital Converter)<br>
![](https://camo.githubusercontent.com/8d6570051f8ba5d87c21ae578c1196fab462708f6901d0ff4ce67fea293d395e/68747470733a2f2f726f636b75617070732e636f6d2f77702d636f6e74656e742f75706c6f6164732f323032302f31312f632d312d373931783631332e6a7067)<br>
**Vin** is input voltage for ADC to sample<br>
**Vref** is reference voltage for ADC to compare with Vin<br>
![](https://private-user-images.githubusercontent.com/161717296/313385938-f520773a-ec36-4ee0-8bea-f212facaf8dd.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTA2NzMzMDEsIm5iZiI6MTcxMDY3MzAwMSwicGF0aCI6Ii8xNjE3MTcyOTYvMzEzMzg1OTM4LWY1MjA3NzNhLWVjMzYtNGVlMC04YmVhLWYyMTJmYWNhZjhkZC5naWY_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMxN1QxMDU2NDFaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0xNzM4YTBiMDhiOTJiMTVjN2UxMDg1MzQ2NmQyNWVmOTM3OGUwMjhjYTdkMmQ3ZjhmM2M0ZTU3NWFlZTAwMDk4JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.S-3JUvKwus6LCjJDTZORYrsA3nK4ebJg4w78gymEyKg)<br>
--- ---
**12-bit ADC** output is a 12-bit binary code, so its value = 0 ~ 4095<br>
![](https://github.com/rkuo2000/MCU-course/raw/main/images/ADC_12bit_table.png?raw=true)<br><br>
### Direct-Conversion ADC<br>
![](https://camo.githubusercontent.com/e136b0af6de1bb9f03230178e79f8897ba4c4eae061fe7378c77f26ee8903fd3/68747470733a2f2f7777772e6d6178696d696e74656772617465642e636f6d2f636f6e74656e742f64616d2f696d616765732f64657369676e2f746563682d646f63732f3633342f45333346696730312e676966)<br>
### Successive-Approximation ADC<br>
![](https://github.com/rkuo2000/MCU-course/raw/main/images/SA_ADC_block_diagram.png?raw=true)<br>
### Sigma-Delta ADC
![](https://github.com/rkuo2000/MCU-course/raw/main/images/Sigma-Delta_ADC_block_diagram.png?raw=true)<br>
--- ---
### DAC (Digital to Analog Converter)<br>
[Introduction to Digital-Analog Conversion]<br>
### Binary-Weighted Resistor DAC
![](https://camo.githubusercontent.com/3732b80cc708c217e66ef513e09b0ca94e4c4c245e6a06da4a85f110725640b7/68747470733a2f2f7777772e616c6c61626f757463697263756974732e636f6d2f75706c6f6164732f61727469636c65732f696e76657274696e672d73756d6d696e672d636972637569742d6469616772616d2e6a7067)<br>
![](https://camo.githubusercontent.com/009f0db3e1c1ad3be114b6e3f7a8825cfc3c693d0218732a103a00687765ef93/68747470733a2f2f7777772e616c6c61626f757463697263756974732e636f6d2f75706c6f6164732f61727469636c65732f362d6269742d62696e6172792d77656967687465642d4441432e6a7067)<br>
--- ---
### PWM (Pulse Width Modulation)<br>
![](https://github.com/rkuo2000/MCU-course/raw/main/images/PWM_functional_diagram.png?raw=true)<br>
CMR >= CNR: PWM output high CMR < CNR: PWM output low PWM Frequency= PWM_Clock/(prescale)*(clock divider)/ CNR<br>
![](https://camo.githubusercontent.com/cc09ed1c66ad20c67e12c1461275b5dd394a73fef4575fd21010a865b355f842/68747470733a2f2f6d6963726f636f6e74726f6c6c6572736c61622e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031392f30342f536572766f2d6d6f746f722d70696e6f75742d65737033322e706e67)<br>
**Duty ratio**= CMR /CNR<br>
--- ---
### I2C (Inter-Integrated Circuit bus)<br>
[I2C bus 簡介](https://magicjackting.pixnet.net/blog/post/173061691)<br>
![](https://camo.githubusercontent.com/6b2311cc3778de9dbb8c1ab9b84e70618c8674a86120666472608f25d6ac4860/68747470733a2f2f7069632e70696d672e74772f6d616769636a61636b74696e672f313434373338323335312d323930393138353236302e706e67)
![](https://camo.githubusercontent.com/5f9b55e2309b359ae305e583c5a833ee302471681fdd904142b5f3764fdca71e/68747470733a2f2f7069632e70696d672e74772f6d616769636a61636b74696e672f313434373733393038352d3233393136303232302e706e67)<br>
![](https://camo.githubusercontent.com/00dc194bbf843ec1ab445c5c1a5e6e40548e43e995186707a421400d64818066/68747470733a2f2f7069632e70696d672e74772f6d616769636a61636b74696e672f313435303738373334312d333539373630393131345f6e2e706e673f763d31343631383039333434)<br>
![](https://camo.githubusercontent.com/2398a8349042646630eb01235b460e268fef3918f66b49d1721efea1744b759f/68747470733a2f2f7069632e70696d672e74772f6d616769636a61636b74696e672f313436313635393430312d3235383436373431362e706e67)<br>
![](https://github.com/rkuo2000/EdgeAI-course/raw/main/images/Example_BMP085.jpg?raw=true)<br>
![](https://github.com/rkuo2000/EdgeAI-course/raw/main/images/Example_BMP280.jpg?raw=true)<br>
--- ---
### SPI (Serial peripheral interface)<br>
[Introduction to SPI Interface](https://www.analog.com/en/resources/analog-dialogue/articles/introduction-to-spi-interface.html)<br>
* CS : Chip select
* SCLK: SPI Clock
* MOSI: Master out, slave in
* MISO: Master in, slave out 
--- ---
### I2S (Inter-IC Sound bus)<br>
[Introdution to the I2C Interface](https://www.allaboutcircuits.com/technical-articles/introduction-to-the-i2s-interface/)<br>
![](https://camo.githubusercontent.com/e0bf14abfde1d29f8cd6fed16e4034cc01e6a0f0fc18b98eb4179eed62724db5/68747470733a2f2f7777772e616c6c61626f757463697263756974732e636f6d2f75706c6f6164732f61727469636c65732f696e74726f64756374696f6e2d746f2d7468652d6932732d696e746572666163655f726b5f6161635f696d616765312e6a7067)<br>
![](https://camo.githubusercontent.com/c3660f1f2a77ad086622100cca5c4ee3e4edf500afb928ff16166fc5c1f90bb5/68747470733a2f2f7777772e616c6c61626f757463697263756974732e636f6d2f75706c6f6164732f61727469636c65732f696e74726f64756374696f6e2d746f2d7468652d6932732d696e746572666163655f726b5f6161635f696d616765322e6a7067)<br>
--- ---
### UART（Universal Asynchronous Receiver/Transmitter）序列埠<br>
[BASIC OF UARTCOMMUNICATION](https://www.circuitbasics.com/basics-uart-communication/)<br>
![](https://camo.githubusercontent.com/6d2febbd5c86a84d304c8374115544adf4f1241795eb84711f55731adc986a83/68747470733a2f2f7777772e636972637569746261736963732e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031362f30312f496e74726f64756374696f6e2d746f2d554152542d446174612d5472616e736d697373696f6e2d4469616772616d2e706e67)<br>
![](https://camo.githubusercontent.com/6269915a8fe7539fc805433db5d88f5a393d2157281ca00aa2923083c0029d93/68747470733a2f2f6d616b657270726f2e63632f77702d636f6e74656e742f75706c6f6164732f323031392f30382f322e706e67)<br>
![](https://camo.githubusercontent.com/2f5bab7bd6d3f35e8ef83c37900b073ae92520c07cba5fc09a46a83f5a7fa07e/68747470733a2f2f7777772e636972637569746261736963732e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031362f30312f496e74726f64756374696f6e2d746f2d554152542d5061636b65742d4672616d652d616e642d426974732d322e706e67)<br>
* Standard Packet : 8 data bits, even parity, 1 stop bit<br>
1. If the parity bit is a 0 (even parity), the 1 bits in the data frame should total to an even number.<br>
2. If the parity bit is a 1 (odd parity), the 1 bits in the data frame should total to an odd number.<br>
![](https://camo.githubusercontent.com/dbc03e128cecfd9a42ac1386a6656d47088c8bcae119a128ed37952d77b57012/68747470733a2f2f6d616b657270726f2e63632f77702d636f6e74656e742f75706c6f6164732f323031392f30382f342e706e67)<br>
的Vpp電壓較高，有 6V~30V；UART 則是較低的 3.3V 或 5V RS232 為負邏輯， UART 為正邏輯，因此兩者波形是反相的**Baud Rate**<br><br>

*This site was last updated March 17, 2024.*