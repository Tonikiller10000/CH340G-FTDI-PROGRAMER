# CH340G-FTDI-PROGRAMER

## FTDI Programmer V2.0
An UART microcontroller programmer using CH340G IC. UART stands for Universal Asynchronous reciver/transmiter Protocol and it works like this:
The communication beggin with a start bit, continue with a data frame of 5 to 9 bits and an optional parity bit to check the sent data integrity, and ends with 1 or 2 stop bits.


<img src="https://github.com/Tonikiller10000/CH340G-FTDI-PROGRAMER/blob/main/FtdiProgramer_Pictures/b5.png" >
<img src="https://github.com/Tonikiller10000/CH340G-FTDI-PROGRAMER/blob/main/FtdiProgramer_Pictures/p7.png" width = 65% >
<img src="https://github.com/Tonikiller10000/CH340G-FTDI-PROGRAMER/blob/main/FtdiProgramer_Pictures/sch.png" width = 65% >


## How it works:
The CH340G ic transform the UART signal into USB signal and the other way around. For it to work, it needs an 12 MHz crystal oscilator and 2 capacitors, 2x 1K protection resistors. For 5V operation, pin 4 is connected to a 4.7-20nF ceramic decouplig capacitor to GND, and for 3.3V operation, it connects dirrectly to VCC. The FTDI programmer is recognised dirrectly by the computer and does not need any additional driver.
The USB data pins connect dirrectly to each other (D+ to D+ and D- to D-)

### CH340G pinout
<table>
  <tr><td>Nr.</td>   <td>Name</td>   <td>Function</td>                                                  </tr>
  <tr><td>1</td>     <td>GND</td>    <td>Ground reference of the chip.</td>                             </tr>
  <tr><td>2</td>     <td>TXD</td>    <td>UART Data Transmit output.</td>                                </tr>          
  <tr><td>3</td>     <td>RXD</td>    <td>UART Data Receive input.</td>                                  </tr>          
  <tr><td>4</td>     <td>V3</td>     <td>3.3V internal reference for USB. </td>                         </tr>          
  <tr><td>5</td>     <td>UD+</td>    <td>USB D+ signal.</td>                                            </tr>          
  <tr><td>6</td>     <td>UD-</td>    <td>USB D- signal.</td>                                            </tr>          
  <tr><td>7</td>     <td>XII</td>    <td>Crystal oscillator input.</td>                                 </tr>          
  <tr><td>8</td>     <td>XO</td>     <td>Output of the crystal oscillator.</td>                         </tr>          
  <tr><td>9</td>     <td>CTS</td>    <td>UART flow control signal Clear to Send.</td>                   </tr>          
  <tr><td>10</td>    <td>DSR</td>    <td>UART flow control signal Data Set Ready.</td>                  </tr>          
  <tr><td>11</td>    <td>RI</td>     <td>UART flow control signal Ring In.</td>                         </tr>          
  <tr><td>12</td>    <td>DCD</td>    <td>UART flow control signal Data Carrier Detect.</td>             </tr>          
  <tr><td>13</td>    <td>DTR</td>    <td>UART flow control signal Data Terminal Ready.</td>             </tr>          
  <tr><td>14</td>    <td>RTS</td>    <td>UART flow control signal Request to Send.</td>                 </tr>          
  <tr><td>15</td>    <td>R232</td>   <td>Auxiliary RS232 enable. Active high, internal pull down.</td>  </tr>          
  <tr><td>16</td>    <td>VCC</td>    <td>PowerSupply rail for the chip.</td>                            </tr>          
</table>


> [!NOTE]
> When programming a device, the Tx pin of the programmer conect\`s to the device Rx pin and the Rx of the programmer to the Tx of the device.

## FTDI Programmer V2.1
This is a new design witch includes an [3.3V voltage regulator on the back of the board](https://github.com/Tonikiller10000/CH340G-FTDI-PROGRAMER/blob/main/FtdiProgramer_Pictures/ss3.png) to be used on the 3.3V devices programming. It also has some other pins pulled out to be able to program stuff trouth the serial port. <br>
To select between the 5V and 3.3V modes, an pin jumper cap is used. 

<img src="https://github.com/Tonikiller10000/CH340G-FTDI-PROGRAMER/blob/main/FtdiProgramer_Pictures/ss2.png" >
<img src="https://github.com/Tonikiller10000/CH340G-FTDI-PROGRAMER/blob/main/FtdiProgramer_Pictures/ss1.png" >


## Links: 
- CH340G Datasheet1: https://pdf1.alldatasheet.com/datasheet-pdf/view/1132618/ETC2/CH340G.html
- CH340G Datasheet2: https://www.mpja.com/download/35227cpdata.pdf
- target: https://github.com/Tonikiller10000/CH340G-FTDI-PROGRAMER/blob/main/FtdiProgramer_Pictures/target.png
- proof of work V1: https://github.com/Tonikiller10000/CH340G-FTDI-PROGRAMER/blob/main/FtdiProgramer_Pictures/ProofOfWorkV1/




















