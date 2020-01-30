Filer på denne webside
----------------------

### Download som mappe på egen computer

- [installere git](https://git-scm.com/downloads) 
- åbn et console vindue (windows: Sartknap->kør->skriv cmd)
- udfør kommandoen: <b>git clone https://github.com/bvirk/myMicrobit</b>

----

### Min egen regel om filendelser for microbit program og hex filer

Microbit hex filer skal ende på .hex fordi

- block og python editor vil kun hente dem ind hvis de hedder .hex
- _ikke_ for at kunne flashe - microbit drevet er ligeglad med fil-endelsen

#### regel

- block hex fil: .t.hex
- block program fil: .ts
- python hex fil: .p.hex
- python program fil: .py

### Sproget dansk i program filer

Det er lettest at huske og forstå når ord kan genkendes - engelske ord kan gøre forståelse sværere.  

Jeg gør det bare ikke i programmer- jeg ville _INTET_ interessant vide om computere hvis jeg skulle have læst det på dansk.

Så - 'en knap' hedder 'a button' osv. - det er ikke Shakespeare engelsk!

[probarbility of getting online help and important knowledge](https://en.wikipedia.org/wiki/List_of_languages_by_total_number_of_speakers)

Eller på  dansk: sansynligheden for at finde beskrivelser og løsninger er 200 gange højere på engelsk end dansk.

Denne README.md fil beskriver
-----------------------------

- links
- noter
- lidt om mine små projekter


### programmering  og viden på microbit.com


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

### dyberegående hardware

- [mbed microbit](https://os.mbed.com/teams/microbit/)

## project [plotBarSTick](https://makecode.microbit.org/_WgzEqqPCVcR9)

##### Beskrivelse

Viser spænding som input fra AnalogPin.P0 som en pind der starter i nederste højre hjørne og er knækket af hver i venstre side for at fortsætte i linien over i højre side.

Fra 0 til 3.3 volt viser som fra ingen til alle lysdioder tændt.  

Målingen optræder også som output på AnalogPin.p1 på en af måderne

1. Pulsbredde til en servo - positiv signal af 1-2 ms varighed hver 20ms
2. Pulsbredde hvis 20ms periodetid kan varieres i dutycycle fra næsten 0 til næsten 100
3. Intet signal - udgang lav.

##### OM

1. lavet i typescript (som ikke helt er javascript)
2. udkommentering forsvinder ved tilbageskift til typescript
3. function plotBarStick
    - x,y
    - plot
    - stick
    - Dirty trick |0
4. enums
5. visningstilstand
6. dirty trick ^1
7. clearScreen vs basic.clearScreen
8. lower camelcase
9. PulseWidth  vs NoneOut
10. showVoltage - retvisende implicit sandhedsværdi
11. block - se udkommentering


