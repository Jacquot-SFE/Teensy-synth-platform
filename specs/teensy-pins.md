# Pin functions of the Teensy 3.2.

*And their mapping to signals for the audio shield.*

Adapted from the postcard that comes with the Teensy, with the audio shield signals added.

## Main column 1 (pins 0..12)

<table class="table table-striped">
<tr align="center"><td colspan="6"><b>Teensy 3.2 pins 0..12</b></td></tr>
<tr align="center"><td><b>Pin #</b></td> <td><b>Basic Function<br>(Digital IO#)</b></td> <td><b>Audio Shield uses?</b></td><td><b>Alt Func 1</b></td>  <td><b>Alt Func 2</b></td><td><b>Alt Func 2</b></td></tr>

<tr align="center"><td>1</td> <td>GND</td>  <td>Y</td>  <td></td><td></td><td></td></tr>
<tr align="center"><td>2</td> <td>0</td>  <td></td>  <td>RX1</td><td></td><td>Touch</td></tr>
<tr align="center"><td>3</td> <td>1</td>  <td></td>  <td>TX1</td><td></td><td>Touch</td></tr>
<tr align="center"><td>4</td> <td>2</td>  <td></td>  <td></td><td></td><td></td></tr>
<tr align="center"><td>5</td> <td>3</td>  <td></td>  <td></td><td>CanTX</td><td>PWM</td></tr>
<tr align="center"><td>6</td> <td>4</td>  <td></td>  <td></td><td>CanRX</td><td>PWM</td></tr>
<tr align="center"><td>7</td> <td>5</td>  <td>SD MOSI</td>  <td>TX1</td><td></td><td>PWM</td></tr>
<tr align="center"><td>8</td> <td>6</td>  <td>EEPROM CS</td>  <td></td><td></td><td>PWM</td></tr>
<tr align="center"><td>9</td> <td>7</td>  <td></td>  <td>RX3</td><td>DOUT</td><td></td></tr>
<tr align="center"><td>10</td> <td>8</td>  <td></td>  <td>TX3</td><td>DIN</td><td></td></tr>
<tr align="center"><td>11</td> <td>9</td>  <td>I2S BCLK</td>  <td>RX2</td><td>CS</td><td></td></tr>
<tr align="center"><td>12</td> <td>10</td>  <td>SD CS</td>  <td>TX2</td><td>CS</td><td></td></tr>
<tr align="center"><td>13</td> <td>11</td>  <td>I2S MCLK</td>  <td></td><td>DOUT</td><td></td></tr>
<tr align="center"><td>14</td> <td>12</td>  <td>DS MISO</td>  <td></td><td>DIN</td><td></td></tr>
</table>

## Main Column 2 (pins 13..23)

<table class="table table-striped">
<tr align="center"><td colspan="6"><b>Teensy 3.2 pins 13..23</b></td></tr>
<tr align="center"><td><b>Pin #</b></td> <td><b>Basic Function<br>(Digital IO#)</b></td> <td><b>Audio Shield uses?</b></td><td><b>Alt Func 1</b></td>  <td><b>Alt Func 2</b></td><td><b>Alt Func 2</b></td></tr>

<tr align="center"><td>15</td> <td>13</td>  <td>I2S TX</td>  <td>LED</td><td>SCK</td><td></td></tr>
<tr align="center"><td>16</td> <td>14</td>  <td>SD CLK</td>  <td>A0</td> <td>SCK</td><td></td></tr>
<tr align="center"><td>17</td> <td>15</td>  <td>(Optional Vol Pot on A1)</td>  <td>A1</td> <td>CS</td><td>Touch</td></tr>
<tr align="center"><td>18</td> <td>16</td>  <td></td>  <td>A2</td> <td>SCL0</td><td>Touch</td></tr>
<tr align="center"><td>19</td> <td>17</td>  <td></td>  <td>A3</td> <td>SDA0</td><td>Touch</td></tr>
<tr align="center"><td>20</td> <td>18</td>  <td>SDA0</td>  <td>A4</td> <td>SDA0</td><td>Touch</td></tr>
<tr align="center"><td>21</td> <td>19</td>  <td>SCL0</td>  <td>A5</td> <td>SCL0</td><td>Touch</td></tr>
<tr align="center"><td>22</td> <td>20</td>  <td></td>  <td>A6</td> <td>CS</td><td>PWM</td></tr>
<tr align="center"><td>23</td> <td>21</td>  <td></td>  <td>A7</td> <td>RX1</td><td>CS</td><td>PWM</td></tr>
<tr align="center"><td>24</td> <td>22</td>  <td>I2S RX</td>  <td>A8</td> <td>Touch</td><td>PWM</td></tr>
<tr align="center"><td>25</td> <td>23</td>  <td>I2S LRCLK</td>  <td>A9</td> <td>Touch</td><td>PWM</td></tr>
<tr align="center"><td>26</td> <td>3.3V</td>  <td>3.3V</td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td>27</td> <td>AGND</td>  <td>(kinda - for vol pot)</td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td>28</td> <td>VIN</td>  <td></td>  <td></td>  <td></td><td></td></tr>
</table>

