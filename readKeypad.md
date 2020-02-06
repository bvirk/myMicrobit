## Aflæsning af numerisk keybad, generelt

Generelt muliggøres aflæsning af keypads ved at taster er forbundet i krydsningspukter mellem et antal ledere på en led og et andet antal ledere på en anden led.  

Det ene antal ledere, her kaldet rækker er input der som udgangspukt har digital niveau 1 idet der er forbundet med pullup modstande til vcc (spænding på 3.3 volt)

Det andet antal ledere, her kaldet søjler (eng. columns) er udgange der som udgangspunkt har nivea høj.

Man genneløber så en cyklys hvor der læses niveauet på alle rækker for hver gang en enkelt søjle er holdt lav.

## Pins i Microbit

er enums konstanter som DigitalPin.P5 hvilket i virkeligheden er andre heltal (musmarkør over P5 i bloks typescript (misvisende kaldet javascript) viser det). Visse programmeringstricks er lettere med heltal - måden er indeksering med arrays 



    P0 ---1---2---3 
          |   |   | 
    P1 ---4---5---6 
          |   |   | 
    P8 ---7---8---9 
          |   |   | 
    P2 ---*---0---# 
          |   |   |   
         P5  P11  P16  


## Bloks typescript


    function readSteadyRow(row: number): number {
        let bits = readRow()
        if (bits == 7)
            return 0;
        basic.pause(10)
        // bit low  4   2   1
        // value    3   5   6
        // ^7       4   2   1
        // row0     1   2   3    
        // row1     4   5   6
        // row2     7   8   9
        // row3     *   0   #
        if (readRow() != bits)
            return 0
        bits = 4 - ((bits ^ 7) - (bits == 3 ? 1 : 0))
        return bits + 3 * row
    
    }
    function readRow(): number {
        return 4 * pins.digitalReadPin(DigitalPin.P5)
            | 2 * pins.digitalReadPin(DigitalPin.P11)
            | pins.digitalReadPin(DigitalPin.P16)
    }
    
    function getkey(): number {
        //let pin: number[] = [7, 8, 15, 9]
        for (let row = 0; row < 4; row++) {
            for (let col = 0; col < 4; col++) {
                pins.digitalWritePin(pin[col], col == row ? 0 : 1)
            }
            basic.pause(20)
            let scan = readSteadyRow(row)
            if (scan != 0)
                return scan
        }
        return 0
    }
    let pin: number[] = [7, 8, 15, 9]
    basic.forever(function () {
        let key = getkey()
        if (key > 0)
            basic.showString(" 123456789*0#".charAt(key), 1)
    })

     
[readKeyPad](https://makecode.microbit.org/_LaYf5cC3ahEF) som makecode.microbit.org project _VIRKER IKKE_     



