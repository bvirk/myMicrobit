### microbit.com links


- [blocks or python](https://www.microbit.org/code)
    - blocks and javascript coding
        - [let's code](https://makecode.microbit.org/#lang=da)
        - [reference](https://makecode.microbit.org/reference)
    - micro python
        - [let's code](https://python.microbit.org/) (starter editor)
        - [reference](https://microbit-micropython.readthedocs.io/en/latest/) : [via](https://microbit.org/guide/python/)
- [firmware flashing](https://microbit.org/guide/firmware/)

### hardware
        
- [Edge Connector & pinout](https://tech.microbit.org/hardware/edgeconnector/)   
- [Breakout board](https://www.kitronik.co.uk/pdf/5601b_built_edge_connector_breakout_board_for_the_bbc_microbit_datasheet_v1_1.pdf)
- [servo motor](https://learn.sparkfun.com/tutorials/hobby-servo-tutorial/all)


### project [plotBarSTick](https://makecode.microbit.org/_WgzEqqPCVcR9)

Shows voltage input on AnalogPin.P0. The reading is presented as a 25 leds stick, starting from bottom right corner and twisted at left for continueing at above row's right side. From 0 to 3.3.v is shown respectively as from no led's to all 25 led's lightening.  

The measurement appears one of following ways

1. PWM signal to a servo - positive signal of 1-2 ms length every 20ms
2. PWM signal, which 20ms time period dutycycle can be cnged fra nearly  0 to almost næsten 100
3. No signal - output low.

### Project [binClock](https://makecode.microbit.org/_LCHfvVM7pJYP)

Binary clock - the led rows shows, counting from top

1. hours
2. tens of minuts
3. ones of minuts
4. tens of seconds
5. ones of seconds

### project [tsOLED](https://makecode.microbit.org/_Y5iFb7dwYEhh)

### Future awesome Projects

- reciever for being a terminal
    - over bluetooth from app
    - over pc using usb or bluetooth
- writting to OLED display, implementing library:
    - lines to scrolling screen implementing
        - cr as \r 
    - redering mechanism for plotting rectangles of text - including
        - left/right/center rectangles
        - virtual y in sequence of block writing for expanding fields vertically
- lcr meter and transistor hfe tester
- controlling power supply
    - adjustable voltage/current
    - signal generation
    