## End Row

*Not including the pins on the above columns.*

<table class="table table-striped">
<tr align="center"><td colspan="6"><b>Teensy 3.2 pins 0..12</b></td></tr>
<tr align="center"><td><b>Pin #</b></td> <td><b>Basic Function<br>(Digital IO#)</b></td> <td><b>Audio Shield uses?</b></td><td><b>Alt Func 1</b></td>  <td><b>Alt Func 2</b></td><td><b>Alt Func 2</b></td></tr>

<tr align="center"><td></td> <td>A14</td>  <td></td>  <td>DAC</td><td></td><td></td></tr>
<tr align="center"><td></td> <td>Program</td>  <td></td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>GND</td>  <td></td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>3.3V</td>  <td></td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>VBat</td>  <td></td>  <td></td> <td></td><td></td></tr>
</table>

----------------------


## Backside dual-row-header col 1 (28..A12)

Some of these make more sense when viewed side by side with the other column.

<table class="table table-striped">
<tr align="center"><td colspan="6"><b>Teensy 3.2 DRH pins 28..A12</b></td></tr>
<tr align="center"><td><b>Pin #</b></td> <td><b>Basic Function<br>(Digital IO#)</b></td> <td><b>Audio Shield uses?</b></td><td><b>Alt Func 1</b></td>  <td><b>Alt Func 2</b></td><td><b>Alt Func 2</b></td></tr>

<tr align="center"><td></td> <td>28</td>  <td></td>  <td>A17</td><td></td><td></td></tr>
<tr align="center"><td></td> <td>27</td>  <td></td>  <td>A16</td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>26</td>  <td></td>  <td>A15</td> <td>RX2</td><td></td></tr>
<tr align="center"><td></td> <td>25</td>  <td></td>  <td>Touch</td> <td>PWM</td><td></td></tr>
<tr align="center"><td></td> <td>24</td>  <td></td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>GND</td>  <td></td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>A12</td>  <td></td>  <td></td> <td></td><td></td></tr>
</table>

## Backside dual-row-header col 2(29..AREF)

**Including the extra off-grid pads**

Some of these make more sense when viewed side by side with the other column.

<table class="table table-striped">
<tr align="center"><td colspan="6"><b>Teensy 3.2 DRH pins 29..AREF</b></td></tr>
<tr align="center"><td><b>Pin #</b></td> <td><b>Basic Function<br>(Digital IO#)</b></td> <td><b>Audio Shield uses?</b></td><td><b>Alt Func 1</b></td>  <td><b>Alt Func 2</b></td><td><b>Alt Func 2</b></td></tr>

<tr align="center"><td></td> <td>29</td>  <td></td>  <td>A18</td><td>SCL1</td><td></td></tr>
<tr align="center"><td></td> <td>30</td>  <td></td>  <td>A19</td> <td>SDA1</td><td></td></tr>
<tr align="center"><td></td> <td>31</td>  <td></td>  <td>A20</td> <td>TX2</td><td></td></tr>
<tr align="center"><td></td> <td>32</td>  <td></td>  <td>Touch</td> <td>PWM</td><td></td></tr>
<tr align="center"><td></td> <td>33</td>  <td></td>  <td>Touch</td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>3.3V</td>  <td></td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>A13</td>  <td></td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>A11</td>  <td></td>  <td></td><td></td><td></td></tr>
<tr align="center"><td></td> <td>A10</td>  <td></td>  <td></td> <td></td><td></td></tr>
<tr align="center"><td></td> <td>AREF</td>  <td>(kinda)</td>  <td></td> <td></td><td></td></tr>
</table>
